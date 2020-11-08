---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EE2ADA86-B2A3-4F6F-96EF-BB61D6DC550F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 338bef67e771bf211c063bf054e13e3844497850
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093490"
---
# <span data-ttu-id="fe2b5-101">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fe2b5-101">Stop-AzureHDInsightJob</span></span>

## <span data-ttu-id="fe2b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe2b5-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2b5-103">Stoppar ett HDInsight-jobb.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-103">Stops an HDInsight job.</span></span>

## <span data-ttu-id="fe2b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe2b5-104">SYNTAX</span></span>

### <span data-ttu-id="fe2b5-105">Starta jobDetails i ett HDInsight-kluster (standard)</span><span class="sxs-lookup"><span data-stu-id="fe2b5-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Stop-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fe2b5-106">Starta jobDetails i ett HDInsight-kluster (med specifik prenumerations uppgifter)</span><span class="sxs-lookup"><span data-stu-id="fe2b5-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Stop-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fe2b5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe2b5-107">DESCRIPTION</span></span>
<span data-ttu-id="fe2b5-108">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="fe2b5-109">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="fe2b5-110">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="fe2b5-111">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="fe2b5-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="fe2b5-112">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="fe2b5-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="fe2b5-113">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fe2b5-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="fe2b5-114">Cmdleten **Stop-AzureHDInsightJob** stoppar ett Azure HDInsight-jobb i angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-114">The **Stop-AzureHDInsightJob** cmdlet stops an Azure HDInsight job on the specified cluster.</span></span>

## <span data-ttu-id="fe2b5-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe2b5-115">EXAMPLES</span></span>

## <span data-ttu-id="fe2b5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe2b5-116">PARAMETERS</span></span>

### <span data-ttu-id="fe2b5-117">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="fe2b5-117">-Certificate</span></span>
<span data-ttu-id="fe2b5-118">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="fe2b5-119">-Kluster</span><span class="sxs-lookup"><span data-stu-id="fe2b5-119">-Cluster</span></span>
<span data-ttu-id="fe2b5-120">Anger ett kluster.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-120">Specifies a cluster.</span></span>
<span data-ttu-id="fe2b5-121">Denna cmdlet stoppar ett jobb som körs på det kluster som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-121">This cmdlet stops a job that runs on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2b5-122">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="fe2b5-122">-Credential</span></span>
<span data-ttu-id="fe2b5-123">Anger de autentiseringsuppgifter som ska användas för direkt HTTP-åtkomst till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="fe2b5-124">Du kan ange den här parametern i stället för parametern *prenumeration* för att autentisera åtkomsten till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

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

### <span data-ttu-id="fe2b5-125">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="fe2b5-125">-Endpoint</span></span>
<span data-ttu-id="fe2b5-126">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="fe2b5-127">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="fe2b5-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="fe2b5-128">-HostedService</span></span>
<span data-ttu-id="fe2b5-129">Anger namn området för en HDInsight-tjänst om du inte vill använda standard namn området.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="fe2b5-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="fe2b5-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="fe2b5-131">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="fe2b5-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="fe2b5-132">-JobId</span></span>
<span data-ttu-id="fe2b5-133">Anger ID: t för HDInsight-jobbet som ska stoppas.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-133">Specifies the ID of the HDInsight job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2b5-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="fe2b5-134">-Profile</span></span>
<span data-ttu-id="fe2b5-135">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe2b5-136">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe2b5-137">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="fe2b5-137">-Subscription</span></span>
<span data-ttu-id="fe2b5-138">Anger ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-138">Specifies a subscription.</span></span>
<span data-ttu-id="fe2b5-139">Denna cmdlet stoppar ett jobb för det abonnemang som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-139">This cmdlet stops a job for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="fe2b5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2b5-140">CommonParameters</span></span>
<span data-ttu-id="fe2b5-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2b5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2b5-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe2b5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2b5-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe2b5-143">INPUTS</span></span>

## <span data-ttu-id="fe2b5-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe2b5-144">OUTPUTS</span></span>

## <span data-ttu-id="fe2b5-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe2b5-145">NOTES</span></span>

## <span data-ttu-id="fe2b5-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe2b5-146">RELATED LINKS</span></span>

[<span data-ttu-id="fe2b5-147">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fe2b5-147">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="fe2b5-148">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fe2b5-148">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="fe2b5-149">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fe2b5-149">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)

