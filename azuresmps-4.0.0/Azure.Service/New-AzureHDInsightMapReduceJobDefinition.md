---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099146"
---
# <span data-ttu-id="5127b-101">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5127b-101">New-AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="5127b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5127b-102">SYNOPSIS</span></span>
<span data-ttu-id="5127b-103">Definierar ett nytt MapReduce-jobb.</span><span class="sxs-lookup"><span data-stu-id="5127b-103">Defines a new MapReduce job.</span></span>

## <span data-ttu-id="5127b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5127b-104">SYNTAX</span></span>

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5127b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5127b-105">DESCRIPTION</span></span>
<span data-ttu-id="5127b-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="5127b-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="5127b-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="5127b-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="5127b-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5127b-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="5127b-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="5127b-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="5127b-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="5127b-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="5127b-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5127b-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="5127b-112">Cmdleten **New-AzureHDInsightMapReduceJobDefinition** definierar ett nytt MapReduce-jobb som ska köras på ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="5127b-112">The **New-AzureHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job to run on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5127b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5127b-113">EXAMPLES</span></span>

### <span data-ttu-id="5127b-114">Exempel 1: definiera ett MapReduce-jobb, kör jobbet och få utdata</span><span class="sxs-lookup"><span data-stu-id="5127b-114">Example 1: Define a MapReduce job, run the job, and get the output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="5127b-115">Det första kommandot får ID för det aktuella abonnemanget och lagrar det sedan i $SubId variabel.</span><span class="sxs-lookup"><span data-stu-id="5127b-115">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="5127b-116">Det andra kommandot tilldelar namnet till $Clustername variabeln.</span><span class="sxs-lookup"><span data-stu-id="5127b-116">The second command assigns the name MyCluster to the $Clustername variable.</span></span>

<span data-ttu-id="5127b-117">I det tredje kommandot används cmdleten **New-AzureHDInsightMapReduceJobDefinition** för att skapa en MapReduce-jobb definition och sedan spara den i $WordCountJob variabel.</span><span class="sxs-lookup"><span data-stu-id="5127b-117">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then store it in the $WordCountJob variable.</span></span>

<span data-ttu-id="5127b-118">Det fjärde kommandot utför en sekvens med operationer genom att använda dessa cmdletar:</span><span class="sxs-lookup"><span data-stu-id="5127b-118">The fourth command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="5127b-119">**Start-AzureHDInsightJob** för att starta jobbet på $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="5127b-119">**Start-AzureHDInsightJob** to start the job on $ClusterName.</span></span> 
- <span data-ttu-id="5127b-120">**Vänta-AzureHDInsightJob** att vänta tills jobbet är klart och visar förloppet mot färdigheten.</span><span class="sxs-lookup"><span data-stu-id="5127b-120">**Wait-AzureHDInsightJob** to wait for the job to finish and to display the progress toward completion.</span></span>
- <span data-ttu-id="5127b-121">**Get-AzureHDInsightJobOutput** för att få jobbet utflödet.</span><span class="sxs-lookup"><span data-stu-id="5127b-121">**Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="5127b-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5127b-122">PARAMETERS</span></span>

### <span data-ttu-id="5127b-123">-Argument</span><span class="sxs-lookup"><span data-stu-id="5127b-123">-Arguments</span></span>
<span data-ttu-id="5127b-124">Anger en matris med argument för ett Hadoop-jobb.</span><span class="sxs-lookup"><span data-stu-id="5127b-124">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="5127b-125">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="5127b-125">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="5127b-126">-Klass namn</span><span class="sxs-lookup"><span data-stu-id="5127b-126">-ClassName</span></span>
<span data-ttu-id="5127b-127">Anger namnet på jobb klassen i burk-filen (Java Archive).</span><span class="sxs-lookup"><span data-stu-id="5127b-127">Specifies the name of the job class in the Java Archive (JAR) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5127b-128">-Definierar</span><span class="sxs-lookup"><span data-stu-id="5127b-128">-Defines</span></span>
<span data-ttu-id="5127b-129">Anger Hadoop-konfigurationsinställningar som ska anges när jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="5127b-129">Specifies Hadoop configuration values to set when the job runs.</span></span>

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

### <span data-ttu-id="5127b-130">-Filer</span><span class="sxs-lookup"><span data-stu-id="5127b-130">-Files</span></span>
<span data-ttu-id="5127b-131">Anger en matris med WASB-filer som krävs för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="5127b-131">Specifies an array of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="5127b-132">-JarFile</span><span class="sxs-lookup"><span data-stu-id="5127b-132">-JarFile</span></span>
<span data-ttu-id="5127b-133">Anger det fullständigt kvalificerade namnet på en JAR-fil som innehåller koden och beroendena för ett MapReduce-jobb.</span><span class="sxs-lookup"><span data-stu-id="5127b-133">Specifies the fully qualified name of a JAR file that contains the code and dependencies of a MapReduce job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5127b-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="5127b-134">-JobName</span></span>
<span data-ttu-id="5127b-135">Anger namnet på ett MapReduce-jobb.</span><span class="sxs-lookup"><span data-stu-id="5127b-135">Specifies the name of a MapReduce job.</span></span>
<span data-ttu-id="5127b-136">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="5127b-136">This parameter is optional.</span></span>
<span data-ttu-id="5127b-137">Om du inte anger den här parametern används värdet för parametern *className* .</span><span class="sxs-lookup"><span data-stu-id="5127b-137">If you do not specify this parameter, the value of the *ClassName* parameter is used.</span></span>

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

### <span data-ttu-id="5127b-138">-LibJars</span><span class="sxs-lookup"><span data-stu-id="5127b-138">-LibJars</span></span>
<span data-ttu-id="5127b-139">Anger en matris med LibJar-referenser för jobbet.</span><span class="sxs-lookup"><span data-stu-id="5127b-139">Specifies an array of LibJar references of the job.</span></span>

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

### <span data-ttu-id="5127b-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="5127b-140">-Profile</span></span>
<span data-ttu-id="5127b-141">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5127b-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5127b-142">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5127b-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5127b-143">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="5127b-143">-StatusFolder</span></span>
<span data-ttu-id="5127b-144">Anger platsen för mappen som innehåller standard utmatning och fel utdata för ett jobb, inklusive dess slutkod och aktivitets loggar.</span><span class="sxs-lookup"><span data-stu-id="5127b-144">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="5127b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5127b-145">CommonParameters</span></span>
<span data-ttu-id="5127b-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5127b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5127b-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5127b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5127b-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5127b-148">INPUTS</span></span>

## <span data-ttu-id="5127b-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5127b-149">OUTPUTS</span></span>

## <span data-ttu-id="5127b-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5127b-150">NOTES</span></span>

## <span data-ttu-id="5127b-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5127b-151">RELATED LINKS</span></span>

[<span data-ttu-id="5127b-152">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="5127b-152">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="5127b-153">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5127b-153">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="5127b-154">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5127b-154">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="5127b-155">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5127b-155">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="5127b-156">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5127b-156">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="5127b-157">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5127b-157">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


