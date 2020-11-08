---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E11AAB11-0CBF-4746-91D7-4D5E64801C29
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6dba4c331a69093f49c95728c028eaaf5d0bdb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099145"
---
# <span data-ttu-id="3c8b9-101">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c8b9-101">New-AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="3c8b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3c8b9-103">Definierar ett nytt Sqoop-jobb.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-103">Defines a new Sqoop job.</span></span>

## <span data-ttu-id="3c8b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c8b9-104">SYNTAX</span></span>

```
New-AzureHDInsightSqoopJobDefinition [-Command <String>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3c8b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c8b9-105">DESCRIPTION</span></span>
<span data-ttu-id="3c8b9-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="3c8b9-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="3c8b9-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="3c8b9-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="3c8b9-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="3c8b9-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="3c8b9-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="3c8b9-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3c8b9-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="3c8b9-112">Cmdleten **New-AzureHDInsightSqoopJobDefinition** skapar ett Sqoop-jobb som körs på ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-112">The **New-AzureHDInsightSqoopJobDefinition** cmdlet creates a Sqoop job to run on an Azure HDInsight cluster.</span></span>

<span data-ttu-id="3c8b9-113">Sqoop är ett verktyg som används för att överföra data mellan Hadoop-kluster och Relations databaser.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-113">Sqoop is a tool to transfer data between Hadoop clusters and relational databases.</span></span>
<span data-ttu-id="3c8b9-114">Du kan använda Sqoop för att importera data från en SQL Server-databas till ett Hadoop Distributed File System (HDFS), transformera data med Hadoop MapReduce och sedan exportera data från HDFS tillbaka till SQL Server-databasen.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-114">You can use Sqoop to import data from a SQL Server database to a Hadoop Distributed File System (HDFS), transform the data with Hadoop MapReduce, and then export the data from the HDFS back to the SQL Server database.</span></span>

## <span data-ttu-id="3c8b9-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c8b9-115">EXAMPLES</span></span>

### <span data-ttu-id="3c8b9-116">Exempel 1: importera data</span><span class="sxs-lookup"><span data-stu-id="3c8b9-116">Example 1: Import data</span></span>
```
PS C:\>$SqoopJobDef = New-AzureHDInsightSqoopJobDefinition -Command "import --connect jdbc:sqlserver://<SQLDatabaseServerName>.database.windows.net:1433;username=<SQLDatabasUsername>@<SQLDatabaseServerName>; password=<SQLDatabasePassword>; database=<SQLDatabaseDatabaseName> --table <TableName> --target-dir wasb://<ContainerName>@<WindowsAzureStorageAccountName>.blob.core.windows.net/<Path>"
```

<span data-ttu-id="3c8b9-117">Det här kommandot definierar ett Sqoop-jobb som importerar alla rader i en tabell från en AzureSQL-Server databas till ett HDInsight-kluster och lagrar sedan jobb definitionen i variabeln $SqoopJobDef.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-117">This command defines a Sqoop job that imports all of the rows in a table from an AzureSQL Server database to an HDInsight cluster, and then stores the job definition in the $SqoopJobDef variable.</span></span>

## <span data-ttu-id="3c8b9-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c8b9-118">PARAMETERS</span></span>

### <span data-ttu-id="3c8b9-119">-Kommando</span><span class="sxs-lookup"><span data-stu-id="3c8b9-119">-Command</span></span>
<span data-ttu-id="3c8b9-120">Anger ett Sqoop-kommando och dess argument.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-120">Specifies a Sqoop command and its arguments.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8b9-121">-Fil</span><span class="sxs-lookup"><span data-stu-id="3c8b9-121">-File</span></span>
<span data-ttu-id="3c8b9-122">Anger sökvägen till en skript fil som innehåller de kommandon som ska köras.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-122">Specifies the path to a script file that contains the commands to run.</span></span>
<span data-ttu-id="3c8b9-123">Skript filen måste finnas på WASB.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-123">The script file must be located on WASB.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8b9-124">-Filer</span><span class="sxs-lookup"><span data-stu-id="3c8b9-124">-Files</span></span>
<span data-ttu-id="3c8b9-125">Anger samlingen med WASB-filer som krävs för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-125">Specifies the collection of WASB files that are required for a job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8b9-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c8b9-126">-Profile</span></span>
<span data-ttu-id="3c8b9-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c8b9-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8b9-129">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="3c8b9-129">-StatusFolder</span></span>
<span data-ttu-id="3c8b9-130">Anger platsen för mappen som innehåller standard utmatning och fel utdata för ett jobb, inklusive dess slutkod och aktivitets loggar.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-130">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8b9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c8b9-131">CommonParameters</span></span>
<span data-ttu-id="3c8b9-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c8b9-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c8b9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c8b9-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c8b9-134">INPUTS</span></span>

## <span data-ttu-id="3c8b9-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c8b9-135">OUTPUTS</span></span>

## <span data-ttu-id="3c8b9-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c8b9-136">NOTES</span></span>

## <span data-ttu-id="3c8b9-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c8b9-137">RELATED LINKS</span></span>

[<span data-ttu-id="3c8b9-138">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c8b9-138">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="3c8b9-139">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c8b9-139">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="3c8b9-140">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c8b9-140">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="3c8b9-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3c8b9-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


