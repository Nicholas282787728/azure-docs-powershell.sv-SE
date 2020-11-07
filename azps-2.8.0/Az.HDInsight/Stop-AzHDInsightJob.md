---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: f2c162427abc1a05c7680e0fc19e0d2406c3e4a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744051"
---
# <span data-ttu-id="9d254-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9d254-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="9d254-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d254-102">SYNOPSIS</span></span>
<span data-ttu-id="9d254-103">Stoppar ett angivet pågående jobb i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="9d254-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="9d254-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d254-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d254-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d254-105">DESCRIPTION</span></span>
<span data-ttu-id="9d254-106">Cmdleten **Stop-AzHDInsightJob** stoppar ett angivet jobb som körs på ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="9d254-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9d254-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d254-107">EXAMPLES</span></span>

### <span data-ttu-id="9d254-108">Exempel 1: stoppa ett jobb i angivet kluster</span><span class="sxs-lookup"><span data-stu-id="9d254-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="9d254-109">Det här kommandot stoppar ett jobb i klustret som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="9d254-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="9d254-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d254-110">PARAMETERS</span></span>

### <span data-ttu-id="9d254-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="9d254-111">-ClusterName</span></span>
<span data-ttu-id="9d254-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="9d254-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="9d254-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d254-113">-DefaultProfile</span></span>
<span data-ttu-id="9d254-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9d254-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d254-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="9d254-115">-HttpCredential</span></span>
<span data-ttu-id="9d254-116">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="9d254-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="9d254-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="9d254-117">-JobId</span></span>
<span data-ttu-id="9d254-118">Anger jobb-ID för jobbet.</span><span class="sxs-lookup"><span data-stu-id="9d254-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d254-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d254-119">-ResourceGroupName</span></span>
<span data-ttu-id="9d254-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9d254-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9d254-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d254-121">CommonParameters</span></span>
<span data-ttu-id="9d254-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d254-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d254-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d254-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d254-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d254-124">INPUTS</span></span>

### <span data-ttu-id="9d254-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9d254-125">System.String</span></span>

## <span data-ttu-id="9d254-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d254-126">OUTPUTS</span></span>

### <span data-ttu-id="9d254-127">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9d254-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="9d254-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d254-128">NOTES</span></span>

## <span data-ttu-id="9d254-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d254-129">RELATED LINKS</span></span>

[<span data-ttu-id="9d254-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9d254-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="9d254-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9d254-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="9d254-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9d254-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)

