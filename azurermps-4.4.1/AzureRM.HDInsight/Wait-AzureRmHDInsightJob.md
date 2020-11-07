---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: 6e19594cfcd79c6be82373af6245ea2154296b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758406"
---
# <span data-ttu-id="0328d-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0328d-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="0328d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0328d-102">SYNOPSIS</span></span>
<span data-ttu-id="0328d-103">Väntar på att ett visst jobb ska slutföras eller misslyckande.</span><span class="sxs-lookup"><span data-stu-id="0328d-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0328d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0328d-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0328d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0328d-105">DESCRIPTION</span></span>
<span data-ttu-id="0328d-106">Cmdleten **wait-AzureRmHDInsightJob** väntar på att ett Azure HDInsight-jobb ska slutföras eller inte.</span><span class="sxs-lookup"><span data-stu-id="0328d-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="0328d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0328d-107">EXAMPLES</span></span>

### <span data-ttu-id="0328d-108">Exempel 1: vänta på att ett jobb är färdigt eller misslyckande</span><span class="sxs-lookup"><span data-stu-id="0328d-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="0328d-109">Det här kommandot väntar på att jobbet ska slutföras eller inte.</span><span class="sxs-lookup"><span data-stu-id="0328d-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="0328d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0328d-110">PARAMETERS</span></span>

### <span data-ttu-id="0328d-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="0328d-111">-ClusterName</span></span>
<span data-ttu-id="0328d-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="0328d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0328d-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="0328d-113">-HttpCredential</span></span>
<span data-ttu-id="0328d-114">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="0328d-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="0328d-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="0328d-115">-JobId</span></span>
<span data-ttu-id="0328d-116">Anger jobb-ID för jobbet.</span><span class="sxs-lookup"><span data-stu-id="0328d-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="0328d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0328d-117">-ResourceGroupName</span></span>
<span data-ttu-id="0328d-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0328d-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0328d-119">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="0328d-119">-TimeoutInSeconds</span></span>
<span data-ttu-id="0328d-120">Den totala vänte tiden för slut för ande av jobb, i sekunder.</span><span class="sxs-lookup"><span data-stu-id="0328d-120">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="0328d-121">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0328d-121">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="0328d-122">Det går inte att vänta mellan jobb status kontrollen i sekunder.</span><span class="sxs-lookup"><span data-stu-id="0328d-122">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="0328d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0328d-123">-DefaultProfile</span></span>
<span data-ttu-id="0328d-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0328d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0328d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0328d-125">CommonParameters</span></span>
<span data-ttu-id="0328d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0328d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0328d-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0328d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0328d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0328d-128">INPUTS</span></span>

### <span data-ttu-id="0328d-129">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="0328d-129">String</span></span>
<span data-ttu-id="0328d-130">Parametern "JobId" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="0328d-130">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="0328d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0328d-131">OUTPUTS</span></span>

### <span data-ttu-id="0328d-132">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0328d-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="0328d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0328d-133">NOTES</span></span>

## <span data-ttu-id="0328d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0328d-134">RELATED LINKS</span></span>

[<span data-ttu-id="0328d-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0328d-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="0328d-136">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0328d-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="0328d-137">Stopp-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0328d-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


