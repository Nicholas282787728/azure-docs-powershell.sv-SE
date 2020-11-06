---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/start-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 8c3e0f01472469be856d69c1a87f8eb5185f2012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585151"
---
# <span data-ttu-id="5b24f-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5b24f-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="5b24f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5b24f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b24f-103">Startar ett definierat Azure HDInsight-jobb i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="5b24f-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b24f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5b24f-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b24f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5b24f-105">DESCRIPTION</span></span>
<span data-ttu-id="5b24f-106">Cmdleten **Start-AzureRMHDInsightJob** startar ett definierat Azure HDInsight-jobb i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="5b24f-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="5b24f-107">Detta kan vara ett MapReduce jobb, ett strömmande MapReduce jobb, ett registrerings jobb eller ett gris-jobb.</span><span class="sxs-lookup"><span data-stu-id="5b24f-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="5b24f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5b24f-108">EXAMPLES</span></span>

### <span data-ttu-id="5b24f-109">Exempel 1: starta ett jobb i angivet kluster</span><span class="sxs-lookup"><span data-stu-id="5b24f-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="5b24f-110">Det här kommandot startar ett jobb i klustret som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="5b24f-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="5b24f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5b24f-111">PARAMETERS</span></span>

### <span data-ttu-id="5b24f-112">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="5b24f-112">-ClusterName</span></span>
<span data-ttu-id="5b24f-113">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="5b24f-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b24f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b24f-114">-DefaultProfile</span></span>
<span data-ttu-id="5b24f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5b24f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b24f-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="5b24f-116">-HttpCredential</span></span>
<span data-ttu-id="5b24f-117">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="5b24f-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b24f-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="5b24f-118">-JobDefinition</span></span>
<span data-ttu-id="5b24f-119">Anger det jobb som ska startas i Azure HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="5b24f-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b24f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b24f-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b24f-121">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5b24f-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b24f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b24f-122">CommonParameters</span></span>
<span data-ttu-id="5b24f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b24f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b24f-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b24f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b24f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5b24f-125">INPUTS</span></span>

### <span data-ttu-id="5b24f-126">AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5b24f-126">AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="5b24f-127">Parametern ' JobDefinition ' godkänner värdet av typen ' AzureHDInsightJobDefinition ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5b24f-127">Parameter 'JobDefinition' accepts value of type 'AzureHDInsightJobDefinition' from the pipeline</span></span>

## <span data-ttu-id="5b24f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5b24f-128">OUTPUTS</span></span>

### <span data-ttu-id="5b24f-129">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5b24f-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="5b24f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5b24f-130">NOTES</span></span>

## <span data-ttu-id="5b24f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5b24f-131">RELATED LINKS</span></span>

[<span data-ttu-id="5b24f-132">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5b24f-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="5b24f-133">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5b24f-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="5b24f-134">Stopp-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5b24f-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="5b24f-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5b24f-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


