---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: 94bd90b644b12723a36266dea34d9b5e9417b45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577008"
---
# <span data-ttu-id="65318-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="65318-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="65318-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65318-102">SYNOPSIS</span></span>
<span data-ttu-id="65318-103">Hämtar loggens utdata för ett jobb från det lagrings konto som är kopplat till ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="65318-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65318-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65318-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65318-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65318-105">DESCRIPTION</span></span>
<span data-ttu-id="65318-106">Cmdleten **Get-AzureRmHDInsightJobOutput** hämtar logg resultatet för ett jobb från det lagrings konto som är kopplat till ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="65318-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="65318-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65318-107">EXAMPLES</span></span>

### <span data-ttu-id="65318-108">Exempel 1: Hämta logg resultatet för ett jobb</span><span class="sxs-lookup"><span data-stu-id="65318-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="65318-109">Det här kommandot hämtar loggen från det kluster som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="65318-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="65318-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65318-110">PARAMETERS</span></span>

### <span data-ttu-id="65318-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="65318-111">-ClusterName</span></span>
<span data-ttu-id="65318-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="65318-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="65318-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="65318-113">-DefaultContainer</span></span>
<span data-ttu-id="65318-114">Anger standard behållarens namn.</span><span class="sxs-lookup"><span data-stu-id="65318-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="65318-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65318-115">-DefaultProfile</span></span>
<span data-ttu-id="65318-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="65318-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65318-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="65318-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="65318-118">Anger standard för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="65318-118">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65318-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="65318-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="65318-120">Anger standard namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="65318-120">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65318-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="65318-121">-DisplayOutputType</span></span>
<span data-ttu-id="65318-122">Anger utskrifts typen för jobbet som begärs.</span><span class="sxs-lookup"><span data-stu-id="65318-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="65318-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="65318-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65318-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="65318-124">StandardOutput</span></span>
- <span data-ttu-id="65318-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="65318-125">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases:
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65318-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="65318-126">-HttpCredential</span></span>
<span data-ttu-id="65318-127">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="65318-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65318-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="65318-128">-JobId</span></span>
<span data-ttu-id="65318-129">Anger jobb-ID för det jobb vars utdata ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="65318-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65318-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65318-130">-ResourceGroupName</span></span>
<span data-ttu-id="65318-131">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="65318-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="65318-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65318-132">CommonParameters</span></span>
<span data-ttu-id="65318-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65318-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65318-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65318-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65318-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65318-135">INPUTS</span></span>

### <span data-ttu-id="65318-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="65318-136">None</span></span>

## <span data-ttu-id="65318-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65318-137">OUTPUTS</span></span>

### <span data-ttu-id="65318-138">System. String</span><span class="sxs-lookup"><span data-stu-id="65318-138">System.String</span></span>

## <span data-ttu-id="65318-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65318-139">NOTES</span></span>

## <span data-ttu-id="65318-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65318-140">RELATED LINKS</span></span>

[<span data-ttu-id="65318-141">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="65318-141">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="65318-142">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="65318-142">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


