---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: f51545cc28a11984c55fa05b6760b71a055de7a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916598"
---
# <span data-ttu-id="dbc41-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="dbc41-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="dbc41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbc41-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc41-103">Skickar en struktur fråga till ett HDInsight-kluster och hämtar frågeresultat i en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="dbc41-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="dbc41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbc41-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbc41-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbc41-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc41-106">Cmdleten **Invoke-AzHDInsightHiveJob** skickar en struktur fråga till ett Azure HDInsight-kluster och hämtar frågeresultat i en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="dbc41-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="dbc41-107">Använd Use-AzHDInsightCluster cmdlet innan du anropar **Invoke-AzHDInsightHiveJob** för att ange vilket kluster som ska användas för frågan.</span><span class="sxs-lookup"><span data-stu-id="dbc41-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="dbc41-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbc41-108">EXAMPLES</span></span>

### <span data-ttu-id="dbc41-109">Exempel 1: skicka en struktur fråga till ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="dbc41-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="dbc41-110">Det här kommandot skickar frågan visar tabeller till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="dbc41-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="dbc41-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbc41-111">PARAMETERS</span></span>

### <span data-ttu-id="dbc41-112">-Argument</span><span class="sxs-lookup"><span data-stu-id="dbc41-112">-Arguments</span></span>
<span data-ttu-id="dbc41-113">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="dbc41-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="dbc41-114">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="dbc41-114">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc41-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="dbc41-115">-DefaultContainer</span></span>
<span data-ttu-id="dbc41-116">Anger namnet på standard behållaren i det standardiserade Azure Storage-kontot som ett HDInsight-kluster använder.</span><span class="sxs-lookup"><span data-stu-id="dbc41-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="dbc41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc41-117">-DefaultProfile</span></span>
<span data-ttu-id="dbc41-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dbc41-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbc41-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="dbc41-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="dbc41-120">Anger konto nycklar för det standard lagrings konto som HDInsight-klustret använder.</span><span class="sxs-lookup"><span data-stu-id="dbc41-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="dbc41-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dbc41-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="dbc41-122">Anger namnet på det standard lagrings konto som HDInsight-klustret använder.</span><span class="sxs-lookup"><span data-stu-id="dbc41-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="dbc41-123">-Definierar</span><span class="sxs-lookup"><span data-stu-id="dbc41-123">-Defines</span></span>
<span data-ttu-id="dbc41-124">Anger Hadoop-konfigurationsinställningar som ska anges när ett jobb körs.</span><span class="sxs-lookup"><span data-stu-id="dbc41-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc41-125">-Fil</span><span class="sxs-lookup"><span data-stu-id="dbc41-125">-File</span></span>
<span data-ttu-id="dbc41-126">Anger sökvägen till en fil i Azure-lagringen som innehåller den fråga du vill köra.</span><span class="sxs-lookup"><span data-stu-id="dbc41-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="dbc41-127">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="dbc41-127">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="dbc41-128">-Filer</span><span class="sxs-lookup"><span data-stu-id="dbc41-128">-Files</span></span>
<span data-ttu-id="dbc41-129">Anger en samling filer som krävs för ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="dbc41-129">Specifies a collection of files that are required for a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc41-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="dbc41-130">-JobName</span></span>
<span data-ttu-id="dbc41-131">Anger namnet på ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="dbc41-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="dbc41-132">Om du inte anger den här parametern använder denna cmdlet standardvärdet: "struktur:" \< första 100 tecken \> ".</span><span class="sxs-lookup"><span data-stu-id="dbc41-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="dbc41-133">-Fråga</span><span class="sxs-lookup"><span data-stu-id="dbc41-133">-Query</span></span>
<span data-ttu-id="dbc41-134">Anger en struktur fråga.</span><span class="sxs-lookup"><span data-stu-id="dbc41-134">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="dbc41-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="dbc41-135">-RunAsFileJob</span></span>
<span data-ttu-id="dbc41-136">Anger att denna cmdlet skapar en fil i det standard-Azure Storage-konto där du vill lagra en fråga.</span><span class="sxs-lookup"><span data-stu-id="dbc41-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="dbc41-137">Denna cmdlet skickar jobbet som refererar till den här filen som ett skript att köra.</span><span class="sxs-lookup"><span data-stu-id="dbc41-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="dbc41-138">Du kan använda den här funktionen för att hantera specialtecken som procent tecken (%) Det innebär att det inte går att skicka jobb via Templeton eftersom Templeton tolkar en fråga med ett procent tecken som en URL-parameter.</span><span class="sxs-lookup"><span data-stu-id="dbc41-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc41-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="dbc41-139">-StatusFolder</span></span>
<span data-ttu-id="dbc41-140">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="dbc41-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="dbc41-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc41-141">CommonParameters</span></span>
<span data-ttu-id="dbc41-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc41-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc41-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbc41-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc41-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbc41-144">INPUTS</span></span>

### <span data-ttu-id="dbc41-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="dbc41-145">None</span></span>

## <span data-ttu-id="dbc41-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbc41-146">OUTPUTS</span></span>

### <span data-ttu-id="dbc41-147">System. String</span><span class="sxs-lookup"><span data-stu-id="dbc41-147">System.String</span></span>

## <span data-ttu-id="dbc41-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbc41-148">NOTES</span></span>

## <span data-ttu-id="dbc41-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbc41-149">RELATED LINKS</span></span>

[<span data-ttu-id="dbc41-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dbc41-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


