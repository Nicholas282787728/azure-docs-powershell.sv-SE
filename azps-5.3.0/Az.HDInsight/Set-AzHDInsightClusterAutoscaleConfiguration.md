---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bb22bda0f22ae128942e6e1d5a7aed9b0b646875
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522627"
---
# <span data-ttu-id="873b8-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="873b8-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="873b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="873b8-102">SYNOPSIS</span></span>
<span data-ttu-id="873b8-103">Ställer in automatisk skalnings konfiguration för ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="873b8-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="873b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="873b8-104">SYNTAX</span></span>

### <span data-ttu-id="873b8-105">LoadAutoscaleByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="873b8-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="873b8-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="873b8-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="873b8-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="873b8-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="873b8-108">LoadAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="873b8-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="873b8-109">ScheduleAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="873b8-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="873b8-110">AutoscaleConfigurationByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="873b8-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="873b8-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="873b8-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="873b8-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="873b8-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="873b8-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="873b8-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="873b8-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="873b8-114">DESCRIPTION</span></span>
<span data-ttu-id="873b8-115">Med den här cmdleten **set-AzHDInsightClusterAutoscaleConfiguration** anges den autoskalningsinställning som konfigurationen för ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="873b8-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="873b8-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="873b8-116">EXAMPLES</span></span>

### <span data-ttu-id="873b8-117">Exempel 1: Ange den inställda autoskalans konfiguration för HDInsight-klustret</span><span class="sxs-lookup"><span data-stu-id="873b8-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="873b8-118">Det här kommandot anger den belastningsutjämnade konfigurationen för automatisk skalning för ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="873b8-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="873b8-119">Exempel 2: Ange den tidsplanerade autoskalan för HDInsight-klustret</span><span class="sxs-lookup"><span data-stu-id="873b8-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="873b8-120">Det här kommandot anger den tidsplanerade autoskalans konfiguration för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="873b8-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="873b8-121">Exempel 3: Ange autoskalans konfiguration för HDInsight-klustret baserat på ett annat kluster som har angett Autoskala-konfiguration</span><span class="sxs-lookup"><span data-stu-id="873b8-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
```powershell
# Get the autoscale configuration of another cluster.
PS C:\> $clusterResourceGroup="group"
PS C:\> $anotherClusterName="anotherClusterName"
PS C:\> $autoscaleConfig=Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $anotherClusterName

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName `
            -Autoscale $autoscaleConfig
```

<span data-ttu-id="873b8-122">Det här kommandot ställer in automatisk skalnings konfiguration för HDInsight-klustret baserat på ett annat kluster.</span><span class="sxs-lookup"><span data-stu-id="873b8-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="873b8-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="873b8-123">PARAMETERS</span></span>

### <span data-ttu-id="873b8-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="873b8-124">-AsJob</span></span>
<span data-ttu-id="873b8-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="873b8-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="873b8-126">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="873b8-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="873b8-127">Hämtar eller anger den autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="873b8-127">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: AutoscaleConfigurationByNameParameterSet, AutoscaleConfigurationByResourceIdParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-128">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="873b8-128">-ClusterName</span></span>
<span data-ttu-id="873b8-129">Hämtar eller anger klustrets namn.</span><span class="sxs-lookup"><span data-stu-id="873b8-129">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-130">-Villkor</span><span class="sxs-lookup"><span data-stu-id="873b8-130">-Condition</span></span>
<span data-ttu-id="873b8-131">Hämtar eller anger villkoret för den schemalagda autoskalan.</span><span class="sxs-lookup"><span data-stu-id="873b8-131">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="873b8-132">-DefaultProfile</span></span>
<span data-ttu-id="873b8-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="873b8-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="873b8-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="873b8-134">-InputObject</span></span>
<span data-ttu-id="873b8-135">Hämtar eller anger indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="873b8-135">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: LoadAutoscaleByInputObjectParameterSet, ScheduleAutoscaleByInputObjectParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="873b8-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="873b8-137">Hämtar eller anger det maximala antalet belastningsutjämnade Autoskala för workernode.</span><span class="sxs-lookup"><span data-stu-id="873b8-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="873b8-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="873b8-139">Hämtar eller anger det minsta antalet belastningsutjämnade workernode.</span><span class="sxs-lookup"><span data-stu-id="873b8-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="873b8-140">-ResourceGroupName</span></span>
<span data-ttu-id="873b8-141">Hämtar eller anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="873b8-141">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="873b8-142">-ResourceId</span></span>
<span data-ttu-id="873b8-143">Hämtar eller anger resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="873b8-143">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByResourceIdParameterSet, AutoscaleConfigurationByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-144">– Schema</span><span class="sxs-lookup"><span data-stu-id="873b8-144">-Schedule</span></span>
<span data-ttu-id="873b8-145">Ange schemabaserade parametrar</span><span class="sxs-lookup"><span data-stu-id="873b8-145">Set schedule-based parameters</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="873b8-146">-TimeZone</span></span>
<span data-ttu-id="873b8-147">Hämtar eller anger tids zonen för den schemalagda autoskalan.</span><span class="sxs-lookup"><span data-stu-id="873b8-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="873b8-148">-Confirm</span></span>
<span data-ttu-id="873b8-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="873b8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="873b8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="873b8-150">-WhatIf</span></span>
<span data-ttu-id="873b8-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="873b8-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="873b8-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="873b8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="873b8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="873b8-153">CommonParameters</span></span>
<span data-ttu-id="873b8-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="873b8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="873b8-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="873b8-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="873b8-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="873b8-156">INPUTS</span></span>

### <span data-ttu-id="873b8-157">System. String</span><span class="sxs-lookup"><span data-stu-id="873b8-157">System.String</span></span>

### <span data-ttu-id="873b8-158">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="873b8-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="873b8-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="873b8-159">OUTPUTS</span></span>

### <span data-ttu-id="873b8-160">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="873b8-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="873b8-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="873b8-161">NOTES</span></span>

## <span data-ttu-id="873b8-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="873b8-162">RELATED LINKS</span></span>

<span data-ttu-id="873b8-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="873b8-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
