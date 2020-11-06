---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/stop-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 7247a4f5e23bc4f0f3c520f909cec221ee03e1ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576277"
---
# <span data-ttu-id="c8296-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c8296-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="c8296-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8296-102">SYNOPSIS</span></span>
<span data-ttu-id="c8296-103">Stoppar ett angivet pågående jobb i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="c8296-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8296-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8296-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8296-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8296-105">DESCRIPTION</span></span>
<span data-ttu-id="c8296-106">Cmdleten **Stop-AzureRmHDInsightJob** stoppar ett angivet jobb som körs på ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="c8296-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c8296-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8296-107">EXAMPLES</span></span>

### <span data-ttu-id="c8296-108">Exempel 1: stoppa ett jobb i angivet kluster</span><span class="sxs-lookup"><span data-stu-id="c8296-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="c8296-109">Det här kommandot stoppar ett jobb i klustret som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="c8296-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c8296-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8296-110">PARAMETERS</span></span>

### <span data-ttu-id="c8296-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="c8296-111">-ClusterName</span></span>
<span data-ttu-id="c8296-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="c8296-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c8296-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8296-113">-DefaultProfile</span></span>
<span data-ttu-id="c8296-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c8296-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8296-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="c8296-115">-HttpCredential</span></span>
<span data-ttu-id="c8296-116">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="c8296-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="c8296-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="c8296-117">-JobId</span></span>
<span data-ttu-id="c8296-118">Anger jobb-ID för jobbet.</span><span class="sxs-lookup"><span data-stu-id="c8296-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="c8296-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8296-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8296-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c8296-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c8296-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8296-121">CommonParameters</span></span>
<span data-ttu-id="c8296-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8296-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8296-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8296-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8296-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8296-124">INPUTS</span></span>

### <span data-ttu-id="c8296-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c8296-125">System.String</span></span>
<span data-ttu-id="c8296-126">Parametrar: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8296-126">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="c8296-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8296-127">OUTPUTS</span></span>

### <span data-ttu-id="c8296-128">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c8296-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="c8296-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8296-129">NOTES</span></span>

## <span data-ttu-id="c8296-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8296-130">RELATED LINKS</span></span>

[<span data-ttu-id="c8296-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c8296-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="c8296-132">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c8296-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="c8296-133">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c8296-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


