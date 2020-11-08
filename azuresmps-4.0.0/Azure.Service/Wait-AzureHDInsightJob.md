---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 2EA36090-1A45-4F77-9222-9C0E9C07656C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea1247fd2b91f173b8125ad61c0bf2b57f408d18
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099062"
---
# <span data-ttu-id="fd5ed-101">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fd5ed-101">Wait-AzureHDInsightJob</span></span>

## <span data-ttu-id="fd5ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd5ed-102">SYNOPSIS</span></span>
<span data-ttu-id="fd5ed-103">Väntar på att ett HDInsight-jobb ska slutföras eller misslyckats och visar projektets förlopp.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-103">Awaits the completion or failure of an HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="fd5ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd5ed-104">SYNTAX</span></span>

### <span data-ttu-id="fd5ed-105">Få jobDetails historik för ett HDInsight-kluster (standard)</span><span class="sxs-lookup"><span data-stu-id="fd5ed-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fd5ed-106">Få jobDetails historik för ett HDInsight-kluster (med specifik prenumerations uppgifter)</span><span class="sxs-lookup"><span data-stu-id="fd5ed-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Wait-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Job <AzureHDInsightJob> -Subscription <String> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fd5ed-107">Vänta med jobb med JobId i ett HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="fd5ed-107">Wait Job with JobId on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-WaitTimeoutInSeconds <Double>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fd5ed-108">Vänta med jobbet i ett HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="fd5ed-108">Wait Job with Job on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] -Job <AzureHDInsightJob> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fd5ed-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd5ed-109">DESCRIPTION</span></span>
<span data-ttu-id="fd5ed-110">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-110">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="fd5ed-111">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-111">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="fd5ed-112">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-112">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="fd5ed-113">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="fd5ed-113">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="fd5ed-114">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="fd5ed-114">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="fd5ed-115">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fd5ed-115">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="fd5ed-116">Cmdleten **wait-AzureHDInsightJob** väntar på att ett Azure HDInsight-jobb är ifyllt eller misslyckat och visar projektets förlopp.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-116">The **Wait-AzureHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="fd5ed-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd5ed-117">EXAMPLES</span></span>

### <span data-ttu-id="fd5ed-118">Exempel 1: kör ett jobb och vänta tills det är färdigt</span><span class="sxs-lookup"><span data-stu-id="fd5ed-118">Example 1: Run a job and wait for it to complete</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:>\ $ClusterName = "MyCluster"
PS C:>\ $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:>\ $WordCountJob | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="fd5ed-119">Det första kommandot får det aktuella Azure-prenumerations-ID: t och lagrar det sedan i $SubId variabel.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-119">The first command gets the current Azure subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="fd5ed-120">Det andra kommandot hämtar det angivna klustret och lagrar det sedan i $ClusterName variabel.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-120">The second command gets the specified cluster, and then stores it in the $ClusterName variable.</span></span>

<span data-ttu-id="fd5ed-121">I det tredje kommandot används cmdleten **New-AzureHDInsightMapReduceJobDefinition** för att skapa en MapReduce jobb definition och sedan lagras den i $WordCountJob variabel.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-121">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="fd5ed-122">Det fjärde kommandot använder flera cmdlets i följd:</span><span class="sxs-lookup"><span data-stu-id="fd5ed-122">The fourth command uses several cmdlets in sequence:</span></span> 

- <span data-ttu-id="fd5ed-123">Den används för att skicka $WordCountJob till cmdleten **Start-AzureHDInsightJob** för att starta jobbet.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-123">It uses the pipeline operator to pass $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span> 
- <span data-ttu-id="fd5ed-124">Jobbet skickas till **vänta-AzureHDInsightJob** cmdlet för att vänta 3600 sekunder för jobbet att slutföras.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-124">The job is passed to the **Wait-AzureHDInsightJob** cmdlet to wait 3600 seconds for the job to complete.</span></span> 
- <span data-ttu-id="fd5ed-125">Om jobbet är slutfört använder kommandot cmdleten **Get-AzureHDInsightJobOutput** för att hämta utskriften.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-125">If the job completes, the command uses the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="fd5ed-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd5ed-126">PARAMETERS</span></span>

### <span data-ttu-id="fd5ed-127">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="fd5ed-127">-Certificate</span></span>
<span data-ttu-id="fd5ed-128">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-128">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5ed-129">-Kluster</span><span class="sxs-lookup"><span data-stu-id="fd5ed-129">-Cluster</span></span>
<span data-ttu-id="fd5ed-130">Anger ett kluster.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-130">Specifies a cluster.</span></span>
<span data-ttu-id="fd5ed-131">Denna cmdlet väntar på ett jobb i klustret som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-131">This cmdlet waits for a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd5ed-132">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="fd5ed-132">-Credential</span></span>
<span data-ttu-id="fd5ed-133">Anger de autentiseringsuppgifter som ska användas för direkt HTTP-åtkomst till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-133">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="fd5ed-134">Du kan ange den här parametern i stället för parametern *prenumeration* för att autentisera åtkomsten till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-134">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster, Wait Job with JobId on an HDInsight Cluster, Wait Job with Job on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5ed-135">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="fd5ed-135">-Endpoint</span></span>
<span data-ttu-id="fd5ed-136">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-136">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="fd5ed-137">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-137">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5ed-138">-HostedService</span><span class="sxs-lookup"><span data-stu-id="fd5ed-138">-HostedService</span></span>
<span data-ttu-id="fd5ed-139">Anger namn området för en HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-139">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="fd5ed-140">Om du inte anger den här parametern används standard namn området.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-140">If you do not specify this parameter, the default namespace is used.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5ed-141">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="fd5ed-141">-IgnoreSslErrors</span></span>
<span data-ttu-id="fd5ed-142">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-142">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5ed-143">-Jobb</span><span class="sxs-lookup"><span data-stu-id="fd5ed-143">-Job</span></span>
<span data-ttu-id="fd5ed-144">Anger ett Azure HDInsight-jobb.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-144">Specifies an Azure HDInsight job.</span></span>

```yaml
Type: AzureHDInsightJob
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential), Wait Job with Job on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd5ed-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="fd5ed-145">-JobId</span></span>
<span data-ttu-id="fd5ed-146">Anger ID för jobbet som ska besvaras.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-146">Specifies the ID of the job to wait for.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd5ed-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="fd5ed-147">-Profile</span></span>
<span data-ttu-id="fd5ed-148">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fd5ed-149">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fd5ed-150">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="fd5ed-150">-Subscription</span></span>
<span data-ttu-id="fd5ed-151">Anger ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-151">Specifies a subscription.</span></span>
<span data-ttu-id="fd5ed-152">Denna cmdlet väntar på ett jobb för det abonnemang som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-152">This cmdlet waits for a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5ed-153">-WaitTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="fd5ed-153">-WaitTimeoutInSeconds</span></span>
<span data-ttu-id="fd5ed-154">Anger timeout i sekunder för vänte åtgärden.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-154">Specifies the time-out, in seconds, for the wait operation.</span></span>
<span data-ttu-id="fd5ed-155">Om timeout infaller innan jobbet är slutfört upphör cmdleten att köras.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-155">If the time-out expires before the job completes, the cmdlet ceases to run.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd5ed-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd5ed-156">CommonParameters</span></span>
<span data-ttu-id="fd5ed-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd5ed-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd5ed-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd5ed-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd5ed-159">INPUTS</span></span>

## <span data-ttu-id="fd5ed-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd5ed-160">OUTPUTS</span></span>

## <span data-ttu-id="fd5ed-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd5ed-161">NOTES</span></span>

## <span data-ttu-id="fd5ed-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd5ed-162">RELATED LINKS</span></span>

[<span data-ttu-id="fd5ed-163">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fd5ed-163">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="fd5ed-164">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="fd5ed-164">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="fd5ed-165">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fd5ed-165">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="fd5ed-166">Stopp-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fd5ed-166">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)


