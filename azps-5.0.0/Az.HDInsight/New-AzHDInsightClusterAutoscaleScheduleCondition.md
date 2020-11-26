---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263089"
---
# <span data-ttu-id="f1309-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="f1309-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="f1309-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1309-102">SYNOPSIS</span></span>
<span data-ttu-id="f1309-103">Skapar ett schema baserat autoskalning.</span><span class="sxs-lookup"><span data-stu-id="f1309-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="f1309-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1309-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1309-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1309-105">DESCRIPTION</span></span>
<span data-ttu-id="f1309-106">**New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet skapar ett schema baserat Autoskala-villkor.</span><span class="sxs-lookup"><span data-stu-id="f1309-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="f1309-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1309-107">EXAMPLES</span></span>

### <span data-ttu-id="f1309-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f1309-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="f1309-109">Det här kommandot skapar ett villkor där klustret ändrar automatiskt till 5 arbetsnoder på 09:00 varje måndag, onsdag.</span><span class="sxs-lookup"><span data-stu-id="f1309-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="f1309-110">Exempel 2: Aktivera schemaläggning-baserad Autoskala för ett kluster med autoskalning.</span><span class="sxs-lookup"><span data-stu-id="f1309-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="f1309-111">Det här kommandot skapar ett villkor där klustret ändrar automatiskt till 5 arbetsnoder på 09:00 varje måndag, onsdag.</span><span class="sxs-lookup"><span data-stu-id="f1309-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="f1309-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1309-112">PARAMETERS</span></span>

### <span data-ttu-id="f1309-113">-Dag</span><span class="sxs-lookup"><span data-stu-id="f1309-113">-Day</span></span>
<span data-ttu-id="f1309-114">Hämtar eller anger dagar för skalning med Autoskala.</span><span class="sxs-lookup"><span data-stu-id="f1309-114">Gets or sets the days of Autoscale schedule condition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightDaysOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1309-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1309-115">-DefaultProfile</span></span>
<span data-ttu-id="f1309-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f1309-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1309-117">-Tid</span><span class="sxs-lookup"><span data-stu-id="f1309-117">-Time</span></span>
<span data-ttu-id="f1309-118">Hämtar eller anger tiden för autoskalning av schema villkor.</span><span class="sxs-lookup"><span data-stu-id="f1309-118">Gets or sets the time of Autoscale schedule condition.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1309-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="f1309-119">-WorkerNodeCount</span></span>
<span data-ttu-id="f1309-120">Hämtar eller anger schemat workernode antalet Autoskala-schema.</span><span class="sxs-lookup"><span data-stu-id="f1309-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1309-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1309-121">CommonParameters</span></span>
<span data-ttu-id="f1309-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1309-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1309-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1309-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1309-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1309-124">INPUTS</span></span>

### <span data-ttu-id="f1309-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="f1309-125">None</span></span>

## <span data-ttu-id="f1309-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1309-126">OUTPUTS</span></span>

### <span data-ttu-id="f1309-127">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="f1309-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="f1309-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1309-128">NOTES</span></span>

## <span data-ttu-id="f1309-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1309-129">RELATED LINKS</span></span>

<span data-ttu-id="f1309-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f1309-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>