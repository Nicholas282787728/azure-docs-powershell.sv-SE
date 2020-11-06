---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: 1fb2ee80a6dafb005509265e6012380eebf5abd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577009"
---
# <span data-ttu-id="7991f-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7991f-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="7991f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7991f-102">SYNOPSIS</span></span>
<span data-ttu-id="7991f-103">Hämtar listan med jobb från ett kluster och visar dem i omvänd kronologisk ordning, eller hämtar ett specifikt jobb.</span><span class="sxs-lookup"><span data-stu-id="7991f-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7991f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7991f-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7991f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7991f-105">DESCRIPTION</span></span>
<span data-ttu-id="7991f-106">Cmdleten **Get-AzureRmHDInsightJob** hämtar de senaste jobben för ett angivet Azure HDInsight-kluster i omvänd kronologisk ordning, med det senaste jobbet högst upp i listan.</span><span class="sxs-lookup"><span data-stu-id="7991f-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="7991f-107">Hämta ett specifikt jobb genom att ange parametern *jobId* .</span><span class="sxs-lookup"><span data-stu-id="7991f-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="7991f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7991f-108">EXAMPLES</span></span>

### <span data-ttu-id="7991f-109">Exempel 1: Hämta senaste jobb för ett angivet Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="7991f-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="7991f-110">Det här kommandot hämtar alla senaste jobb för det kluster som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="7991f-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="7991f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7991f-111">PARAMETERS</span></span>

### <span data-ttu-id="7991f-112">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="7991f-112">-ClusterName</span></span>
<span data-ttu-id="7991f-113">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="7991f-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7991f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7991f-114">-DefaultProfile</span></span>
<span data-ttu-id="7991f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7991f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7991f-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="7991f-116">-HttpCredential</span></span>
<span data-ttu-id="7991f-117">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="7991f-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7991f-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="7991f-118">-JobId</span></span>
<span data-ttu-id="7991f-119">Anger jobb-ID för jobbet som ska visas.</span><span class="sxs-lookup"><span data-stu-id="7991f-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7991f-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="7991f-120">-NumOfJobs</span></span>
<span data-ttu-id="7991f-121">Anger hur många jobb som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="7991f-121">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="7991f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7991f-122">-ResourceGroupName</span></span>
<span data-ttu-id="7991f-123">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7991f-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7991f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7991f-124">CommonParameters</span></span>
<span data-ttu-id="7991f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7991f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7991f-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7991f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7991f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7991f-127">INPUTS</span></span>

### <span data-ttu-id="7991f-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="7991f-128">None</span></span>

## <span data-ttu-id="7991f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7991f-129">OUTPUTS</span></span>

### <span data-ttu-id="7991f-130">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7991f-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="7991f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7991f-131">NOTES</span></span>

## <span data-ttu-id="7991f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7991f-132">RELATED LINKS</span></span>

[<span data-ttu-id="7991f-133">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7991f-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="7991f-134">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7991f-134">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="7991f-135">Stopp-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7991f-135">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="7991f-136">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7991f-136">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


