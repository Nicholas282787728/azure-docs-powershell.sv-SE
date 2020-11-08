---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100687"
---
# <span data-ttu-id="51968-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="51968-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="51968-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51968-102">SYNOPSIS</span></span>
<span data-ttu-id="51968-103">Uppdaterar en Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="51968-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="51968-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51968-104">SYNTAX</span></span>

### <span data-ttu-id="51968-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51968-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51968-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51968-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51968-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51968-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51968-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51968-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51968-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51968-109">DESCRIPTION</span></span>
<span data-ttu-id="51968-110">Cmdleten **Update-AzSynapseSparkPool** uppdaterar en Azure Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="51968-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="51968-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51968-111">EXAMPLES</span></span>

### <span data-ttu-id="51968-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51968-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="51968-113">Det här kommandot uppdaterar en Azure Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="51968-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="51968-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="51968-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="51968-115">Det här kommandot uppdaterar en Azure Synapse Analytics Spark-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="51968-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="51968-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="51968-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="51968-117">Det här kommandot uppdaterar en Azure Synapse Analytics Spark-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="51968-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="51968-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="51968-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="51968-119">Det här kommandot uppdaterar en Azure Synapse Analytics Spark-pool med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="51968-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="51968-120">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="51968-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="51968-121">Det här kommandot aktiverar automatisk skalning för en Azure Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="51968-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="51968-122">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="51968-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="51968-123">Det här kommandot inaktiverar automatisk skalning för en Azure Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="51968-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="51968-124">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="51968-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="51968-125">Det här kommandot aktiverar automatisk paus för en Azure Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="51968-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="51968-126">Exempel 8</span><span class="sxs-lookup"><span data-stu-id="51968-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="51968-127">Det här kommandot inaktiverar automatisk paus för en Azure Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="51968-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="51968-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51968-128">PARAMETERS</span></span>

### <span data-ttu-id="51968-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51968-129">-AsJob</span></span>
<span data-ttu-id="51968-130">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="51968-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51968-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="51968-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="51968-132">Antal overksamma minuter.</span><span class="sxs-lookup"><span data-stu-id="51968-132">Number of minutes idle.</span></span> <span data-ttu-id="51968-133">Den här parametern måste anges när Auto-paus är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="51968-133">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="51968-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="51968-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="51968-135">Maximalt antal noder som ska tilldelas till den angivna Spark-poolen.</span><span class="sxs-lookup"><span data-stu-id="51968-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="51968-136">Den här parametern måste anges när Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="51968-136">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="51968-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="51968-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="51968-138">Det minsta antalet noder som ska tilldelas till den angivna Spark-poolen.</span><span class="sxs-lookup"><span data-stu-id="51968-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="51968-139">Den här parametern måste anges när Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="51968-139">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="51968-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51968-140">-DefaultProfile</span></span>
<span data-ttu-id="51968-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51968-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51968-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="51968-142">-EnableAutoPause</span></span>
<span data-ttu-id="51968-143">Anger om Auto-paus ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="51968-143">Indicates whether Auto-pause should be enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51968-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="51968-144">-EnableAutoScale</span></span>
<span data-ttu-id="51968-145">Anger om automatisk skalning ska aktive ras</span><span class="sxs-lookup"><span data-stu-id="51968-145">Indicates whether Auto-scale should be enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51968-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51968-146">-InputObject</span></span>
<span data-ttu-id="51968-147">Indata från Spark-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="51968-147">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51968-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="51968-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="51968-149">Konfigurations fil för miljön ("PIP Freeze"-utdata).</span><span class="sxs-lookup"><span data-stu-id="51968-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="51968-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="51968-150">-Name</span></span>
<span data-ttu-id="51968-151">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="51968-151">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51968-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="51968-152">-NodeCount</span></span>
<span data-ttu-id="51968-153">Antalet noder som ska tilldelas i den angivna Spark-poolen.</span><span class="sxs-lookup"><span data-stu-id="51968-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="51968-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="51968-154">-NodeSize</span></span>
<span data-ttu-id="51968-155">Antal kärnor och minne som ska användas för noder som tilldelats i den angivna Spark-poolen.</span><span class="sxs-lookup"><span data-stu-id="51968-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="51968-156">Den här parametern måste anges när Autoskala är inaktiverat</span><span class="sxs-lookup"><span data-stu-id="51968-156">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51968-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51968-157">-ResourceGroupName</span></span>
<span data-ttu-id="51968-158">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="51968-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51968-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51968-159">-ResourceId</span></span>
<span data-ttu-id="51968-160">Resurs-ID för Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="51968-160">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51968-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="51968-161">-SparkVersion</span></span>
<span data-ttu-id="51968-162">Apache Spark-version.</span><span class="sxs-lookup"><span data-stu-id="51968-162">Apache Spark version.</span></span>
<span data-ttu-id="51968-163">Tillåtna värden: 2,4</span><span class="sxs-lookup"><span data-stu-id="51968-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="51968-164">-Tagg</span><span class="sxs-lookup"><span data-stu-id="51968-164">-Tag</span></span>
<span data-ttu-id="51968-165">En sträng, en sträng ord lista med flaggor associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="51968-165">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="51968-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="51968-166">-WorkspaceName</span></span>
<span data-ttu-id="51968-167">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="51968-167">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51968-168">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="51968-168">-WorkspaceObject</span></span>
<span data-ttu-id="51968-169">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="51968-169">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51968-170">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51968-170">-Confirm</span></span>
<span data-ttu-id="51968-171">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51968-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51968-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51968-172">-WhatIf</span></span>
<span data-ttu-id="51968-173">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51968-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51968-174">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51968-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51968-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51968-175">CommonParameters</span></span>
<span data-ttu-id="51968-176">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51968-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51968-177">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51968-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51968-178">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51968-178">INPUTS</span></span>

### <span data-ttu-id="51968-179">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="51968-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="51968-180">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="51968-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="51968-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51968-181">OUTPUTS</span></span>

### <span data-ttu-id="51968-182">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="51968-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="51968-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51968-183">NOTES</span></span>

## <span data-ttu-id="51968-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51968-184">RELATED LINKS</span></span>
