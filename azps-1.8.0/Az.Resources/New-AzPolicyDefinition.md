---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 07882064fae3cfc4a24899b6106480551f3681a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747113"
---
# <span data-ttu-id="ecb16-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecb16-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="ecb16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecb16-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb16-103">Skapar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="ecb16-103">Creates a policy definition.</span></span>

## <span data-ttu-id="ecb16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecb16-104">SYNTAX</span></span>

### <span data-ttu-id="ecb16-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ecb16-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb16-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecb16-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb16-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecb16-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecb16-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecb16-108">DESCRIPTION</span></span>
<span data-ttu-id="ecb16-109">Cmdleten **New-AzPolicyDefinition** skapar en princip definition som innehåller en policy regel i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="ecb16-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="ecb16-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecb16-110">EXAMPLES</span></span>

### <span data-ttu-id="ecb16-111">Exempel 1: skapa en princip definition med hjälp av en princip fil</span><span class="sxs-lookup"><span data-stu-id="ecb16-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="ecb16-112">Det här kommandot skapar en princip definition med namnet LocationDefinition som innehåller policy regeln som angetts i C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="ecb16-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="ecb16-113">Exempel på innehåll för LocationPolicy.jsi filen visas ovan.</span><span class="sxs-lookup"><span data-stu-id="ecb16-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="ecb16-114">Exempel 2: skapa en parametriserad princip definition med hjälp av infogade parametrar</span><span class="sxs-lookup"><span data-stu-id="ecb16-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="ecb16-115">Det här kommandot skapar en princip definition med namnet LocationDefinition som innehåller policy regeln som angetts i C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="ecb16-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="ecb16-116">Parameter definitionen för policy regeln tillhandahålls infogad.</span><span class="sxs-lookup"><span data-stu-id="ecb16-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="ecb16-117">Exempel 3: skapa en princip definitions rad i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="ecb16-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="ecb16-118">Det här kommandot skapar en princip definition med namnet VMPolicyDefinition i Dept42 för hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="ecb16-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="ecb16-119">Kommandot anger principen som en sträng i giltigt JSON-format.</span><span class="sxs-lookup"><span data-stu-id="ecb16-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="ecb16-120">Exempel 4: skapa en princip definitions rad med metadata</span><span class="sxs-lookup"><span data-stu-id="ecb16-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="ecb16-121">Det här kommandot skapar en princip definition med namnet VMPolicyDefinition med metadata som visar att dess kategori är "virtuell dator".</span><span class="sxs-lookup"><span data-stu-id="ecb16-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="ecb16-122">Kommandot anger principen som en sträng i giltigt JSON-format.</span><span class="sxs-lookup"><span data-stu-id="ecb16-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="ecb16-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecb16-123">PARAMETERS</span></span>

### <span data-ttu-id="ecb16-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ecb16-124">-ApiVersion</span></span>
<span data-ttu-id="ecb16-125">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ecb16-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ecb16-126">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="ecb16-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb16-127">-DefaultProfile</span></span>
<span data-ttu-id="ecb16-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ecb16-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-129">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ecb16-129">-Description</span></span>
<span data-ttu-id="ecb16-130">Anger en beskrivning för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ecb16-130">Specifies a description for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ecb16-131">-DisplayName</span></span>
<span data-ttu-id="ecb16-132">Anger ett visnings namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ecb16-132">Specifies a display name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb16-133">-ManagementGroupName</span></span>
<span data-ttu-id="ecb16-134">Namnet på hanterings gruppen för den nya princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ecb16-134">The name of the management group of the new policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ecb16-135">-Metadata</span></span>
<span data-ttu-id="ecb16-136">Metadata för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ecb16-136">The metadata for policy definition.</span></span> <span data-ttu-id="ecb16-137">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata, eller metadata som sträng</span><span class="sxs-lookup"><span data-stu-id="ecb16-137">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-138">-Mode</span><span class="sxs-lookup"><span data-stu-id="ecb16-138">-Mode</span></span>
<span data-ttu-id="ecb16-139">Läget för princip definitionen</span><span class="sxs-lookup"><span data-stu-id="ecb16-139">The mode of the policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: All
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="ecb16-140">-Name</span></span>
<span data-ttu-id="ecb16-141">Anger ett namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ecb16-141">Specifies a name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-142">-Parameter</span><span class="sxs-lookup"><span data-stu-id="ecb16-142">-Parameter</span></span>
<span data-ttu-id="ecb16-143">Parameter deklarationen för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ecb16-143">The parameters declaration for policy definition.</span></span> <span data-ttu-id="ecb16-144">Det kan antingen vara en sökväg till ett fil namn som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="ecb16-144">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-145">-Princip</span><span class="sxs-lookup"><span data-stu-id="ecb16-145">-Policy</span></span>
<span data-ttu-id="ecb16-146">Anger en policy regel för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ecb16-146">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="ecb16-147">Du kan ange sökvägen till en. JSON-fil eller en sträng som innehåller principen i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="ecb16-147">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-148">-För</span><span class="sxs-lookup"><span data-stu-id="ecb16-148">-Pre</span></span>
<span data-ttu-id="ecb16-149">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ecb16-149">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecb16-150">-SubscriptionId</span></span>
<span data-ttu-id="ecb16-151">Abonnemangs-ID för den nya princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="ecb16-151">The subscription ID of the new policy definition.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb16-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb16-152">CommonParameters</span></span>
<span data-ttu-id="ecb16-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecb16-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb16-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecb16-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb16-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecb16-155">INPUTS</span></span>

### <span data-ttu-id="ecb16-156">System. String</span><span class="sxs-lookup"><span data-stu-id="ecb16-156">System.String</span></span>

### <span data-ttu-id="ecb16-157">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ecb16-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ecb16-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecb16-158">OUTPUTS</span></span>

### <span data-ttu-id="ecb16-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ecb16-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ecb16-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecb16-160">NOTES</span></span>

## <span data-ttu-id="ecb16-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecb16-161">RELATED LINKS</span></span>

[<span data-ttu-id="ecb16-162">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecb16-162">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="ecb16-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecb16-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="ecb16-164">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecb16-164">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


