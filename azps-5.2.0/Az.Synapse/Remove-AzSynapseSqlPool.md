---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cce6c35fa1186829760bab7c69d9e149cedfc015
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395907"
---
# <span data-ttu-id="51331-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="51331-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="51331-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51331-102">SYNOPSIS</span></span>
<span data-ttu-id="51331-103">Tar bort en Synapse Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="51331-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="51331-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51331-104">SYNTAX</span></span>

### <span data-ttu-id="51331-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51331-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51331-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51331-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51331-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51331-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51331-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51331-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51331-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51331-109">DESCRIPTION</span></span>
<span data-ttu-id="51331-110">Cmdleten **Remove-AzSynapseSqlPool** tar bort en Azure SYNAPSE Analytics SQL-pool permanent.</span><span class="sxs-lookup"><span data-stu-id="51331-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="51331-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51331-111">EXAMPLES</span></span>

### <span data-ttu-id="51331-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51331-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="51331-113">Det här kommandot tar bort en Azure Synapse-BA SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="51331-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="51331-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="51331-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="51331-115">Det här kommandot tar bort en Azure Synapse-BA-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="51331-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="51331-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="51331-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="51331-117">Det här kommandot tar bort en Azure Synapse-BA-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="51331-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="51331-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="51331-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="51331-119">Det här kommandot tar bort en Azure Synapse-BA-pool med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="51331-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="51331-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51331-120">PARAMETERS</span></span>

### <span data-ttu-id="51331-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51331-121">-AsJob</span></span>
<span data-ttu-id="51331-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="51331-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51331-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51331-123">-DefaultProfile</span></span>
<span data-ttu-id="51331-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51331-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51331-125">-Force</span><span class="sxs-lookup"><span data-stu-id="51331-125">-Force</span></span>
<span data-ttu-id="51331-126">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="51331-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="51331-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51331-127">-InputObject</span></span>
<span data-ttu-id="51331-128">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="51331-128">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="51331-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="51331-129">-Name</span></span>
<span data-ttu-id="51331-130">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="51331-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="51331-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51331-131">-PassThru</span></span>
<span data-ttu-id="51331-132">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="51331-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="51331-133">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="51331-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="51331-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51331-134">-ResourceGroupName</span></span>
<span data-ttu-id="51331-135">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="51331-135">Resource group name.</span></span>

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

### <span data-ttu-id="51331-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51331-136">-ResourceId</span></span>
<span data-ttu-id="51331-137">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="51331-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="51331-138">-Version</span><span class="sxs-lookup"><span data-stu-id="51331-138">-Version</span></span>
<span data-ttu-id="51331-139">Version av Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="51331-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="51331-140">Till exempel 2 eller 3.</span><span class="sxs-lookup"><span data-stu-id="51331-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="51331-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="51331-141">-WorkspaceName</span></span>
<span data-ttu-id="51331-142">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="51331-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="51331-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="51331-143">-WorkspaceObject</span></span>
<span data-ttu-id="51331-144">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="51331-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="51331-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51331-145">-Confirm</span></span>
<span data-ttu-id="51331-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51331-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51331-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51331-147">-WhatIf</span></span>
<span data-ttu-id="51331-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51331-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51331-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51331-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51331-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51331-150">CommonParameters</span></span>
<span data-ttu-id="51331-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51331-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51331-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51331-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51331-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51331-153">INPUTS</span></span>

### <span data-ttu-id="51331-154">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="51331-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="51331-155">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="51331-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="51331-156">System. String</span><span class="sxs-lookup"><span data-stu-id="51331-156">System.String</span></span>

## <span data-ttu-id="51331-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51331-157">OUTPUTS</span></span>

### <span data-ttu-id="51331-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51331-158">System.Boolean</span></span>

## <span data-ttu-id="51331-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51331-159">NOTES</span></span>

## <span data-ttu-id="51331-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51331-160">RELATED LINKS</span></span>
