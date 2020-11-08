---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0DFCB891-7431-4C00-98DD-263DC2794354
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea6fbc76a76533c07b11935e50e25418d10e38ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099147"
---
# <span data-ttu-id="529f2-101">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="529f2-101">New-AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="529f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="529f2-102">SYNOPSIS</span></span>
<span data-ttu-id="529f2-103">Definierar ett nytt struktur jobb för en HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="529f2-103">Defines a new Hive job for an HDInsight service.</span></span>

## <span data-ttu-id="529f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="529f2-104">SYNTAX</span></span>

```
New-AzureHDInsightHiveJobDefinition [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="529f2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="529f2-105">DESCRIPTION</span></span>
<span data-ttu-id="529f2-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="529f2-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="529f2-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="529f2-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="529f2-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="529f2-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="529f2-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="529f2-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="529f2-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="529f2-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="529f2-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="529f2-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="529f2-112">Cmdleten **New-AzureHDInsightHiveJobDefinition** definierar ett Hive-jobb för en Azure HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="529f2-112">The **New-AzureHDInsightHiveJobDefinition** cmdlet defines a Hive job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="529f2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="529f2-113">EXAMPLES</span></span>

### <span data-ttu-id="529f2-114">Exempel 1: skapa en struktur jobb definition</span><span class="sxs-lookup"><span data-stu-id="529f2-114">Example 1: Create a Hive job definition</span></span>
```
PS C:\>$HiveJobDefinition = New-AzureHDInsightHiveJobDefinition -Query $QueryString
```

<span data-ttu-id="529f2-115">Det här kommandot skapar en struktur jobb definition som använder en fördefinierad frågesträng och lagrar den sedan i $HiveJobDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="529f2-115">This command creates a Hive job definition that uses a pre-defined query string, and then stores it in the $HiveJobDefinition variable.</span></span>

## <span data-ttu-id="529f2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="529f2-116">PARAMETERS</span></span>

### <span data-ttu-id="529f2-117">-Argument</span><span class="sxs-lookup"><span data-stu-id="529f2-117">-Arguments</span></span>
<span data-ttu-id="529f2-118">Anger en matris med argument för ett Hadoop-jobb.</span><span class="sxs-lookup"><span data-stu-id="529f2-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="529f2-119">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="529f2-119">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="529f2-120">-Definierar</span><span class="sxs-lookup"><span data-stu-id="529f2-120">-Defines</span></span>
<span data-ttu-id="529f2-121">Anger Hadoop-konfigurationsinställningar som ska anges när ett jobb körs.</span><span class="sxs-lookup"><span data-stu-id="529f2-121">Specifies Hadoop configuration values to set for when a job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f2-122">-Fil</span><span class="sxs-lookup"><span data-stu-id="529f2-122">-File</span></span>
<span data-ttu-id="529f2-123">Anger sökvägen till en fil som innehåller en fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="529f2-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="529f2-124">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="529f2-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="529f2-125">-Filer</span><span class="sxs-lookup"><span data-stu-id="529f2-125">-Files</span></span>
<span data-ttu-id="529f2-126">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="529f2-126">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="529f2-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="529f2-127">-JobName</span></span>
<span data-ttu-id="529f2-128">Anger namnet på det struktur jobb som ska definieras.</span><span class="sxs-lookup"><span data-stu-id="529f2-128">Specifies the name of the Hive job to define.</span></span>
<span data-ttu-id="529f2-129">Om du inte anger den här parametern används standard namnet: "struktur: \<first 100 characters of query\> ".</span><span class="sxs-lookup"><span data-stu-id="529f2-129">If you do not specify this parameter, the default name is used: "Hive: \<first 100 characters of query\>".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f2-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="529f2-130">-Profile</span></span>
<span data-ttu-id="529f2-131">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="529f2-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="529f2-132">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="529f2-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="529f2-133">-Fråga</span><span class="sxs-lookup"><span data-stu-id="529f2-133">-Query</span></span>
<span data-ttu-id="529f2-134">Anger en struktur fråga.</span><span class="sxs-lookup"><span data-stu-id="529f2-134">Specifies a Hive query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f2-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="529f2-135">-RunAsFileJob</span></span>
<span data-ttu-id="529f2-136">Anger att denna cmdlet skapar en fil i det standard-Azure Storage-konto där du vill lagra en fråga.</span><span class="sxs-lookup"><span data-stu-id="529f2-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="529f2-137">Denna cmdlet skickar jobbet som refererar till den här filen som ett skript att köra.</span><span class="sxs-lookup"><span data-stu-id="529f2-137">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="529f2-138">Du kan använda den här funktionen för att hantera specialtecken som procent tecken (%) Det innebär att det inte går att skicka jobb via Templeton eftersom Templeton tolkar en fråga med ett procent tecken som en URL-parameter.</span><span class="sxs-lookup"><span data-stu-id="529f2-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f2-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="529f2-139">-StatusFolder</span></span>
<span data-ttu-id="529f2-140">Anger platsen för mappen som innehåller standard utmatning och fel utdata för ett jobb, inklusive dess slutkod och aktivitets loggar.</span><span class="sxs-lookup"><span data-stu-id="529f2-140">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="529f2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529f2-141">CommonParameters</span></span>
<span data-ttu-id="529f2-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="529f2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529f2-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="529f2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529f2-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="529f2-144">INPUTS</span></span>

## <span data-ttu-id="529f2-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="529f2-145">OUTPUTS</span></span>

## <span data-ttu-id="529f2-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="529f2-146">NOTES</span></span>

## <span data-ttu-id="529f2-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="529f2-147">RELATED LINKS</span></span>

[<span data-ttu-id="529f2-148">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="529f2-148">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="529f2-149">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="529f2-149">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="529f2-150">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="529f2-150">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="529f2-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="529f2-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


