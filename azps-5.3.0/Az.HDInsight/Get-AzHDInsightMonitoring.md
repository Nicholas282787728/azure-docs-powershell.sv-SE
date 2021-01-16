---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523598"
---
# <span data-ttu-id="688ff-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="688ff-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="688ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="688ff-102">SYNOPSIS</span></span>
<span data-ttu-id="688ff-103">Hämtar status för övervakning av installationen i klustret.</span><span class="sxs-lookup"><span data-stu-id="688ff-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="688ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="688ff-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="688ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="688ff-105">DESCRIPTION</span></span>
<span data-ttu-id="688ff-106">Cmdleten **Get-AzHDInsightMonitoring** får övervaka installationen i ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="688ff-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="688ff-107">Om övervakning är aktiverat returneras också ID för logganalys-arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="688ff-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="688ff-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="688ff-108">EXAMPLES</span></span>

### <span data-ttu-id="688ff-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="688ff-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="688ff-110">Övervakning är aktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är true.</span><span class="sxs-lookup"><span data-stu-id="688ff-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="688ff-111">ID för övervaknings arbets ytan där loggarna flödar är 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="688ff-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="688ff-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="688ff-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="688ff-113">Övervakning är aktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är true.</span><span class="sxs-lookup"><span data-stu-id="688ff-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="688ff-114">ID för övervaknings arbets ytan där loggarna flödar är 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="688ff-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="688ff-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="688ff-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="688ff-116">Övervakning är inaktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är falsk.</span><span class="sxs-lookup"><span data-stu-id="688ff-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="688ff-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="688ff-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="688ff-118">Övervakning är inaktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är falsk.</span><span class="sxs-lookup"><span data-stu-id="688ff-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="688ff-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="688ff-119">PARAMETERS</span></span>

### <span data-ttu-id="688ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="688ff-120">-DefaultProfile</span></span>
<span data-ttu-id="688ff-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="688ff-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="688ff-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="688ff-122">-Name</span></span>
<span data-ttu-id="688ff-123">Namnet på klustret för att få övervaka status.</span><span class="sxs-lookup"><span data-stu-id="688ff-123">The name of the cluster to get the status of monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="688ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="688ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="688ff-125">Klustrets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="688ff-125">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="688ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="688ff-126">CommonParameters</span></span>
<span data-ttu-id="688ff-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="688ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="688ff-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="688ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="688ff-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="688ff-129">INPUTS</span></span>

### <span data-ttu-id="688ff-130">System. String</span><span class="sxs-lookup"><span data-stu-id="688ff-130">System.String</span></span>

## <span data-ttu-id="688ff-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="688ff-131">OUTPUTS</span></span>

### <span data-ttu-id="688ff-132">Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="688ff-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="688ff-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="688ff-133">NOTES</span></span>

## <span data-ttu-id="688ff-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="688ff-134">RELATED LINKS</span></span>
