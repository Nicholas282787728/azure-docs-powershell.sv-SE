---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523041"
---
# <span data-ttu-id="1523b-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1523b-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="1523b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1523b-102">SYNOPSIS</span></span>
<span data-ttu-id="1523b-103">Tar bort en uppsättning definitioner för principer.</span><span class="sxs-lookup"><span data-stu-id="1523b-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="1523b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1523b-104">SYNTAX</span></span>

### <span data-ttu-id="1523b-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1523b-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1523b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1523b-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1523b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1523b-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1523b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1523b-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1523b-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1523b-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1523b-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1523b-110">DESCRIPTION</span></span>
<span data-ttu-id="1523b-111">Cmdleten **Remove-AzPolicySetDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="1523b-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="1523b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1523b-112">EXAMPLES</span></span>

### <span data-ttu-id="1523b-113">Exempel 1: ta bort princip uppsättnings definition efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="1523b-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="1523b-114">Det första kommandot får en princip uppsättnings definition med hjälp av Get-AzPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1523b-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="1523b-115">Kommandot sparar det i $PolicySetDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="1523b-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="1523b-116">Det andra kommandot tar bort princip uppsättnings definitionen som identifieras av egenskapen **ResourceID** för $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="1523b-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="1523b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1523b-117">PARAMETERS</span></span>

### <span data-ttu-id="1523b-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1523b-118">-ApiVersion</span></span>
<span data-ttu-id="1523b-119">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1523b-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1523b-120">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="1523b-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1523b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1523b-121">-DefaultProfile</span></span>
<span data-ttu-id="1523b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1523b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1523b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1523b-123">-Force</span></span>
<span data-ttu-id="1523b-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1523b-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1523b-125">-ID</span><span class="sxs-lookup"><span data-stu-id="1523b-125">-Id</span></span>
<span data-ttu-id="1523b-126">Det fullständiga kvalificerade princip uppsättningens Definitions-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1523b-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="1523b-127">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1523b-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="1523b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1523b-128">-InputObject</span></span>
<span data-ttu-id="1523b-129">Den princip uppsättningens definitions objekt som ska tas bort från en annan cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1523b-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1523b-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1523b-130">-ManagementGroupName</span></span>
<span data-ttu-id="1523b-131">Namnet på hanterings gruppen för princip uppsättnings definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1523b-131">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="1523b-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="1523b-132">-Name</span></span>
<span data-ttu-id="1523b-133">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="1523b-133">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1523b-134">-För</span><span class="sxs-lookup"><span data-stu-id="1523b-134">-Pre</span></span>
<span data-ttu-id="1523b-135">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1523b-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1523b-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1523b-136">-SubscriptionId</span></span>
<span data-ttu-id="1523b-137">Abonnemangs-ID för princip uppsättnings definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1523b-137">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="1523b-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1523b-138">-Confirm</span></span>
<span data-ttu-id="1523b-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1523b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1523b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1523b-140">-WhatIf</span></span>
<span data-ttu-id="1523b-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1523b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1523b-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1523b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1523b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1523b-143">CommonParameters</span></span>
<span data-ttu-id="1523b-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1523b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1523b-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1523b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1523b-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1523b-146">INPUTS</span></span>

### <span data-ttu-id="1523b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1523b-147">System.String</span></span>

### <span data-ttu-id="1523b-148">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1523b-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1523b-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1523b-149">OUTPUTS</span></span>

### <span data-ttu-id="1523b-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1523b-150">System.Boolean</span></span>

## <span data-ttu-id="1523b-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1523b-151">NOTES</span></span>

## <span data-ttu-id="1523b-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1523b-152">RELATED LINKS</span></span>
