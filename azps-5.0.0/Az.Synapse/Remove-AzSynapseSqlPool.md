---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cd715bed20477fae4cbb17d033fd67fefa4e1cdc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270367"
---
# <span data-ttu-id="67967-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="67967-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="67967-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67967-102">SYNOPSIS</span></span>
<span data-ttu-id="67967-103">Tar bort en Synapse Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="67967-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="67967-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67967-104">SYNTAX</span></span>

### <span data-ttu-id="67967-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="67967-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67967-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67967-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67967-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67967-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67967-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67967-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67967-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67967-109">DESCRIPTION</span></span>
<span data-ttu-id="67967-110">Cmdleten **Remove-AzSynapseSqlPool** tar bort en Azure SYNAPSE Analytics SQL-pool permanent.</span><span class="sxs-lookup"><span data-stu-id="67967-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="67967-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67967-111">EXAMPLES</span></span>

### <span data-ttu-id="67967-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="67967-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="67967-113">Det här kommandot tar bort en Azure Synapse-BA SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="67967-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="67967-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="67967-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="67967-115">Det här kommandot tar bort en Azure Synapse-BA-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="67967-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="67967-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="67967-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="67967-117">Det här kommandot tar bort en Azure Synapse-BA-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="67967-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="67967-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="67967-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="67967-119">Det här kommandot tar bort en Azure Synapse-BA-pool med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="67967-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="67967-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67967-120">PARAMETERS</span></span>

### <span data-ttu-id="67967-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67967-121">-AsJob</span></span>
<span data-ttu-id="67967-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="67967-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67967-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67967-123">-DefaultProfile</span></span>
<span data-ttu-id="67967-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67967-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67967-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67967-125">-InputObject</span></span>
<span data-ttu-id="67967-126">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="67967-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67967-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="67967-127">-Name</span></span>
<span data-ttu-id="67967-128">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="67967-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67967-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67967-129">-PassThru</span></span>
<span data-ttu-id="67967-130">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="67967-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="67967-131">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="67967-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="67967-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67967-132">-ResourceGroupName</span></span>
<span data-ttu-id="67967-133">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="67967-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67967-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67967-134">-ResourceId</span></span>
<span data-ttu-id="67967-135">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="67967-135">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67967-136">-Version</span><span class="sxs-lookup"><span data-stu-id="67967-136">-Version</span></span>
<span data-ttu-id="67967-137">Version av Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="67967-137">Version of Synapse SQL pool.</span></span> <span data-ttu-id="67967-138">Till exempel 2 eller 3.</span><span class="sxs-lookup"><span data-stu-id="67967-138">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="67967-139">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="67967-139">-WorkspaceName</span></span>
<span data-ttu-id="67967-140">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="67967-140">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67967-141">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="67967-141">-WorkspaceObject</span></span>
<span data-ttu-id="67967-142">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="67967-142">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67967-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="67967-143">-Confirm</span></span>
<span data-ttu-id="67967-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="67967-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67967-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67967-145">-WhatIf</span></span>
<span data-ttu-id="67967-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="67967-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67967-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="67967-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67967-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67967-148">CommonParameters</span></span>
<span data-ttu-id="67967-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67967-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67967-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67967-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67967-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67967-151">INPUTS</span></span>

### <span data-ttu-id="67967-152">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="67967-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="67967-153">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="67967-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="67967-154">System. String</span><span class="sxs-lookup"><span data-stu-id="67967-154">System.String</span></span>

## <span data-ttu-id="67967-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67967-155">OUTPUTS</span></span>

### <span data-ttu-id="67967-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67967-156">System.Boolean</span></span>

## <span data-ttu-id="67967-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67967-157">NOTES</span></span>

## <span data-ttu-id="67967-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67967-158">RELATED LINKS</span></span>
