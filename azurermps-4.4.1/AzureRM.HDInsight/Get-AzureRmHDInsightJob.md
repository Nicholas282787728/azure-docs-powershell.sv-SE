---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: e3cfd7978ecd7f8395a0c499d3d194f133960a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756345"
---
# <span data-ttu-id="5f45d-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5f45d-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="5f45d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f45d-102">SYNOPSIS</span></span>
<span data-ttu-id="5f45d-103">Hämtar listan med jobb från ett kluster och visar dem i omvänd kronologisk ordning, eller hämtar ett specifikt jobb.</span><span class="sxs-lookup"><span data-stu-id="5f45d-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f45d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f45d-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f45d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f45d-105">DESCRIPTION</span></span>
<span data-ttu-id="5f45d-106">Cmdleten **Get-AzureRmHDInsightJob** hämtar de senaste jobben för ett angivet Azure HDInsight-kluster i omvänd kronologisk ordning, med det senaste jobbet högst upp i listan.</span><span class="sxs-lookup"><span data-stu-id="5f45d-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="5f45d-107">Hämta ett specifikt jobb genom att ange parametern *jobId* .</span><span class="sxs-lookup"><span data-stu-id="5f45d-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="5f45d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f45d-108">EXAMPLES</span></span>

### <span data-ttu-id="5f45d-109">Exempel 1: Hämta senaste jobb för ett angivet Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="5f45d-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
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

<span data-ttu-id="5f45d-110">Det här kommandot hämtar alla senaste jobb för det kluster som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="5f45d-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="5f45d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f45d-111">PARAMETERS</span></span>

### <span data-ttu-id="5f45d-112">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="5f45d-112">-ClusterName</span></span>
<span data-ttu-id="5f45d-113">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="5f45d-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5f45d-114">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="5f45d-114">-HttpCredential</span></span>
<span data-ttu-id="5f45d-115">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="5f45d-115">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="5f45d-116">-JobId</span><span class="sxs-lookup"><span data-stu-id="5f45d-116">-JobId</span></span>
<span data-ttu-id="5f45d-117">Anger jobb-ID för jobbet som ska visas.</span><span class="sxs-lookup"><span data-stu-id="5f45d-117">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="5f45d-118">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="5f45d-118">-NumOfJobs</span></span>
<span data-ttu-id="5f45d-119">Anger hur många jobb som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="5f45d-119">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="5f45d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f45d-120">-ResourceGroupName</span></span>
<span data-ttu-id="5f45d-121">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5f45d-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5f45d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f45d-122">-DefaultProfile</span></span>
<span data-ttu-id="5f45d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f45d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f45d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f45d-124">CommonParameters</span></span>
<span data-ttu-id="5f45d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f45d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f45d-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f45d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f45d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f45d-127">INPUTS</span></span>

## <span data-ttu-id="5f45d-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f45d-128">OUTPUTS</span></span>

### <span data-ttu-id="5f45d-129">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5f45d-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="5f45d-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f45d-130">NOTES</span></span>

## <span data-ttu-id="5f45d-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f45d-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f45d-132">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5f45d-132">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="5f45d-133">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5f45d-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="5f45d-134">Stopp-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5f45d-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="5f45d-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5f45d-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


