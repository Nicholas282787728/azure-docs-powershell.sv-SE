---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 8a8559058b0bb5e1b33d93451bed35182a44783b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089460"
---
# <span data-ttu-id="dafaa-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="dafaa-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="dafaa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dafaa-102">SYNOPSIS</span></span>
<span data-ttu-id="dafaa-103">Ändrar en definition för en princip uppsättning</span><span class="sxs-lookup"><span data-stu-id="dafaa-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="dafaa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dafaa-104">SYNTAX</span></span>

### <span data-ttu-id="dafaa-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dafaa-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dafaa-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dafaa-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dafaa-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dafaa-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dafaa-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dafaa-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dafaa-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dafaa-109">DESCRIPTION</span></span>
<span data-ttu-id="dafaa-110">Cmdleten **set-AzPolicySetDefinition** ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="dafaa-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="dafaa-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dafaa-111">EXAMPLES</span></span>

### <span data-ttu-id="dafaa-112">Exempel 1: Uppdatera beskrivningen av en definition för princip uppsättning</span><span class="sxs-lookup"><span data-stu-id="dafaa-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="dafaa-113">Det första kommandot får en princip uppsättnings definition med hjälp av Get-AzPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dafaa-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="dafaa-114">Kommandot lagrar objektet i $PolicySetDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="dafaa-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="dafaa-115">Det andra kommandot uppdaterar beskrivningen av den definition av princip uppsättning som identifieras av egenskapen **ResourceID** för $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="dafaa-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="dafaa-116">Exempel 2: uppdatera metadata för en princip uppsättnings definition</span><span class="sxs-lookup"><span data-stu-id="dafaa-116">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="dafaa-117">Det här kommandot uppdaterar metadata för en princip uppsättnings definition med namnet VMPolicySetDefinition för att visa att kategorin är "virtuell dator".</span><span class="sxs-lookup"><span data-stu-id="dafaa-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="dafaa-118">Exempel 3: uppdatera grupperna i en definition för princip uppsättningar</span><span class="sxs-lookup"><span data-stu-id="dafaa-118">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="dafaa-119">Det här kommandot uppdaterar grupperna för en princip uppsättnings definition med namnet VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="dafaa-119">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="dafaa-120">Exempel 4: uppdatera gruppens grupper med hjälp av en hash-tabell</span><span class="sxs-lookup"><span data-stu-id="dafaa-120">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="dafaa-121">Det här kommandot uppdaterar grupperna för en princip uppsättnings definition med namnet VMPolicySetDefinition med hjälp av en hash-tabell för att skapa grupper.</span><span class="sxs-lookup"><span data-stu-id="dafaa-121">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="dafaa-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dafaa-122">PARAMETERS</span></span>

### <span data-ttu-id="dafaa-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dafaa-123">-ApiVersion</span></span>
<span data-ttu-id="dafaa-124">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="dafaa-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="dafaa-125">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="dafaa-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="dafaa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafaa-126">-DefaultProfile</span></span>
<span data-ttu-id="dafaa-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dafaa-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dafaa-128">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="dafaa-128">-Description</span></span>
<span data-ttu-id="dafaa-129">Beskrivningen för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="dafaa-129">The description for policy set definition.</span></span>

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

### <span data-ttu-id="dafaa-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dafaa-130">-DisplayName</span></span>
<span data-ttu-id="dafaa-131">Visnings namnet för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="dafaa-131">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="dafaa-132">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="dafaa-132">-GroupDefinition</span></span>
<span data-ttu-id="dafaa-133">Princip definitions grupperna för den uppdaterade definitionen för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="dafaa-133">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="dafaa-134">Det kan antingen vara en sökväg till en fil som innehåller grupperna eller grupperna som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="dafaa-134">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="dafaa-135">-ID</span><span class="sxs-lookup"><span data-stu-id="dafaa-135">-Id</span></span>
<span data-ttu-id="dafaa-136">Fullständigt kvalificerat ID för principer, inklusive abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="dafaa-136">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="dafaa-137">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="dafaa-137">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dafaa-138">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="dafaa-138">-ManagementGroupName</span></span>
<span data-ttu-id="dafaa-139">Namnet på hanterings gruppen för princip uppsättnings definitionen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="dafaa-139">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="dafaa-140">-Metadata</span><span class="sxs-lookup"><span data-stu-id="dafaa-140">-Metadata</span></span>
<span data-ttu-id="dafaa-141">Metadata för den uppdaterade definitionen för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="dafaa-141">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="dafaa-142">Det kan vara en sökväg till ett fil namn som innehåller metadata, eller metadata som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="dafaa-142">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="dafaa-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="dafaa-143">-Name</span></span>
<span data-ttu-id="dafaa-144">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="dafaa-144">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dafaa-145">-Parameter</span><span class="sxs-lookup"><span data-stu-id="dafaa-145">-Parameter</span></span>
<span data-ttu-id="dafaa-146">Parameter deklarationen för den uppdaterade definitionen för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="dafaa-146">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="dafaa-147">Det kan antingen vara en sökväg till ett fil namn eller en URI som innehåller parameter deklarationen eller parameter deklarationen som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="dafaa-147">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="dafaa-148">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dafaa-148">-PolicyDefinition</span></span>
<span data-ttu-id="dafaa-149">Princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="dafaa-149">The policy definitions.</span></span> <span data-ttu-id="dafaa-150">Det kan vara en sökväg till ett fil namn som innehåller princip definitionerna eller princip definitionerna som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="dafaa-150">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="dafaa-151">-För</span><span class="sxs-lookup"><span data-stu-id="dafaa-151">-Pre</span></span>
<span data-ttu-id="dafaa-152">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="dafaa-152">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="dafaa-153">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dafaa-153">-SubscriptionId</span></span>
<span data-ttu-id="dafaa-154">Prenumerations-ID för princip uppsättnings definitionen att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="dafaa-154">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="dafaa-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dafaa-155">-Confirm</span></span>
<span data-ttu-id="dafaa-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dafaa-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dafaa-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dafaa-157">-WhatIf</span></span>
<span data-ttu-id="dafaa-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dafaa-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dafaa-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dafaa-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dafaa-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafaa-160">CommonParameters</span></span>
<span data-ttu-id="dafaa-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dafaa-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafaa-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dafaa-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafaa-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dafaa-163">INPUTS</span></span>

### <span data-ttu-id="dafaa-164">System. String</span><span class="sxs-lookup"><span data-stu-id="dafaa-164">System.String</span></span>

### <span data-ttu-id="dafaa-165">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dafaa-165">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dafaa-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dafaa-166">OUTPUTS</span></span>

### <span data-ttu-id="dafaa-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="dafaa-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="dafaa-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dafaa-168">NOTES</span></span>

## <span data-ttu-id="dafaa-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dafaa-169">RELATED LINKS</span></span>
