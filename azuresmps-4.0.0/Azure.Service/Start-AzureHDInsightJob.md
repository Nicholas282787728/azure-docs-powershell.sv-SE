---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 60A5ACF7-2637-4BDC-BF41-80E81B23F4CD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0308c3ff5bee358a82d74d452784f42c69bc7c32
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093150"
---
# <span data-ttu-id="1372b-101">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1372b-101">Start-AzureHDInsightJob</span></span>

## <span data-ttu-id="1372b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1372b-102">SYNOPSIS</span></span>
<span data-ttu-id="1372b-103">Startar ett HDInsight-jobb.</span><span class="sxs-lookup"><span data-stu-id="1372b-103">Starts an HDInsight job.</span></span>

## <span data-ttu-id="1372b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1372b-104">SYNTAX</span></span>

### <span data-ttu-id="1372b-105">Starta jobDetails i ett HDInsight-kluster (standard)</span><span class="sxs-lookup"><span data-stu-id="1372b-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Start-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>]
 -JobDefinition <AzureHDInsightJobDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1372b-106">Starta jobDetails i ett HDInsight-kluster (med specifik prenumerations uppgifter)</span><span class="sxs-lookup"><span data-stu-id="1372b-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Start-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobDefinition <AzureHDInsightJobDefinition>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1372b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1372b-107">DESCRIPTION</span></span>
<span data-ttu-id="1372b-108">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="1372b-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="1372b-109">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="1372b-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="1372b-110">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1372b-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="1372b-111">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="1372b-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="1372b-112">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="1372b-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="1372b-113">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1372b-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="1372b-114">Cmdleten **Start-AzureHDInsightJob** startar ett definierat Azure HDInsight-jobb i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="1372b-114">The **Start-AzureHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="1372b-115">Jobbet som ska startas kan vara ett MapReduce jobb, ett strömmande jobb, ett registrerings jobb eller ett gris-jobb.</span><span class="sxs-lookup"><span data-stu-id="1372b-115">The job to start can be a MapReduce job, a streaming job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="1372b-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1372b-116">EXAMPLES</span></span>

### <span data-ttu-id="1372b-117">Exempel 1: starta ett HDInsight-jobb</span><span class="sxs-lookup"><span data-stu-id="1372b-117">Example 1: Start an HDInsight job</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "Cluster01" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="1372b-118">Det första kommandot får aktuellt abonnemangs-ID och lagrar det sedan i $SubId variabel.</span><span class="sxs-lookup"><span data-stu-id="1372b-118">The first command gets the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="1372b-119">Det andra kommandot tilldelar namnet Cluster01 till variabeln $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="1372b-119">The second command assigns the name Cluster01 to the $ClusterName variable.</span></span>

<span data-ttu-id="1372b-120">I det tredje kommandot används cmdleten **New-AzureHDInsightMapReduceJobDefinition** för att skapa en MapReduce jobb definition och sedan lagras den i $WordCountJob variabel.</span><span class="sxs-lookup"><span data-stu-id="1372b-120">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="1372b-121">Det sista kommandot använder pipeline-operatorn för att överföra $WordCountJob till cmdleten **Start-AzureHDInsightJob** för att starta jobbet.</span><span class="sxs-lookup"><span data-stu-id="1372b-121">The final command uses the pipeline operator to pass the $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="1372b-122">När jobbet har startat skickas det till cmdleten **wait-AzureHDInsightJob** , som väntar på att jobbet ska slutföras innan det skickas till cmdleten **Get-AzureHDInsightJobOutput** för att få jobbet.</span><span class="sxs-lookup"><span data-stu-id="1372b-122">After the job starts, it is passed to the **Wait-AzureHDInsightJob** cmdlet, which waits for the job to complete before passing it to the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="1372b-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1372b-123">PARAMETERS</span></span>

### <span data-ttu-id="1372b-124">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="1372b-124">-Certificate</span></span>
<span data-ttu-id="1372b-125">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1372b-125">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1372b-126">-Kluster</span><span class="sxs-lookup"><span data-stu-id="1372b-126">-Cluster</span></span>
<span data-ttu-id="1372b-127">Anger ett kluster.</span><span class="sxs-lookup"><span data-stu-id="1372b-127">Specifies a cluster.</span></span>
<span data-ttu-id="1372b-128">Denna cmdlet startar ett jobb på klustret som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1372b-128">This cmdlet starts a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1372b-129">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="1372b-129">-Credential</span></span>
<span data-ttu-id="1372b-130">Anger klusterkonfigurationer för direkt HTTP-åtkomst till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="1372b-130">Specifies cluster credentials for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="1372b-131">Du kan ange den här parametern i stället för parametern *prenumeration* för att autentisera åtkomsten till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="1372b-131">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1372b-132">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="1372b-132">-Endpoint</span></span>
<span data-ttu-id="1372b-133">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="1372b-133">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="1372b-134">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="1372b-134">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1372b-135">-HostedService</span><span class="sxs-lookup"><span data-stu-id="1372b-135">-HostedService</span></span>
<span data-ttu-id="1372b-136">Anger namn området för en HDInsight-tjänst om du inte vill använda standard namn området.</span><span class="sxs-lookup"><span data-stu-id="1372b-136">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1372b-137">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="1372b-137">-IgnoreSslErrors</span></span>
<span data-ttu-id="1372b-138">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="1372b-138">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1372b-139">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="1372b-139">-JobDefinition</span></span>
<span data-ttu-id="1372b-140">Anger den slut punkt som ska användas vid anslutning till Microsoft Azure om slut punkten skiljer sig från standard.</span><span class="sxs-lookup"><span data-stu-id="1372b-140">Specifies the endpoint to use when connecting to Microsoft Azure if the endpoint is different from the default.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: jobDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1372b-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="1372b-141">-Profile</span></span>
<span data-ttu-id="1372b-142">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1372b-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1372b-143">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="1372b-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1372b-144">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="1372b-144">-Subscription</span></span>
<span data-ttu-id="1372b-145">Anger ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="1372b-145">Specifies a subscription.</span></span>
<span data-ttu-id="1372b-146">Denna cmdlet startar ett jobb för det abonnemang som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1372b-146">This cmdlet starts a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1372b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1372b-147">CommonParameters</span></span>
<span data-ttu-id="1372b-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1372b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1372b-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1372b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1372b-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1372b-150">INPUTS</span></span>

## <span data-ttu-id="1372b-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1372b-151">OUTPUTS</span></span>

## <span data-ttu-id="1372b-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1372b-152">NOTES</span></span>

## <span data-ttu-id="1372b-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1372b-153">RELATED LINKS</span></span>

[<span data-ttu-id="1372b-154">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1372b-154">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="1372b-155">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="1372b-155">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="1372b-156">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1372b-156">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="1372b-157">Stopp-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1372b-157">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="1372b-158">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1372b-158">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


