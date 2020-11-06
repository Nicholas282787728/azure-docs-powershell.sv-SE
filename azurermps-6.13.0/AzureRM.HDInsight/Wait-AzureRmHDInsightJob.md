---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/wait-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: de7df9417e617f88c61e75c64dd42f32b83fc66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578044"
---
# <span data-ttu-id="a524e-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a524e-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="a524e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a524e-102">SYNOPSIS</span></span>
<span data-ttu-id="a524e-103">Väntar på att ett visst jobb ska slutföras eller misslyckande.</span><span class="sxs-lookup"><span data-stu-id="a524e-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a524e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a524e-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a524e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a524e-105">DESCRIPTION</span></span>
<span data-ttu-id="a524e-106">Cmdleten **wait-AzureRmHDInsightJob** väntar på att ett Azure HDInsight-jobb ska slutföras eller inte.</span><span class="sxs-lookup"><span data-stu-id="a524e-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="a524e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a524e-107">EXAMPLES</span></span>

### <span data-ttu-id="a524e-108">Exempel 1: vänta på att ett jobb är färdigt eller misslyckande</span><span class="sxs-lookup"><span data-stu-id="a524e-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="a524e-109">Det här kommandot väntar på att jobbet ska slutföras eller inte.</span><span class="sxs-lookup"><span data-stu-id="a524e-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="a524e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a524e-110">PARAMETERS</span></span>

### <span data-ttu-id="a524e-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="a524e-111">-ClusterName</span></span>
<span data-ttu-id="a524e-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="a524e-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a524e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a524e-113">-DefaultProfile</span></span>
<span data-ttu-id="a524e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a524e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a524e-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="a524e-115">-HttpCredential</span></span>
<span data-ttu-id="a524e-116">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="a524e-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="a524e-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="a524e-117">-JobId</span></span>
<span data-ttu-id="a524e-118">Anger jobb-ID för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a524e-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="a524e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a524e-119">-ResourceGroupName</span></span>
<span data-ttu-id="a524e-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a524e-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a524e-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="a524e-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="a524e-122">Den totala vänte tiden för slut för ande av jobb, i sekunder.</span><span class="sxs-lookup"><span data-stu-id="a524e-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="a524e-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a524e-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="a524e-124">Det går inte att vänta mellan jobb status kontrollen i sekunder.</span><span class="sxs-lookup"><span data-stu-id="a524e-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="a524e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a524e-125">CommonParameters</span></span>
<span data-ttu-id="a524e-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a524e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a524e-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a524e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a524e-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a524e-128">INPUTS</span></span>

### <span data-ttu-id="a524e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a524e-129">System.String</span></span>
<span data-ttu-id="a524e-130">Parametrar: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a524e-130">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="a524e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a524e-131">OUTPUTS</span></span>

### <span data-ttu-id="a524e-132">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a524e-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="a524e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a524e-133">NOTES</span></span>

## <span data-ttu-id="a524e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a524e-134">RELATED LINKS</span></span>

[<span data-ttu-id="a524e-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a524e-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="a524e-136">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a524e-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="a524e-137">Stopp-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a524e-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


