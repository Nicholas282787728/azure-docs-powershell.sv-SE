---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 6eab5c80fa8c21d5b592f0e194a5aba50c4d3002
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101316"
---
# <span data-ttu-id="f7637-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7637-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="f7637-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7637-102">SYNOPSIS</span></span>
<span data-ttu-id="f7637-103">Startar ett definierat Azure HDInsight-jobb i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="f7637-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="f7637-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7637-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7637-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7637-105">DESCRIPTION</span></span>
<span data-ttu-id="f7637-106">Cmdleten **Start-AzHDInsightJob** startar ett definierat Azure HDInsight-jobb i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="f7637-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="f7637-107">Detta kan vara ett MapReduce jobb, ett strömmande MapReduce jobb, ett registrerings jobb eller ett gris-jobb.</span><span class="sxs-lookup"><span data-stu-id="f7637-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="f7637-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7637-108">EXAMPLES</span></span>

### <span data-ttu-id="f7637-109">Exempel 1: starta ett jobb i angivet kluster</span><span class="sxs-lookup"><span data-stu-id="f7637-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f7637-110">Det här kommandot startar ett jobb i klustret som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="f7637-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f7637-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7637-111">PARAMETERS</span></span>

### <span data-ttu-id="f7637-112">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="f7637-112">-ClusterName</span></span>
<span data-ttu-id="f7637-113">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="f7637-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f7637-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7637-114">-DefaultProfile</span></span>
<span data-ttu-id="f7637-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f7637-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7637-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f7637-116">-HttpCredential</span></span>
<span data-ttu-id="f7637-117">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="f7637-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7637-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="f7637-118">-JobDefinition</span></span>
<span data-ttu-id="f7637-119">Anger det jobb som ska startas i Azure HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="f7637-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7637-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7637-120">-ResourceGroupName</span></span>
<span data-ttu-id="f7637-121">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f7637-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f7637-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7637-122">CommonParameters</span></span>
<span data-ttu-id="f7637-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7637-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7637-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7637-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7637-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7637-125">INPUTS</span></span>

### <span data-ttu-id="f7637-126">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f7637-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="f7637-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7637-127">OUTPUTS</span></span>

### <span data-ttu-id="f7637-128">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7637-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="f7637-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7637-129">NOTES</span></span>

## <span data-ttu-id="f7637-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7637-130">RELATED LINKS</span></span>

[<span data-ttu-id="f7637-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7637-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="f7637-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f7637-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f7637-133">Stopp-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7637-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="f7637-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7637-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


