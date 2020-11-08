---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093366"
---
# <span data-ttu-id="71c0e-101">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="71c0e-101">Get-AzureHDInsightJobOutput</span></span>

## <span data-ttu-id="71c0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="71c0e-103">Hämtar loggen för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="71c0e-103">Gets the log output for a job.</span></span>

## <span data-ttu-id="71c0e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71c0e-104">SYNTAX</span></span>

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="71c0e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71c0e-105">DESCRIPTION</span></span>
<span data-ttu-id="71c0e-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="71c0e-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="71c0e-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="71c0e-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="71c0e-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="71c0e-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="71c0e-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i skapa Linux-baserade kluster i [HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="71c0e-109">For information about how to use the new HDInsight to create a cluster, see Create Linux-based clusters in [HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="71c0e-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="71c0e-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="71c0e-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight-cmdletar](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="71c0e-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="71c0e-112">Cmdleten **Get-AzureHDInsightJobOutput** hämtar logg resultatet för ett jobb från det lagrings konto som är kopplat till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="71c0e-112">The **Get-AzureHDInsightJobOutput** cmdlet gets the log output for a job from the storage account associated with a cluster.</span></span>
<span data-ttu-id="71c0e-113">Du kan få olika typer av jobb loggar, inklusive standardutdata, standard fel, aktivitets loggar och en sammanfattning av aktivitets loggarna.</span><span class="sxs-lookup"><span data-stu-id="71c0e-113">You can get various types of job logs including standard output, standard error, task logs, and a summary of the task logs.</span></span>

## <span data-ttu-id="71c0e-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71c0e-114">EXAMPLES</span></span>

### <span data-ttu-id="71c0e-115">Exempel 1: få jobb ut</span><span class="sxs-lookup"><span data-stu-id="71c0e-115">Example 1: Get job output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

<span data-ttu-id="71c0e-116">Det första kommandot får ID för det aktuella abonnemanget och lagrar det sedan i $SubId variabel.</span><span class="sxs-lookup"><span data-stu-id="71c0e-116">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="71c0e-117">Med det andra kommandot lagras namnet mina kluster i $Clustername variabel.</span><span class="sxs-lookup"><span data-stu-id="71c0e-117">The second command stores the name MyCluster in the $Clustername variable.</span></span>

<span data-ttu-id="71c0e-118">Det tredje kommandot skapar en MapReduce och lagrar sedan den i $WordCountJob variabel.</span><span class="sxs-lookup"><span data-stu-id="71c0e-118">The third command creates a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>
<span data-ttu-id="71c0e-119">Kommandot skickar jobbet i $WordCountJob till cmdleten **Start-AzureHDInsightJob** för att starta jobbet.</span><span class="sxs-lookup"><span data-stu-id="71c0e-119">The command passes the job in $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="71c0e-120">Den skickar också $WordCountJob till **wait-AzureHDInsightJob** -cmdleten för att vänta på att jobbet avslutas och sedan används **Get-AzureHDInsightJobOutput** för att hämta utskriften.</span><span class="sxs-lookup"><span data-stu-id="71c0e-120">It also passes $WordCountJob to the **Wait-AzureHDInsightJob** cmdlet to wait for the job to finish, and then it uses **Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="71c0e-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71c0e-121">PARAMETERS</span></span>

### <span data-ttu-id="71c0e-122">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="71c0e-122">-Certificate</span></span>
<span data-ttu-id="71c0e-123">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="71c0e-123">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c0e-124">-Kluster</span><span class="sxs-lookup"><span data-stu-id="71c0e-124">-Cluster</span></span>
<span data-ttu-id="71c0e-125">Anger ett kluster.</span><span class="sxs-lookup"><span data-stu-id="71c0e-125">Specifies a cluster.</span></span>
<span data-ttu-id="71c0e-126">Denna cmdlet hämtar jobb loggar från klustret som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="71c0e-126">This cmdlet gets job logs from the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71c0e-127">-DownloadTaskLogs</span><span class="sxs-lookup"><span data-stu-id="71c0e-127">-DownloadTaskLogs</span></span>
<span data-ttu-id="71c0e-128">Anger att denna cmdlet hämtar aktivitets loggar för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="71c0e-128">Indicates that this cmdlet gets the task logs for a job.</span></span>

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

### <span data-ttu-id="71c0e-129">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="71c0e-129">-Endpoint</span></span>
<span data-ttu-id="71c0e-130">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="71c0e-130">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="71c0e-131">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="71c0e-131">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c0e-132">-HostedService</span><span class="sxs-lookup"><span data-stu-id="71c0e-132">-HostedService</span></span>
<span data-ttu-id="71c0e-133">Anger namn området för en HDInsight-tjänst om du inte vill använda standard namn området.</span><span class="sxs-lookup"><span data-stu-id="71c0e-133">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c0e-134">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="71c0e-134">-IgnoreSslErrors</span></span>
<span data-ttu-id="71c0e-135">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="71c0e-135">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c0e-136">-JobId</span><span class="sxs-lookup"><span data-stu-id="71c0e-136">-JobId</span></span>
<span data-ttu-id="71c0e-137">Anger ID för det jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="71c0e-137">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71c0e-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="71c0e-138">-Profile</span></span>
<span data-ttu-id="71c0e-139">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="71c0e-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71c0e-140">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="71c0e-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71c0e-141">-StandardError</span><span class="sxs-lookup"><span data-stu-id="71c0e-141">-StandardError</span></span>
<span data-ttu-id="71c0e-142">Anger att denna cmdlet får StdErr-resultatet från ett jobb.</span><span class="sxs-lookup"><span data-stu-id="71c0e-142">Indicates that this cmdlet gets the StdErr output of a job.</span></span>

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

### <span data-ttu-id="71c0e-143">-StandardOutput</span><span class="sxs-lookup"><span data-stu-id="71c0e-143">-StandardOutput</span></span>
<span data-ttu-id="71c0e-144">Anger att den här cmdleten får SdtOut-utdata från ett jobb.</span><span class="sxs-lookup"><span data-stu-id="71c0e-144">Indicates that this cmdlet gets the SdtOut output of a job.</span></span>

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

### <span data-ttu-id="71c0e-145">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="71c0e-145">-Subscription</span></span>
<span data-ttu-id="71c0e-146">Anger den prenumeration som innehåller HDInsight-klustret att få.</span><span class="sxs-lookup"><span data-stu-id="71c0e-146">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c0e-147">-TaskLogsDirectory</span><span class="sxs-lookup"><span data-stu-id="71c0e-147">-TaskLogsDirectory</span></span>
<span data-ttu-id="71c0e-148">Anger en lokal mapp där aktivitets loggar ska sparas.</span><span class="sxs-lookup"><span data-stu-id="71c0e-148">Specifies a local folder in which to store tasks logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c0e-149">-TaskSummary</span><span class="sxs-lookup"><span data-stu-id="71c0e-149">-TaskSummary</span></span>
<span data-ttu-id="71c0e-150">Anger att den här cmdleten hämtar sammanfattningen av aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="71c0e-150">Indicates that this cmdlets gets the task log summary.</span></span>

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

### <span data-ttu-id="71c0e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c0e-151">CommonParameters</span></span>
<span data-ttu-id="71c0e-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c0e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c0e-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c0e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c0e-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71c0e-154">INPUTS</span></span>

## <span data-ttu-id="71c0e-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71c0e-155">OUTPUTS</span></span>

## <span data-ttu-id="71c0e-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71c0e-156">NOTES</span></span>

## <span data-ttu-id="71c0e-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71c0e-157">RELATED LINKS</span></span>

[<span data-ttu-id="71c0e-158">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="71c0e-158">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="71c0e-159">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="71c0e-159">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="71c0e-160">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="71c0e-160">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)
