---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: d9e3160d5ba0620ff881c940bf8383a7046136a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103361"
---
# <span data-ttu-id="bf1f3-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="bf1f3-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="bf1f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1f3-103">Tar bort en Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="bf1f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf1f3-104">SYNTAX</span></span>

### <span data-ttu-id="bf1f3-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bf1f3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf1f3-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf1f3-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf1f3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf1f3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf1f3-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf1f3-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf1f3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf1f3-109">DESCRIPTION</span></span>
<span data-ttu-id="bf1f3-110">Cmdleten **Remove-AzSynapseSparkPool** tar bort en Azure Synapse Analytics Spark-pool permanent.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="bf1f3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf1f3-111">EXAMPLES</span></span>

### <span data-ttu-id="bf1f3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bf1f3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="bf1f3-113">Det här kommandot tar bort en Azure Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="bf1f3-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bf1f3-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="bf1f3-115">Det här kommandot tar bort en Azure Synapse Analytics Spark-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="bf1f3-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="bf1f3-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="bf1f3-117">Det här kommandot tar bort en Azure Synapse Analytics Spark-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="bf1f3-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="bf1f3-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="bf1f3-119">Det här kommandot tar bort en Azure Synapse Analytics Spark-pool med ett resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="bf1f3-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf1f3-120">PARAMETERS</span></span>

### <span data-ttu-id="bf1f3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf1f3-121">-AsJob</span></span>
<span data-ttu-id="bf1f3-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bf1f3-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf1f3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1f3-123">-DefaultProfile</span></span>
<span data-ttu-id="bf1f3-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf1f3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf1f3-125">-InputObject</span></span>
<span data-ttu-id="bf1f3-126">Indata från Spark-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-126">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf1f3-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="bf1f3-127">-Name</span></span>
<span data-ttu-id="bf1f3-128">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-128">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1f3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf1f3-129">-PassThru</span></span>
<span data-ttu-id="bf1f3-130">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="bf1f3-131">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bf1f3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf1f3-132">-ResourceGroupName</span></span>
<span data-ttu-id="bf1f3-133">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-133">Resource group name.</span></span>

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

### <span data-ttu-id="bf1f3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf1f3-134">-ResourceId</span></span>
<span data-ttu-id="bf1f3-135">Resurs-ID för Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-135">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1f3-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bf1f3-136">-WorkspaceName</span></span>
<span data-ttu-id="bf1f3-137">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bf1f3-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bf1f3-138">-WorkspaceObject</span></span>
<span data-ttu-id="bf1f3-139">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bf1f3-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf1f3-140">-Confirm</span></span>
<span data-ttu-id="bf1f3-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf1f3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf1f3-142">-WhatIf</span></span>
<span data-ttu-id="bf1f3-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf1f3-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf1f3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1f3-145">CommonParameters</span></span>
<span data-ttu-id="bf1f3-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf1f3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1f3-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf1f3-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1f3-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf1f3-148">INPUTS</span></span>

### <span data-ttu-id="bf1f3-149">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bf1f3-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bf1f3-150">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="bf1f3-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="bf1f3-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf1f3-151">OUTPUTS</span></span>

### <span data-ttu-id="bf1f3-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf1f3-152">System.Boolean</span></span>

## <span data-ttu-id="bf1f3-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf1f3-153">NOTES</span></span>

## <span data-ttu-id="bf1f3-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf1f3-154">RELATED LINKS</span></span>
