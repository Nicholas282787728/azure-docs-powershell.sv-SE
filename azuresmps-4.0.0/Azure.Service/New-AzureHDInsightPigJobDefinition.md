---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 227D933A-9272-4C53-89AF-711379B47A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c32a80bec0820123a8ccf1a85f5c99bdac3195d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099240"
---
# <span data-ttu-id="69069-101">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="69069-101">New-AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="69069-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69069-102">SYNOPSIS</span></span>
<span data-ttu-id="69069-103">Definierar ett nytt gris-jobb för en HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="69069-103">Defines a new Pig job for an HDInsight service.</span></span>

## <span data-ttu-id="69069-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69069-104">SYNTAX</span></span>

```
New-AzureHDInsightPigJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-Query <String>] [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69069-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69069-105">DESCRIPTION</span></span>
<span data-ttu-id="69069-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="69069-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="69069-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="69069-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="69069-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="69069-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="69069-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="69069-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="69069-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="69069-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="69069-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="69069-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="69069-112">**New-AzureHDInsightPigJobDefinition** definierar ett gris-jobb för en Azure HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="69069-112">The **New-AzureHDInsightPigJobDefinition** defines a Pig job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="69069-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69069-113">EXAMPLES</span></span>

### <span data-ttu-id="69069-114">Exempel 1: definiera ett nytt gris-jobb</span><span class="sxs-lookup"><span data-stu-id="69069-114">Example 1: Define a new Pig job</span></span>
```
PS C:\>$0 = '$0';
PS C:\> $QueryString =  "LOGS = LOAD 'wasb:///example/data/sample.log';" + "LEVELS = foreach LOGS generate REGEX_EXTRACT($0, '(TRACE|DEBUG|INFO|WARN|ERROR|FATAL)', 1) as LOGLEVEL;" + "FILTEREDLEVELS = FILTER LEVELS by LOGLEVEL is not null;" + "GROUPEDLEVELS = GROUP FILTEREDLEVELS by LOGLEVEL;" + "FREQUENCIES = foreach GROUPEDLEVELS generate group as LOGLEVEL, COUNT(FILTEREDLEVELS.LOGLEVEL) as COUNT;" + "RESULT = order FREQUENCIES by COUNT desc;" + "DUMP RESULT;"
PS C:\> $PigJobDefinition = New-AzureHDInsightPigJobDefinition -Query $QueryString
```

<span data-ttu-id="69069-115">Det första kommandot förklarar ett sträng värde och lagrar sedan i $0-variabeln.</span><span class="sxs-lookup"><span data-stu-id="69069-115">The first command declares a string value, and then stores in the $0 variable.</span></span>

<span data-ttu-id="69069-116">Det andra kommandot skapar en gris-jobbiljett och lagrar dem sedan i $QueryString variabel.</span><span class="sxs-lookup"><span data-stu-id="69069-116">The second command creates a Pig job query, and then stores it in the $QueryString variable.</span></span>

<span data-ttu-id="69069-117">Med kommandot slut skapas en jobb definition för gris som använder frågan i $QueryString och lagrar sedan jobb definitionen i $PigJobDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="69069-117">The final command creates a Pig job definition that uses the query in $QueryString, and then stores the job definition in the $PigJobDefinition variable.</span></span>

## <span data-ttu-id="69069-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69069-118">PARAMETERS</span></span>

### <span data-ttu-id="69069-119">-Argument</span><span class="sxs-lookup"><span data-stu-id="69069-119">-Arguments</span></span>
<span data-ttu-id="69069-120">Anger en matris med argument för ett gris-jobb.</span><span class="sxs-lookup"><span data-stu-id="69069-120">Specifies an array of arguments for a Pig job.</span></span>
<span data-ttu-id="69069-121">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="69069-121">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69069-122">-Fil</span><span class="sxs-lookup"><span data-stu-id="69069-122">-File</span></span>
<span data-ttu-id="69069-123">Anger sökvägen till en fil som innehåller en fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="69069-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="69069-124">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="69069-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="69069-125">-Filer</span><span class="sxs-lookup"><span data-stu-id="69069-125">-Files</span></span>
<span data-ttu-id="69069-126">Anger en samling filer som är associerade med ett gris-jobb.</span><span class="sxs-lookup"><span data-stu-id="69069-126">Specifies a collection of files that are associated with a Pig job.</span></span>

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

### <span data-ttu-id="69069-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="69069-127">-Profile</span></span>
<span data-ttu-id="69069-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="69069-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69069-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="69069-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69069-130">-Fråga</span><span class="sxs-lookup"><span data-stu-id="69069-130">-Query</span></span>
<span data-ttu-id="69069-131">Anger en gris-jobbiljett.</span><span class="sxs-lookup"><span data-stu-id="69069-131">Specifies a Pig job query.</span></span>

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

### <span data-ttu-id="69069-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="69069-132">-StatusFolder</span></span>
<span data-ttu-id="69069-133">Anger platsen för mappen som innehåller standard utmatning och fel utdata för ett jobb, inklusive dess slutkod och aktivitets loggar.</span><span class="sxs-lookup"><span data-stu-id="69069-133">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="69069-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69069-134">CommonParameters</span></span>
<span data-ttu-id="69069-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69069-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69069-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69069-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69069-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69069-137">INPUTS</span></span>

## <span data-ttu-id="69069-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69069-138">OUTPUTS</span></span>

## <span data-ttu-id="69069-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69069-139">NOTES</span></span>

## <span data-ttu-id="69069-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69069-140">RELATED LINKS</span></span>

[<span data-ttu-id="69069-141">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="69069-141">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="69069-142">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="69069-142">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="69069-143">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="69069-143">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="69069-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="69069-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


