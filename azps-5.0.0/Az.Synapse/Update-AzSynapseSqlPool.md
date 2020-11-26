---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 79bd39616f33a50684827276c6af919990b269ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269545"
---
# <span data-ttu-id="4d26d-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4d26d-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="4d26d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d26d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d26d-103">Uppdaterar en Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="4d26d-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4d26d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d26d-104">SYNTAX</span></span>

### <span data-ttu-id="4d26d-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4d26d-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d26d-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d26d-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d26d-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d26d-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d26d-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d26d-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d26d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d26d-109">DESCRIPTION</span></span>
<span data-ttu-id="4d26d-110">Cmdleten **Update-AzSynapseSqlPool** uppdaterar en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="4d26d-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4d26d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d26d-111">EXAMPLES</span></span>

### <span data-ttu-id="4d26d-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d26d-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="4d26d-113">Det här kommandot uppdaterar en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="4d26d-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="4d26d-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4d26d-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="4d26d-115">Det här kommandot uppdaterar en Azure Synapse-SQL-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d26d-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="4d26d-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="4d26d-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="4d26d-117">Det här kommandot uppdaterar en Azure Synapse-SQL-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d26d-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="4d26d-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="4d26d-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="4d26d-119">Det här kommandot uppdaterar en Azure Synapse SQL-pool med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4d26d-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="4d26d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d26d-120">PARAMETERS</span></span>

### <span data-ttu-id="4d26d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d26d-121">-AsJob</span></span>
<span data-ttu-id="4d26d-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4d26d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d26d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d26d-123">-DefaultProfile</span></span>
<span data-ttu-id="4d26d-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d26d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d26d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d26d-125">-InputObject</span></span>
<span data-ttu-id="4d26d-126">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d26d-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d26d-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d26d-127">-Name</span></span>
<span data-ttu-id="4d26d-128">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="4d26d-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d26d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d26d-129">-PassThru</span></span>
<span data-ttu-id="4d26d-130">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="4d26d-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="4d26d-131">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="4d26d-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4d26d-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="4d26d-132">-PerformanceLevel</span></span>
<span data-ttu-id="4d26d-133">SQL Service Tier och prestanda nivå som ska kopplas till SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="4d26d-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="4d26d-134">Till exempel DW2000c.</span><span class="sxs-lookup"><span data-stu-id="4d26d-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="4d26d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d26d-135">-ResourceGroupName</span></span>
<span data-ttu-id="4d26d-136">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4d26d-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d26d-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d26d-137">-ResourceId</span></span>
<span data-ttu-id="4d26d-138">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="4d26d-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d26d-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4d26d-139">-Tag</span></span>
<span data-ttu-id="4d26d-140">En sträng, en sträng ord lista med flaggor associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="4d26d-140">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d26d-141">-Version</span><span class="sxs-lookup"><span data-stu-id="4d26d-141">-Version</span></span>
<span data-ttu-id="4d26d-142">Version av Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="4d26d-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="4d26d-143">Till exempel 2 eller 3.</span><span class="sxs-lookup"><span data-stu-id="4d26d-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="4d26d-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d26d-144">-WorkspaceName</span></span>
<span data-ttu-id="4d26d-145">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="4d26d-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d26d-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4d26d-146">-WorkspaceObject</span></span>
<span data-ttu-id="4d26d-147">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d26d-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d26d-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d26d-148">-Confirm</span></span>
<span data-ttu-id="4d26d-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d26d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d26d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d26d-150">-WhatIf</span></span>
<span data-ttu-id="4d26d-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d26d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d26d-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d26d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d26d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d26d-153">CommonParameters</span></span>
<span data-ttu-id="4d26d-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d26d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d26d-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d26d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d26d-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d26d-156">INPUTS</span></span>

### <span data-ttu-id="4d26d-157">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d26d-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4d26d-158">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4d26d-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4d26d-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d26d-159">OUTPUTS</span></span>

### <span data-ttu-id="4d26d-160">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4d26d-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4d26d-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d26d-161">NOTES</span></span>

## <span data-ttu-id="4d26d-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d26d-162">RELATED LINKS</span></span>