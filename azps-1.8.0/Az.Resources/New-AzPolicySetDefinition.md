---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: cf1f1993c58e9c87c36538199555e5ebd7c2175a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747107"
---
# <span data-ttu-id="65552-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="65552-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="65552-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65552-102">SYNOPSIS</span></span>
<span data-ttu-id="65552-103">Skapar en definition för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="65552-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="65552-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65552-104">SYNTAX</span></span>

### <span data-ttu-id="65552-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="65552-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65552-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="65552-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65552-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65552-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65552-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65552-108">DESCRIPTION</span></span>
<span data-ttu-id="65552-109">Cmdleten **New-AzPolicySetDefinition** skapar en definition för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="65552-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="65552-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65552-110">EXAMPLES</span></span>

### <span data-ttu-id="65552-111">Exempel 1: skapa en definition för princip uppsättning med hjälp av en princip uppsättnings fil</span><span class="sxs-lookup"><span data-stu-id="65552-111">Example 1: Create a policy set definition by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="65552-112">Det här kommandot skapar en princip uppsättnings definition med namnet VMPolicyDefinition som innehåller de princip definitioner som anges i C:\VMPolicy.jspå.</span><span class="sxs-lookup"><span data-stu-id="65552-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="65552-113">Exempel på innehållet i VMPolicy.jsär aktiverat ovan.</span><span class="sxs-lookup"><span data-stu-id="65552-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="65552-114">Exempel 2: skapa en definition för parameter uppsättning</span><span class="sxs-lookup"><span data-stu-id="65552-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="65552-115">Det här kommandot skapar en parameter uppsättnings definition med namnet VMPolicyDefinition som innehåller de princip definitioner som anges i C:\VMPolicy.jspå.</span><span class="sxs-lookup"><span data-stu-id="65552-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="65552-116">Exempel på innehållet i VMPolicy.jsär aktiverat ovan.</span><span class="sxs-lookup"><span data-stu-id="65552-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="65552-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65552-117">PARAMETERS</span></span>

### <span data-ttu-id="65552-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="65552-118">-ApiVersion</span></span>
<span data-ttu-id="65552-119">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="65552-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="65552-120">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="65552-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="65552-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65552-121">-DefaultProfile</span></span>
<span data-ttu-id="65552-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="65552-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65552-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="65552-123">-Description</span></span>
<span data-ttu-id="65552-124">Beskrivningen för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="65552-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="65552-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="65552-125">-DisplayName</span></span>
<span data-ttu-id="65552-126">Visnings namnet för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="65552-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="65552-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="65552-127">-ManagementGroupName</span></span>
<span data-ttu-id="65552-128">Namnet på hanterings gruppen för den nya definitionen för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="65552-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="65552-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="65552-129">-Metadata</span></span>
<span data-ttu-id="65552-130">Metadata för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="65552-130">The metadata for policy set definition.</span></span> <span data-ttu-id="65552-131">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata, eller metadata som sträng</span><span class="sxs-lookup"><span data-stu-id="65552-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="65552-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="65552-132">-Name</span></span>
<span data-ttu-id="65552-133">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="65552-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="65552-134">-Parameter</span><span class="sxs-lookup"><span data-stu-id="65552-134">-Parameter</span></span>
<span data-ttu-id="65552-135">Parameter deklarationen för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="65552-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="65552-136">Det kan antingen vara en sökväg till ett fil namn som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="65552-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="65552-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="65552-137">-PolicyDefinition</span></span>
<span data-ttu-id="65552-138">Den här definitionen av princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="65552-138">The policy set definition.</span></span> <span data-ttu-id="65552-139">Det kan antingen vara en sökväg till ett fil namn som innehåller princip definitionerna, eller så är princip uppsättnings definitionen som sträng.</span><span class="sxs-lookup"><span data-stu-id="65552-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="65552-140">-För</span><span class="sxs-lookup"><span data-stu-id="65552-140">-Pre</span></span>
<span data-ttu-id="65552-141">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="65552-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="65552-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65552-142">-SubscriptionId</span></span>
<span data-ttu-id="65552-143">Prenumerations-ID för den nya definitionen för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="65552-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="65552-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="65552-144">-Confirm</span></span>
<span data-ttu-id="65552-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65552-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65552-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65552-146">-WhatIf</span></span>
<span data-ttu-id="65552-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="65552-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65552-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="65552-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65552-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65552-149">CommonParameters</span></span>
<span data-ttu-id="65552-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65552-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65552-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65552-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65552-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65552-152">INPUTS</span></span>

### <span data-ttu-id="65552-153">System. String</span><span class="sxs-lookup"><span data-stu-id="65552-153">System.String</span></span>

### <span data-ttu-id="65552-154">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="65552-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="65552-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65552-155">OUTPUTS</span></span>

### <span data-ttu-id="65552-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="65552-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="65552-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65552-157">NOTES</span></span>

## <span data-ttu-id="65552-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65552-158">RELATED LINKS</span></span>
