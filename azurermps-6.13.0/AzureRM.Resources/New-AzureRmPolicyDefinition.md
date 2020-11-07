---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 22c8ea5c93a301796b2b42184a54744e9841163d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755185"
---
# <span data-ttu-id="a0d6f-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a0d6f-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="a0d6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d6f-103">Skapar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0d6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0d6f-104">SYNTAX</span></span>

### <span data-ttu-id="a0d6f-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a0d6f-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a0d6f-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0d6f-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a0d6f-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0d6f-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a0d6f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0d6f-108">DESCRIPTION</span></span>
<span data-ttu-id="a0d6f-109">Cmdleten **New-AzureRmPolicyDefinition** skapar en princip definition som innehåller en policy regel i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="a0d6f-109">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="a0d6f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0d6f-110">EXAMPLES</span></span>

### <span data-ttu-id="a0d6f-111">Exempel 1: skapa en princip definition med hjälp av en princip fil</span><span class="sxs-lookup"><span data-stu-id="a0d6f-111">Example 1: Create a policy definition by using a policy file</span></span>
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
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="a0d6f-112">Det här kommandot skapar en princip definition med namnet LocationDefinition som innehåller policy regeln som angetts i C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="a0d6f-113">Exempel på innehåll för LocationPolicy.jsi filen visas ovan.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="a0d6f-114">Exempel 2: skapa en parametriserad princip definition med hjälp av infogade parametrar</span><span class="sxs-lookup"><span data-stu-id="a0d6f-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="a0d6f-115">Det här kommandot skapar en princip definition med namnet LocationDefinition som innehåller policy regeln som angetts i C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="a0d6f-116">Parameter definitionen för policy regeln tillhandahålls infogad.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="a0d6f-117">Exempel 3: skapa en princip definitions rad i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="a0d6f-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="a0d6f-118">Det här kommandot skapar en princip definition med namnet VMPolicyDefinition i Dept42 för hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="a0d6f-119">Kommandot anger principen som en sträng i giltigt JSON-format.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="a0d6f-120">Exempel 4: skapa en princip definitions rad med metadata</span><span class="sxs-lookup"><span data-stu-id="a0d6f-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="a0d6f-121">Det här kommandot skapar en princip definition med namnet VMPolicyDefinition med metadata som visar att dess kategori är "virtuell dator".</span><span class="sxs-lookup"><span data-stu-id="a0d6f-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="a0d6f-122">Kommandot anger principen som en sträng i giltigt JSON-format.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="a0d6f-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0d6f-123">PARAMETERS</span></span>

### <span data-ttu-id="a0d6f-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a0d6f-124">-ApiVersion</span></span>
<span data-ttu-id="a0d6f-125">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a0d6f-126">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a0d6f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d6f-127">-DefaultProfile</span></span>
<span data-ttu-id="a0d6f-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a0d6f-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d6f-129">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a0d6f-129">-Description</span></span>
<span data-ttu-id="a0d6f-130">Anger en beskrivning för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="a0d6f-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a0d6f-131">-DisplayName</span></span>
<span data-ttu-id="a0d6f-132">Anger ett visnings namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="a0d6f-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a0d6f-133">-InformationAction</span></span>
<span data-ttu-id="a0d6f-134">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-134">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="a0d6f-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a0d6f-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a0d6f-136">Vidare</span><span class="sxs-lookup"><span data-stu-id="a0d6f-136">Continue</span></span>
- <span data-ttu-id="a0d6f-137">Över</span><span class="sxs-lookup"><span data-stu-id="a0d6f-137">Ignore</span></span>
- <span data-ttu-id="a0d6f-138">Inquire</span><span class="sxs-lookup"><span data-stu-id="a0d6f-138">Inquire</span></span>
- <span data-ttu-id="a0d6f-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a0d6f-139">SilentlyContinue</span></span>
- <span data-ttu-id="a0d6f-140">Stanna</span><span class="sxs-lookup"><span data-stu-id="a0d6f-140">Stop</span></span>
- <span data-ttu-id="a0d6f-141">Avbryt</span><span class="sxs-lookup"><span data-stu-id="a0d6f-141">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d6f-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a0d6f-142">-InformationVariable</span></span>
<span data-ttu-id="a0d6f-143">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-143">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d6f-144">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d6f-144">-ManagementGroupName</span></span>
<span data-ttu-id="a0d6f-145">Namnet på hanterings gruppen för den nya princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-145">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="a0d6f-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a0d6f-146">-Metadata</span></span>
<span data-ttu-id="a0d6f-147">Metadata för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-147">The metadata for policy definition.</span></span> <span data-ttu-id="a0d6f-148">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata, eller metadata som sträng</span><span class="sxs-lookup"><span data-stu-id="a0d6f-148">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="a0d6f-149">-Mode</span><span class="sxs-lookup"><span data-stu-id="a0d6f-149">-Mode</span></span>
<span data-ttu-id="a0d6f-150">Läget för princip definitionen</span><span class="sxs-lookup"><span data-stu-id="a0d6f-150">The mode of the policy definition</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d6f-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0d6f-151">-Name</span></span>
<span data-ttu-id="a0d6f-152">Anger ett namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-152">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="a0d6f-153">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a0d6f-153">-Parameter</span></span>
<span data-ttu-id="a0d6f-154">Parameter deklarationen för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-154">The parameters declaration for policy definition.</span></span> <span data-ttu-id="a0d6f-155">Det kan antingen vara en sökväg till ett fil namn som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-155">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="a0d6f-156">-Princip</span><span class="sxs-lookup"><span data-stu-id="a0d6f-156">-Policy</span></span>
<span data-ttu-id="a0d6f-157">Anger en policy regel för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-157">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="a0d6f-158">Du kan ange sökvägen till en. JSON-fil eller en sträng som innehåller principen i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-158">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="a0d6f-159">-För</span><span class="sxs-lookup"><span data-stu-id="a0d6f-159">-Pre</span></span>
<span data-ttu-id="a0d6f-160">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-160">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a0d6f-161">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0d6f-161">-SubscriptionId</span></span>
<span data-ttu-id="a0d6f-162">Abonnemangs-ID för den nya princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-162">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="a0d6f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d6f-163">CommonParameters</span></span>
<span data-ttu-id="a0d6f-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d6f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d6f-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d6f-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d6f-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0d6f-166">INPUTS</span></span>

## <span data-ttu-id="a0d6f-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0d6f-167">OUTPUTS</span></span>

## <span data-ttu-id="a0d6f-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0d6f-168">NOTES</span></span>

## <span data-ttu-id="a0d6f-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0d6f-169">RELATED LINKS</span></span>

[<span data-ttu-id="a0d6f-170">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a0d6f-170">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="a0d6f-171">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a0d6f-171">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="a0d6f-172">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a0d6f-172">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


