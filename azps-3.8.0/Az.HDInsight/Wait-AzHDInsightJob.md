---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 6b87b7f6e3482aad974c5f7d334724f5d2f99e7c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088165"
---
# <span data-ttu-id="70bff-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="70bff-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="70bff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70bff-102">SYNOPSIS</span></span>
<span data-ttu-id="70bff-103">Väntar på att ett visst jobb ska slutföras eller misslyckande.</span><span class="sxs-lookup"><span data-stu-id="70bff-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="70bff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70bff-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70bff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70bff-105">DESCRIPTION</span></span>
<span data-ttu-id="70bff-106">Cmdleten **wait-AzHDInsightJob** väntar på att ett Azure HDInsight-jobb ska slutföras eller inte.</span><span class="sxs-lookup"><span data-stu-id="70bff-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="70bff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70bff-107">EXAMPLES</span></span>

### <span data-ttu-id="70bff-108">Exempel 1: vänta på att ett jobb är färdigt eller misslyckande</span><span class="sxs-lookup"><span data-stu-id="70bff-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="70bff-109">Det här kommandot väntar på att jobbet ska slutföras eller inte.</span><span class="sxs-lookup"><span data-stu-id="70bff-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="70bff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70bff-110">PARAMETERS</span></span>

### <span data-ttu-id="70bff-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="70bff-111">-ClusterName</span></span>
<span data-ttu-id="70bff-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="70bff-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="70bff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bff-113">-DefaultProfile</span></span>
<span data-ttu-id="70bff-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="70bff-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70bff-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="70bff-115">-HttpCredential</span></span>
<span data-ttu-id="70bff-116">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="70bff-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="70bff-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="70bff-117">-JobId</span></span>
<span data-ttu-id="70bff-118">Anger jobb-ID för jobbet.</span><span class="sxs-lookup"><span data-stu-id="70bff-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="70bff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70bff-119">-ResourceGroupName</span></span>
<span data-ttu-id="70bff-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="70bff-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="70bff-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="70bff-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="70bff-122">Den totala vänte tiden för slut för ande av jobb, i sekunder.</span><span class="sxs-lookup"><span data-stu-id="70bff-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="70bff-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="70bff-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="70bff-124">Det går inte att vänta mellan jobb status kontrollen i sekunder.</span><span class="sxs-lookup"><span data-stu-id="70bff-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="70bff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bff-125">CommonParameters</span></span>
<span data-ttu-id="70bff-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70bff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bff-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70bff-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bff-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70bff-128">INPUTS</span></span>

### <span data-ttu-id="70bff-129">System. String</span><span class="sxs-lookup"><span data-stu-id="70bff-129">System.String</span></span>

## <span data-ttu-id="70bff-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70bff-130">OUTPUTS</span></span>

### <span data-ttu-id="70bff-131">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="70bff-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="70bff-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70bff-132">NOTES</span></span>

## <span data-ttu-id="70bff-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70bff-133">RELATED LINKS</span></span>

[<span data-ttu-id="70bff-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="70bff-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="70bff-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="70bff-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="70bff-136">Stopp-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="70bff-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

