---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396611"
---
# <span data-ttu-id="3b446-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="3b446-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="3b446-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b446-102">SYNOPSIS</span></span>
<span data-ttu-id="3b446-103">Hämtar status för övervakning av installationen i klustret.</span><span class="sxs-lookup"><span data-stu-id="3b446-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="3b446-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b446-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b446-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b446-105">DESCRIPTION</span></span>
<span data-ttu-id="3b446-106">Cmdleten **Get-AzHDInsightMonitoring** får övervaka installationen i ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="3b446-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="3b446-107">Om övervakning är aktiverat returneras också ID för logganalys-arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="3b446-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="3b446-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b446-108">EXAMPLES</span></span>

### <span data-ttu-id="3b446-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3b446-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="3b446-110">Övervakning är aktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är true.</span><span class="sxs-lookup"><span data-stu-id="3b446-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="3b446-111">ID för övervaknings arbets ytan där loggarna flödar är 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="3b446-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="3b446-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3b446-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="3b446-113">Övervakning är aktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är true.</span><span class="sxs-lookup"><span data-stu-id="3b446-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="3b446-114">ID för övervaknings arbets ytan där loggarna flödar är 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="3b446-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="3b446-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3b446-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="3b446-116">Övervakning är inaktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är falsk.</span><span class="sxs-lookup"><span data-stu-id="3b446-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="3b446-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="3b446-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="3b446-118">Övervakning är inaktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är falsk.</span><span class="sxs-lookup"><span data-stu-id="3b446-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="3b446-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b446-119">PARAMETERS</span></span>

### <span data-ttu-id="3b446-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b446-120">-DefaultProfile</span></span>
<span data-ttu-id="3b446-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3b446-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b446-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3b446-122">-Name</span></span>
<span data-ttu-id="3b446-123">Namnet på klustret för att få övervaka status.</span><span class="sxs-lookup"><span data-stu-id="3b446-123">The name of the cluster to get the status of monitoring.</span></span>

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

### <span data-ttu-id="3b446-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b446-124">-ResourceGroupName</span></span>
<span data-ttu-id="3b446-125">Klustrets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3b446-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="3b446-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b446-126">CommonParameters</span></span>
<span data-ttu-id="3b446-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b446-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b446-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b446-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b446-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b446-129">INPUTS</span></span>

### <span data-ttu-id="3b446-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3b446-130">System.String</span></span>

## <span data-ttu-id="3b446-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b446-131">OUTPUTS</span></span>

### <span data-ttu-id="3b446-132">Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="3b446-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="3b446-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b446-133">NOTES</span></span>

## <span data-ttu-id="3b446-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b446-134">RELATED LINKS</span></span>
