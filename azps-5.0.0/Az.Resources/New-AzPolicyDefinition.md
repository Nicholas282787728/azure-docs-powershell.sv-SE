---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 51c5608c8212b519e6ca979e470c2ab1a5d96e6b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322124"
---
# <span data-ttu-id="6d1ae-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6d1ae-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="6d1ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1ae-103">Skapar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-103">Creates a policy definition.</span></span>

## <span data-ttu-id="6d1ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d1ae-104">SYNTAX</span></span>

### <span data-ttu-id="6d1ae-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6d1ae-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d1ae-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d1ae-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d1ae-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d1ae-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d1ae-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d1ae-108">DESCRIPTION</span></span>
<span data-ttu-id="6d1ae-109">Cmdleten **New-AzPolicyDefinition** skapar en princip definition som innehåller en policy regel i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="6d1ae-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="6d1ae-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d1ae-110">EXAMPLES</span></span>

### <span data-ttu-id="6d1ae-111">Exempel 1: skapa en princip definition med hjälp av en princip fil</span><span class="sxs-lookup"><span data-stu-id="6d1ae-111">Example 1: Create a policy definition by using a policy file</span></span>
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

<span data-ttu-id="6d1ae-112">Det här kommandot skapar en princip definition med namnet LocationDefinition som innehåller policy regeln som angetts i C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="6d1ae-113">Exempel på innehåll för LocationPolicy.jsi filen visas ovan.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="6d1ae-114">Exempel 2: skapa en parametriserad princip definition med hjälp av infogade parametrar</span><span class="sxs-lookup"><span data-stu-id="6d1ae-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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

<span data-ttu-id="6d1ae-115">Det här kommandot skapar en princip definition med namnet LocationDefinition som innehåller policy regeln som angetts i C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="6d1ae-116">Parameter definitionen för policy regeln tillhandahålls infogad.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="6d1ae-117">Exempel 3: skapa en princip definitions rad i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="6d1ae-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="6d1ae-118">Det här kommandot skapar en princip definition med namnet VMPolicyDefinition i Dept42 för hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="6d1ae-119">Kommandot anger principen som en sträng i giltigt JSON-format.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="6d1ae-120">Exempel 4: skapa en princip definitions rad med metadata</span><span class="sxs-lookup"><span data-stu-id="6d1ae-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="6d1ae-121">Det här kommandot skapar en princip definition med namnet VMPolicyDefinition med metadata som visar att dess kategori är "virtuell dator".</span><span class="sxs-lookup"><span data-stu-id="6d1ae-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="6d1ae-122">Kommandot anger principen som en sträng i giltigt JSON-format.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="6d1ae-123">Exempel 5: skapa en princip definitions rad med ett läge</span><span class="sxs-lookup"><span data-stu-id="6d1ae-123">Example 5: Create a policy definition inline with mode</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'TagsPolicyDefinition' -Policy '{"if":{"value":"[less(length(field(''tags'')), 3)]","equals":true},"then":{"effect":"deny"}}' -Mode Indexed


Name               : TagsPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
ResourceName       : TagsPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=TagsPolicyDefinition; policyType=Custom; mode=Indexed; metadata=; parameters=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
```

<span data-ttu-id="6d1ae-124">Det här kommandot skapar en princip definition med namnet TagsPolicyDefinition med läget "indexerat" som anger att principen bara ska utvärderas för resurs typer som stöder taggar och plats.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="6d1ae-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d1ae-125">PARAMETERS</span></span>

### <span data-ttu-id="6d1ae-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6d1ae-126">-ApiVersion</span></span>
<span data-ttu-id="6d1ae-127">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6d1ae-128">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6d1ae-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1ae-129">-DefaultProfile</span></span>
<span data-ttu-id="6d1ae-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6d1ae-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d1ae-131">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6d1ae-131">-Description</span></span>
<span data-ttu-id="6d1ae-132">Anger en beskrivning för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="6d1ae-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6d1ae-133">-DisplayName</span></span>
<span data-ttu-id="6d1ae-134">Anger ett visnings namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="6d1ae-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6d1ae-135">-ManagementGroupName</span></span>
<span data-ttu-id="6d1ae-136">Namnet på hanterings gruppen för den nya princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="6d1ae-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6d1ae-137">-Metadata</span></span>
<span data-ttu-id="6d1ae-138">Metadata för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-138">The metadata for policy definition.</span></span> <span data-ttu-id="6d1ae-139">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata, eller metadata som sträng</span><span class="sxs-lookup"><span data-stu-id="6d1ae-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="6d1ae-140">-Mode</span><span class="sxs-lookup"><span data-stu-id="6d1ae-140">-Mode</span></span>
<span data-ttu-id="6d1ae-141">Läget för princip definitionen</span><span class="sxs-lookup"><span data-stu-id="6d1ae-141">The mode of the policy definition</span></span>

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

### <span data-ttu-id="6d1ae-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d1ae-142">-Name</span></span>
<span data-ttu-id="6d1ae-143">Anger ett namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-143">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="6d1ae-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="6d1ae-144">-Parameter</span></span>
<span data-ttu-id="6d1ae-145">Parameter deklarationen för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="6d1ae-146">Det kan antingen vara en sökväg till ett fil namn som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="6d1ae-147">-Princip</span><span class="sxs-lookup"><span data-stu-id="6d1ae-147">-Policy</span></span>
<span data-ttu-id="6d1ae-148">Anger en policy regel för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="6d1ae-149">Du kan ange sökvägen till en. JSON-fil eller en sträng som innehåller principen i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="6d1ae-150">-För</span><span class="sxs-lookup"><span data-stu-id="6d1ae-150">-Pre</span></span>
<span data-ttu-id="6d1ae-151">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6d1ae-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d1ae-152">-SubscriptionId</span></span>
<span data-ttu-id="6d1ae-153">Abonnemangs-ID för den nya princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="6d1ae-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1ae-154">CommonParameters</span></span>
<span data-ttu-id="6d1ae-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d1ae-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1ae-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d1ae-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1ae-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d1ae-157">INPUTS</span></span>

### <span data-ttu-id="6d1ae-158">System. String</span><span class="sxs-lookup"><span data-stu-id="6d1ae-158">System.String</span></span>

### <span data-ttu-id="6d1ae-159">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6d1ae-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6d1ae-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d1ae-160">OUTPUTS</span></span>

### <span data-ttu-id="6d1ae-161">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6d1ae-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6d1ae-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d1ae-162">NOTES</span></span>

## <span data-ttu-id="6d1ae-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d1ae-163">RELATED LINKS</span></span>

[<span data-ttu-id="6d1ae-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6d1ae-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="6d1ae-165">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6d1ae-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="6d1ae-166">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6d1ae-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


