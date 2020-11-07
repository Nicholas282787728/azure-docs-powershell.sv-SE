---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 5b6d514fc41c909fdd48b6a13ba85ab5836a5668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920035"
---
# <span data-ttu-id="e1991-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e1991-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="e1991-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1991-102">SYNOPSIS</span></span>
<span data-ttu-id="e1991-103">Ändrar en definition för en princip uppsättning</span><span class="sxs-lookup"><span data-stu-id="e1991-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="e1991-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1991-104">SYNTAX</span></span>

### <span data-ttu-id="e1991-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e1991-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1991-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1991-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1991-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1991-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1991-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1991-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1991-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1991-109">DESCRIPTION</span></span>
<span data-ttu-id="e1991-110">Cmdleten **set-AzPolicySetDefinition** ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="e1991-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="e1991-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1991-111">EXAMPLES</span></span>

### <span data-ttu-id="e1991-112">Exempel 1: Uppdatera beskrivningen av en definition för princip uppsättning</span><span class="sxs-lookup"><span data-stu-id="e1991-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="e1991-113">Det första kommandot får en princip uppsättnings definition med hjälp av Get-AzPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1991-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="e1991-114">Kommandot lagrar objektet i $PolicySetDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="e1991-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="e1991-115">Det andra kommandot uppdaterar beskrivningen av den definition av princip uppsättning som identifieras av egenskapen **ResourceID** för $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="e1991-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="e1991-116">Exempel 2: uppdatera metadata för en princip uppsättnings definition</span><span class="sxs-lookup"><span data-stu-id="e1991-116">Example 2: Update the metadata of a policy set definition</span></span>
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

<span data-ttu-id="e1991-117">Det här kommandot uppdaterar metadata för en princip uppsättnings definition med namnet VMPolicySetDefinition för att visa att kategorin är "virtuell dator".</span><span class="sxs-lookup"><span data-stu-id="e1991-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="e1991-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1991-118">PARAMETERS</span></span>

### <span data-ttu-id="e1991-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e1991-119">-ApiVersion</span></span>
<span data-ttu-id="e1991-120">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e1991-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e1991-121">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="e1991-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e1991-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1991-122">-DefaultProfile</span></span>
<span data-ttu-id="e1991-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e1991-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1991-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="e1991-124">-Description</span></span>
<span data-ttu-id="e1991-125">Beskrivningen för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="e1991-125">The description for policy set definition.</span></span>

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

### <span data-ttu-id="e1991-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e1991-126">-DisplayName</span></span>
<span data-ttu-id="e1991-127">Visnings namnet för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="e1991-127">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="e1991-128">-ID</span><span class="sxs-lookup"><span data-stu-id="e1991-128">-Id</span></span>
<span data-ttu-id="e1991-129">Fullständigt kvalificerat ID för principer, inklusive abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e1991-129">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="e1991-130">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="e1991-130">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="e1991-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e1991-131">-ManagementGroupName</span></span>
<span data-ttu-id="e1991-132">Namnet på hanterings gruppen för princip uppsättnings definitionen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="e1991-132">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="e1991-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e1991-133">-Metadata</span></span>
<span data-ttu-id="e1991-134">Metadata för den uppdaterade definitionen för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="e1991-134">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="e1991-135">Det kan vara en sökväg till ett fil namn som innehåller metadata, eller metadata som en sträng.</span><span class="sxs-lookup"><span data-stu-id="e1991-135">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="e1991-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1991-136">-Name</span></span>
<span data-ttu-id="e1991-137">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="e1991-137">The policy set definition name.</span></span>

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

### <span data-ttu-id="e1991-138">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e1991-138">-Parameter</span></span>
<span data-ttu-id="e1991-139">Parameter deklarationen för den uppdaterade definitionen för princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="e1991-139">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="e1991-140">Det kan antingen vara en sökväg till ett fil namn eller en URI som innehåller parameter deklarationen eller parameter deklarationen som en sträng.</span><span class="sxs-lookup"><span data-stu-id="e1991-140">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="e1991-141">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e1991-141">-PolicyDefinition</span></span>
<span data-ttu-id="e1991-142">Princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="e1991-142">The policy definitions.</span></span> <span data-ttu-id="e1991-143">Det kan vara en sökväg till ett fil namn som innehåller princip definitionerna eller princip definitionerna som sträng.</span><span class="sxs-lookup"><span data-stu-id="e1991-143">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

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

### <span data-ttu-id="e1991-144">-För</span><span class="sxs-lookup"><span data-stu-id="e1991-144">-Pre</span></span>
<span data-ttu-id="e1991-145">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e1991-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e1991-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1991-146">-SubscriptionId</span></span>
<span data-ttu-id="e1991-147">Prenumerations-ID för princip uppsättnings definitionen att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="e1991-147">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="e1991-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1991-148">-Confirm</span></span>
<span data-ttu-id="e1991-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1991-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1991-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1991-150">-WhatIf</span></span>
<span data-ttu-id="e1991-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1991-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1991-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1991-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1991-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1991-153">CommonParameters</span></span>
<span data-ttu-id="e1991-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1991-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1991-155">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1991-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1991-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1991-156">INPUTS</span></span>

### <span data-ttu-id="e1991-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e1991-157">System.String</span></span>

### <span data-ttu-id="e1991-158">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e1991-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e1991-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1991-159">OUTPUTS</span></span>

### <span data-ttu-id="e1991-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e1991-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e1991-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1991-161">NOTES</span></span>

## <span data-ttu-id="e1991-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1991-162">RELATED LINKS</span></span>
