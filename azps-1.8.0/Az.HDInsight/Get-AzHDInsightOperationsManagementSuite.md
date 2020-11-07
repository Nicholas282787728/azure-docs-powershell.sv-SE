---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fa19e7817d9d9be5e0c941db6d814500bad33509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916633"
---
# <span data-ttu-id="a31d6-101">Get-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="a31d6-101">Get-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="a31d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a31d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a31d6-103">Hämtar statusen för Operations Management Suite (OMS) i klustret.</span><span class="sxs-lookup"><span data-stu-id="a31d6-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

## <span data-ttu-id="a31d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a31d6-104">SYNTAX</span></span>

```
Get-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a31d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a31d6-105">DESCRIPTION</span></span>
<span data-ttu-id="a31d6-106">Cmdleten **Get-AzHDInsightOperationsManagementSuite** får statusen OMS-installation i ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="a31d6-106">The **Get-AzHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="a31d6-107">Om OMS är aktiverat returneras också ID för OMS-arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="a31d6-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="a31d6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a31d6-108">EXAMPLES</span></span>

### <span data-ttu-id="a31d6-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a31d6-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="a31d6-110">Operations Management Suite (OMS) är aktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är true.</span><span class="sxs-lookup"><span data-stu-id="a31d6-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="a31d6-111">ID för OMS-arbetsytan där loggarna flödar är 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="a31d6-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="a31d6-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a31d6-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="a31d6-113">Operations Management Suite (OMS) är aktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är true.</span><span class="sxs-lookup"><span data-stu-id="a31d6-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="a31d6-114">ID för OMS-arbetsytan där loggarna flödar är 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="a31d6-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="a31d6-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a31d6-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="a31d6-116">Operations Management Suite (OMS) är inaktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är falsk.</span><span class="sxs-lookup"><span data-stu-id="a31d6-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="a31d6-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="a31d6-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="a31d6-118">Operations Management Suite (OMS) är inaktiverat på klustret eftersom egenskapen ClusterMonitoringEnabled är falsk.</span><span class="sxs-lookup"><span data-stu-id="a31d6-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="a31d6-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a31d6-119">PARAMETERS</span></span>

### <span data-ttu-id="a31d6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31d6-120">-DefaultProfile</span></span>
<span data-ttu-id="a31d6-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a31d6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a31d6-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="a31d6-122">-Name</span></span>
<span data-ttu-id="a31d6-123">Namnet på klustret för att få statusen för Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="a31d6-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a31d6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a31d6-124">-ResourceGroupName</span></span>
<span data-ttu-id="a31d6-125">Klustrets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a31d6-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="a31d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31d6-126">CommonParameters</span></span>
<span data-ttu-id="a31d6-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a31d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31d6-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31d6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31d6-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a31d6-129">INPUTS</span></span>

### <span data-ttu-id="a31d6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a31d6-130">System.String</span></span>

## <span data-ttu-id="a31d6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a31d6-131">OUTPUTS</span></span>

### <span data-ttu-id="a31d6-132">Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a31d6-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="a31d6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a31d6-133">NOTES</span></span>

## <span data-ttu-id="a31d6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a31d6-134">RELATED LINKS</span></span>
