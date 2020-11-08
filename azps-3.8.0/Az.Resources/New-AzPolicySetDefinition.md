---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091289"
---
# <span data-ttu-id="4aaa3-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="4aaa3-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="4aaa3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4aaa3-102">SYNOPSIS</span></span>
<span data-ttu-id="4aaa3-103">Skapar en definition för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="4aaa3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4aaa3-104">SYNTAX</span></span>

### <span data-ttu-id="4aaa3-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4aaa3-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aaa3-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aaa3-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4aaa3-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aaa3-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4aaa3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4aaa3-108">DESCRIPTION</span></span>
<span data-ttu-id="4aaa3-109">Cmdleten **New-AzPolicySetDefinition** skapar en definition för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="4aaa3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4aaa3-110">EXAMPLES</span></span>

### <span data-ttu-id="4aaa3-111">Exempel 1: skapa en definition för princip uppsättning med metadata genom att använda en princip uppsättnings fil</span><span class="sxs-lookup"><span data-stu-id="4aaa3-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="4aaa3-112">Det här kommandot skapar en princip uppsättnings definition med namnet VMPolicySetDefinition med metadata som visar att dess kategori är "virtuell dator" som innehåller de princip definitioner som anges i C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="4aaa3-113">Exempel på innehållet i VMPolicy.jsär aktiverat ovan.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="4aaa3-114">Exempel 2: skapa en definition för parameter uppsättning</span><span class="sxs-lookup"><span data-stu-id="4aaa3-114">Example 2: Create a parameterized policy set definition</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="4aaa3-115">Det här kommandot skapar en parameter uppsättnings definition med namnet VMPolicySetDefinition som innehåller de princip definitioner som anges i C:\VMPolicy.jspå.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="4aaa3-116">Exempel på innehållet i VMPolicy.jsär aktiverat ovan.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="4aaa3-117">Exempel 3: skapa en definition för princip uppsättningar med princip definitions grupper</span><span class="sxs-lookup"><span data-stu-id="4aaa3-117">Example 3: Create a policy set definition with policy definition groups</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "groupNames": [ "group1" ]
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf",
      "groupNames": [ "group2" ]
   }
]
```

```
$groupsJson = ConvertTo-Json @{ name = "group1" }, @{ name = "group2" }
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="4aaa3-118">Det här kommandot skapar en princip uppsättnings definition med namnet VMPolicySetDefinition med gruppering av princip definitioner som anges i C:\VMPolicy.jspå.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="4aaa3-119">Exempel på innehållet i VMPolicy.jsär aktiverat ovan.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="4aaa3-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4aaa3-120">PARAMETERS</span></span>

### <span data-ttu-id="4aaa3-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4aaa3-121">-ApiVersion</span></span>
<span data-ttu-id="4aaa3-122">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4aaa3-123">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4aaa3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aaa3-124">-DefaultProfile</span></span>
<span data-ttu-id="4aaa3-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4aaa3-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4aaa3-126">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4aaa3-126">-Description</span></span>
<span data-ttu-id="4aaa3-127">Beskrivningen för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="4aaa3-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4aaa3-128">-DisplayName</span></span>
<span data-ttu-id="4aaa3-129">Visnings namnet för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="4aaa3-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="4aaa3-130">-GroupDefinition</span></span>
<span data-ttu-id="4aaa3-131">Princip definitions grupperna för den nya definitionen för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="4aaa3-132">Det kan antingen vara en sökväg till en fil som innehåller grupperna eller grupperna som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="4aaa3-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4aaa3-133">-ManagementGroupName</span></span>
<span data-ttu-id="4aaa3-134">Namnet på hanterings gruppen för den nya definitionen för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="4aaa3-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4aaa3-135">-Metadata</span></span>
<span data-ttu-id="4aaa3-136">Metadata för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-136">The metadata for policy set definition.</span></span> <span data-ttu-id="4aaa3-137">Det kan vara en sökväg till ett fil namn som innehåller metadata, eller metadata som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="4aaa3-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="4aaa3-138">-Name</span></span>
<span data-ttu-id="4aaa3-139">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="4aaa3-140">-Parameter</span><span class="sxs-lookup"><span data-stu-id="4aaa3-140">-Parameter</span></span>
<span data-ttu-id="4aaa3-141">Parameter deklarationen för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="4aaa3-142">Det kan antingen vara en sökväg till ett fil namn som innehåller parameter deklarationen eller parameter deklarationen som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="4aaa3-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4aaa3-143">-PolicyDefinition</span></span>
<span data-ttu-id="4aaa3-144">Princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-144">The policy definitions.</span></span> <span data-ttu-id="4aaa3-145">Det kan vara en sökväg till ett fil namn som innehåller princip definitionerna eller princip definitionerna som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="4aaa3-146">-För</span><span class="sxs-lookup"><span data-stu-id="4aaa3-146">-Pre</span></span>
<span data-ttu-id="4aaa3-147">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4aaa3-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4aaa3-148">-SubscriptionId</span></span>
<span data-ttu-id="4aaa3-149">Prenumerations-ID för den nya definitionen för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="4aaa3-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4aaa3-150">-Confirm</span></span>
<span data-ttu-id="4aaa3-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aaa3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aaa3-152">-WhatIf</span></span>
<span data-ttu-id="4aaa3-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4aaa3-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aaa3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aaa3-155">CommonParameters</span></span>
<span data-ttu-id="4aaa3-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aaa3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aaa3-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4aaa3-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aaa3-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4aaa3-158">INPUTS</span></span>

### <span data-ttu-id="4aaa3-159">System. String</span><span class="sxs-lookup"><span data-stu-id="4aaa3-159">System.String</span></span>

### <span data-ttu-id="4aaa3-160">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4aaa3-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4aaa3-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4aaa3-161">OUTPUTS</span></span>

### <span data-ttu-id="4aaa3-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4aaa3-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4aaa3-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4aaa3-163">NOTES</span></span>

## <span data-ttu-id="4aaa3-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4aaa3-164">RELATED LINKS</span></span>
