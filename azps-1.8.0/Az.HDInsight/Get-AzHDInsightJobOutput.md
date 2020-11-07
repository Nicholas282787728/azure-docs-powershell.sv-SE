---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 3d4ffa7a3172921b8aba7d73fc2c468c0e3117f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916634"
---
# <span data-ttu-id="b0894-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="b0894-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="b0894-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0894-102">SYNOPSIS</span></span>
<span data-ttu-id="b0894-103">Hämtar loggens utdata för ett jobb från det lagrings konto som är kopplat till ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="b0894-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="b0894-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0894-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0894-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0894-105">DESCRIPTION</span></span>
<span data-ttu-id="b0894-106">Cmdleten **Get-AzHDInsightJobOutput** hämtar logg resultatet för ett jobb från det lagrings konto som är kopplat till ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="b0894-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b0894-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0894-107">EXAMPLES</span></span>

### <span data-ttu-id="b0894-108">Exempel 1: Hämta logg resultatet för ett jobb</span><span class="sxs-lookup"><span data-stu-id="b0894-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b0894-109">Det här kommandot hämtar loggen från det kluster som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="b0894-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b0894-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0894-110">PARAMETERS</span></span>

### <span data-ttu-id="b0894-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="b0894-111">-ClusterName</span></span>
<span data-ttu-id="b0894-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="b0894-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b0894-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="b0894-113">-DefaultContainer</span></span>
<span data-ttu-id="b0894-114">Anger standard behållarens namn.</span><span class="sxs-lookup"><span data-stu-id="b0894-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="b0894-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0894-115">-DefaultProfile</span></span>
<span data-ttu-id="b0894-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b0894-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0894-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b0894-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="b0894-118">Anger standard för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b0894-118">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="b0894-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b0894-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="b0894-120">Anger standard namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="b0894-120">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="b0894-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="b0894-121">-DisplayOutputType</span></span>
<span data-ttu-id="b0894-122">Anger utskrifts typen för jobbet som begärs.</span><span class="sxs-lookup"><span data-stu-id="b0894-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="b0894-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b0894-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b0894-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="b0894-124">StandardOutput</span></span>
- <span data-ttu-id="b0894-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="b0894-125">StandardError</span></span>

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

### <span data-ttu-id="b0894-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="b0894-126">-HttpCredential</span></span>
<span data-ttu-id="b0894-127">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="b0894-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="b0894-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="b0894-128">-JobId</span></span>
<span data-ttu-id="b0894-129">Anger jobb-ID för det jobb vars utdata ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="b0894-129">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="b0894-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0894-130">-ResourceGroupName</span></span>
<span data-ttu-id="b0894-131">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b0894-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b0894-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0894-132">CommonParameters</span></span>
<span data-ttu-id="b0894-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0894-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0894-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0894-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0894-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0894-135">INPUTS</span></span>

### <span data-ttu-id="b0894-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="b0894-136">None</span></span>

## <span data-ttu-id="b0894-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0894-137">OUTPUTS</span></span>

### <span data-ttu-id="b0894-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b0894-138">System.String</span></span>

## <span data-ttu-id="b0894-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0894-139">NOTES</span></span>

## <span data-ttu-id="b0894-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0894-140">RELATED LINKS</span></span>

[<span data-ttu-id="b0894-141">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b0894-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="b0894-142">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b0894-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


