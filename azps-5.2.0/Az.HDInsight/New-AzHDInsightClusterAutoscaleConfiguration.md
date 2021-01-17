---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388029"
---
# <span data-ttu-id="1afec-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1afec-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="1afec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1afec-102">SYNOPSIS</span></span>
<span data-ttu-id="1afec-103">Skapar ett icke bevarat objekt som beskriver autoskalans konfiguration för ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="1afec-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1afec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1afec-104">SYNTAX</span></span>

### <span data-ttu-id="1afec-105">LoadAutoscaleParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1afec-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1afec-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="1afec-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1afec-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1afec-107">DESCRIPTION</span></span>
<span data-ttu-id="1afec-108">Med cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** skapas ett icke bevarat objekt som beskriver autoskalans konfiguration för ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="1afec-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1afec-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1afec-109">EXAMPLES</span></span>

### <span data-ttu-id="1afec-110">Exempel 1: skapa ett objekt som beskriver load-baserad Autoskala-konfiguration</span><span class="sxs-lookup"><span data-stu-id="1afec-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="1afec-111">Det här kommandot skapar ett objekt som beskriver load-baserad Autoskala-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1afec-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="1afec-112">Exempel 2: skapa ett objekt som beskriver schemaläggning baserad Autoskala-konfiguration</span><span class="sxs-lookup"><span data-stu-id="1afec-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="1afec-113">Det här kommandot skapar ett objekt som beskriver schemaläggning baserad Autoskala-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1afec-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="1afec-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1afec-114">PARAMETERS</span></span>

### <span data-ttu-id="1afec-115">-Villkor</span><span class="sxs-lookup"><span data-stu-id="1afec-115">-Condition</span></span>
<span data-ttu-id="1afec-116">Hämtar eller anger villkoret för den schemalagda autoskalan.</span><span class="sxs-lookup"><span data-stu-id="1afec-116">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afec-117">-DefaultProfile</span></span>
<span data-ttu-id="1afec-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1afec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1afec-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="1afec-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="1afec-120">Hämtar eller anger det maximala antalet belastningsutjämnade Autoskala för workernode.</span><span class="sxs-lookup"><span data-stu-id="1afec-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afec-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="1afec-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="1afec-122">Hämtar eller anger det minsta antalet belastningsutjämnade workernode.</span><span class="sxs-lookup"><span data-stu-id="1afec-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afec-123">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="1afec-123">-TimeZone</span></span>
<span data-ttu-id="1afec-124">Hämtar eller anger tids zonen för den schemalagda autoskalan.</span><span class="sxs-lookup"><span data-stu-id="1afec-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afec-125">CommonParameters</span></span>
<span data-ttu-id="1afec-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1afec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afec-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1afec-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afec-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1afec-128">INPUTS</span></span>

### <span data-ttu-id="1afec-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="1afec-129">None</span></span>

## <span data-ttu-id="1afec-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1afec-130">OUTPUTS</span></span>

### <span data-ttu-id="1afec-131">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="1afec-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="1afec-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1afec-132">NOTES</span></span>

## <span data-ttu-id="1afec-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1afec-133">RELATED LINKS</span></span>

<span data-ttu-id="1afec-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1afec-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
