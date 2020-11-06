---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 674c8f1cb5fdf8d8c76da36a7bb6d8df06e29c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585548"
---
# <span data-ttu-id="cf0b4-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cf0b4-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="cf0b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf0b4-102">SYNOPSIS</span></span>
<span data-ttu-id="cf0b4-103">Stoppar ett angivet pågående jobb i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf0b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf0b4-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf0b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf0b4-105">DESCRIPTION</span></span>
<span data-ttu-id="cf0b4-106">Cmdleten **Stop-AzureRmHDInsightJob** stoppar ett angivet jobb som körs på ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="cf0b4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf0b4-107">EXAMPLES</span></span>

### <span data-ttu-id="cf0b4-108">Exempel 1: stoppa ett jobb i angivet kluster</span><span class="sxs-lookup"><span data-stu-id="cf0b4-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="cf0b4-109">Det här kommandot stoppar ett jobb i klustret som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="cf0b4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf0b4-110">PARAMETERS</span></span>

### <span data-ttu-id="cf0b4-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="cf0b4-111">-ClusterName</span></span>
<span data-ttu-id="cf0b4-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="cf0b4-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="cf0b4-113">-HttpCredential</span></span>
<span data-ttu-id="cf0b4-114">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="cf0b4-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="cf0b4-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="cf0b4-115">-JobId</span></span>
<span data-ttu-id="cf0b4-116">Anger jobb-ID för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="cf0b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf0b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf0b4-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cf0b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf0b4-119">-DefaultProfile</span></span>
<span data-ttu-id="cf0b4-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf0b4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf0b4-121">CommonParameters</span></span>
<span data-ttu-id="cf0b4-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf0b4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf0b4-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf0b4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf0b4-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf0b4-124">INPUTS</span></span>

### <span data-ttu-id="cf0b4-125">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="cf0b4-125">String</span></span>
<span data-ttu-id="cf0b4-126">Parametern "JobId" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="cf0b4-126">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="cf0b4-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf0b4-127">OUTPUTS</span></span>

### <span data-ttu-id="cf0b4-128">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cf0b4-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="cf0b4-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf0b4-129">NOTES</span></span>

## <span data-ttu-id="cf0b4-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf0b4-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf0b4-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cf0b4-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="cf0b4-132">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cf0b4-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="cf0b4-133">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cf0b4-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


