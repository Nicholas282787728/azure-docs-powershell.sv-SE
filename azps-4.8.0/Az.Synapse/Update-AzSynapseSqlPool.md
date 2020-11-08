---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 62b1e0ef03d52337c03506d3bddc8bbfd3d5512d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261183"
---
# <span data-ttu-id="ebfec-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ebfec-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="ebfec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ebfec-102">SYNOPSIS</span></span>
<span data-ttu-id="ebfec-103">Uppdaterar en Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="ebfec-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ebfec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ebfec-104">SYNTAX</span></span>

### <span data-ttu-id="ebfec-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ebfec-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebfec-106">PauseByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfec-106">PauseByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Suspend] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebfec-107">ResumeByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfec-107">ResumeByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Resume] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebfec-108">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfec-108">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebfec-109">PauseByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfec-109">PauseByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Suspend] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebfec-110">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfec-110">ResumeByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Resume] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebfec-111">PauseByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfec-111">PauseByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebfec-112">PauseByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfec-112">PauseByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebfec-113">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfec-113">ResumeByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebfec-114">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfec-114">ResumeByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebfec-115">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfec-115">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebfec-116">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfec-116">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebfec-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ebfec-117">DESCRIPTION</span></span>
<span data-ttu-id="ebfec-118">Cmdleten **Update-AzSynapseSqlPool** uppdaterar en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="ebfec-118">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ebfec-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ebfec-119">EXAMPLES</span></span>

### <span data-ttu-id="ebfec-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ebfec-120">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="ebfec-121">Det här kommandot uppdaterar en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="ebfec-121">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="ebfec-122">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ebfec-122">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="ebfec-123">Det här kommandot uppdaterar en Azure Synapse-SQL-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="ebfec-123">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="ebfec-124">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ebfec-124">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="ebfec-125">Det här kommandot uppdaterar en Azure Synapse-SQL-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="ebfec-125">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="ebfec-126">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="ebfec-126">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="ebfec-127">Det här kommandot uppdaterar en Azure Synapse SQL-pool med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ebfec-127">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="ebfec-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ebfec-128">PARAMETERS</span></span>

### <span data-ttu-id="ebfec-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebfec-129">-AsJob</span></span>
<span data-ttu-id="ebfec-130">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ebfec-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebfec-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebfec-131">-DefaultProfile</span></span>
<span data-ttu-id="ebfec-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ebfec-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebfec-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebfec-133">-InputObject</span></span>
<span data-ttu-id="ebfec-134">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="ebfec-134">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: PauseByInputObjectParameterSet, ResumeByInputObjectParameterSet, UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfec-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="ebfec-135">-Name</span></span>
<span data-ttu-id="ebfec-136">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="ebfec-136">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet, UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfec-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebfec-137">-PassThru</span></span>
<span data-ttu-id="ebfec-138">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="ebfec-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="ebfec-139">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="ebfec-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ebfec-140">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="ebfec-140">-PerformanceLevel</span></span>
<span data-ttu-id="ebfec-141">SQL Service Tier och prestanda nivå som ska kopplas till SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="ebfec-141">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="ebfec-142">Till exempel DW2000c.</span><span class="sxs-lookup"><span data-stu-id="ebfec-142">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfec-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebfec-143">-ResourceGroupName</span></span>
<span data-ttu-id="ebfec-144">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ebfec-144">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfec-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebfec-145">-ResourceId</span></span>
<span data-ttu-id="ebfec-146">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="ebfec-146">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: PauseByResourceIdParameterSet, ResumeByResourceIdParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfec-147">-Fortsätt</span><span class="sxs-lookup"><span data-stu-id="ebfec-147">-Resume</span></span>
<span data-ttu-id="ebfec-148">Anger att SQL-poolen ska återupptas</span><span class="sxs-lookup"><span data-stu-id="ebfec-148">Indicates to resume the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet, ResumeByInputObjectParameterSet, ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfec-149">-Pausa</span><span class="sxs-lookup"><span data-stu-id="ebfec-149">-Suspend</span></span>
<span data-ttu-id="ebfec-150">Anger att pausa SQL-poolen</span><span class="sxs-lookup"><span data-stu-id="ebfec-150">Indicates to pause the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PauseByNameParameterSet, PauseByParentObjectParameterSet, PauseByInputObjectParameterSet, PauseByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfec-151">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ebfec-151">-Tag</span></span>
<span data-ttu-id="ebfec-152">En sträng, en sträng ord lista med flaggor associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="ebfec-152">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfec-153">-Version</span><span class="sxs-lookup"><span data-stu-id="ebfec-153">-Version</span></span>
<span data-ttu-id="ebfec-154">Version av Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="ebfec-154">Version of Synapse SQL pool.</span></span> <span data-ttu-id="ebfec-155">Till exempel 2 eller 3.</span><span class="sxs-lookup"><span data-stu-id="ebfec-155">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfec-156">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ebfec-156">-WorkspaceName</span></span>
<span data-ttu-id="ebfec-157">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="ebfec-157">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfec-158">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ebfec-158">-WorkspaceObject</span></span>
<span data-ttu-id="ebfec-159">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="ebfec-159">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfec-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ebfec-160">-Confirm</span></span>
<span data-ttu-id="ebfec-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ebfec-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebfec-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebfec-162">-WhatIf</span></span>
<span data-ttu-id="ebfec-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ebfec-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebfec-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ebfec-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebfec-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebfec-165">CommonParameters</span></span>
<span data-ttu-id="ebfec-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebfec-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebfec-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebfec-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebfec-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ebfec-168">INPUTS</span></span>

### <span data-ttu-id="ebfec-169">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ebfec-169">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ebfec-170">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ebfec-170">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ebfec-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ebfec-171">OUTPUTS</span></span>

### <span data-ttu-id="ebfec-172">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ebfec-172">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ebfec-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ebfec-173">NOTES</span></span>

## <span data-ttu-id="ebfec-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ebfec-174">RELATED LINKS</span></span>
