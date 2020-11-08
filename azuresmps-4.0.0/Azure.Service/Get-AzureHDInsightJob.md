---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3E3C9626-7AED-4B15-93D0-0B79AD17A834
online version: ''
schema: 2.0.0
ms.openlocfilehash: de4b768dbc6c97e84bccd4c8e0ef42f6f81a5b31
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099580"
---
# <span data-ttu-id="6c8df-101">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6c8df-101">Get-AzureHDInsightJob</span></span>

## <span data-ttu-id="6c8df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c8df-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8df-103">Hämtar HDInsight-jobb.</span><span class="sxs-lookup"><span data-stu-id="6c8df-103">Gets HDInsight jobs.</span></span>

## <span data-ttu-id="6c8df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c8df-104">SYNTAX</span></span>

### <span data-ttu-id="6c8df-105">Få jobDetails historik för ett HDInsight-kluster (standard)</span><span class="sxs-lookup"><span data-stu-id="6c8df-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Get-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] [-IgnoreSslErrors <Boolean>]
 [-JobId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6c8df-106">Få jobDetails historik för ett HDInsight-kluster (med specifik prenumerations uppgifter)</span><span class="sxs-lookup"><span data-stu-id="6c8df-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Get-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] [-JobId <String>] [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6c8df-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c8df-107">DESCRIPTION</span></span>
<span data-ttu-id="6c8df-108">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="6c8df-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="6c8df-109">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="6c8df-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="6c8df-110">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6c8df-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="6c8df-111">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="6c8df-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="6c8df-112">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="6c8df-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="6c8df-113">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6c8df-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="6c8df-114">Cmdleten **Get-AzureHDInsightJob** får senaste Azure HDInsight-jobb för ett angivet kluster och visar dem i omvänd kronologisk ordning.</span><span class="sxs-lookup"><span data-stu-id="6c8df-114">The **Get-AzureHDInsightJob** cmdlet gets recent Azure HDInsight jobs for a specified cluster and displays them in reverse chronological order.</span></span>

## <span data-ttu-id="6c8df-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c8df-115">EXAMPLES</span></span>

## <span data-ttu-id="6c8df-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c8df-116">PARAMETERS</span></span>

### <span data-ttu-id="6c8df-117">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="6c8df-117">-Certificate</span></span>
<span data-ttu-id="6c8df-118">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="6c8df-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="6c8df-119">-Kluster</span><span class="sxs-lookup"><span data-stu-id="6c8df-119">-Cluster</span></span>
<span data-ttu-id="6c8df-120">Anger ett kluster.</span><span class="sxs-lookup"><span data-stu-id="6c8df-120">Specifies a cluster.</span></span>
<span data-ttu-id="6c8df-121">Denna cmdlet hämtar HDInsight-jobb som körs på klustret som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6c8df-121">This cmdlet gets HDInsight jobs that run on the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="6c8df-122">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="6c8df-122">-Credential</span></span>
<span data-ttu-id="6c8df-123">Anger de autentiseringsuppgifter som ska användas för direkt HTTP-åtkomst till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="6c8df-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="6c8df-124">Du kan ange den här parametern i stället för parametern *prenumeration* för att autentisera åtkomsten till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="6c8df-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8df-125">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="6c8df-125">-Endpoint</span></span>
<span data-ttu-id="6c8df-126">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="6c8df-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="6c8df-127">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="6c8df-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="6c8df-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="6c8df-128">-HostedService</span></span>
<span data-ttu-id="6c8df-129">Anger namn området för en HDInsight-tjänst om du inte vill använda standard namn området.</span><span class="sxs-lookup"><span data-stu-id="6c8df-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="6c8df-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="6c8df-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="6c8df-131">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="6c8df-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="6c8df-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="6c8df-132">-JobId</span></span>
<span data-ttu-id="6c8df-133">Anger ID för det jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="6c8df-133">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8df-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="6c8df-134">-Profile</span></span>
<span data-ttu-id="6c8df-135">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6c8df-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c8df-136">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6c8df-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c8df-137">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="6c8df-137">-Subscription</span></span>
<span data-ttu-id="6c8df-138">Anger den prenumeration som innehåller de HDInsight-jobb som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="6c8df-138">Specifies the subscription that contains the HDInsight jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8df-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8df-139">CommonParameters</span></span>
<span data-ttu-id="6c8df-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c8df-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8df-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c8df-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8df-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c8df-142">INPUTS</span></span>

## <span data-ttu-id="6c8df-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c8df-143">OUTPUTS</span></span>

## <span data-ttu-id="6c8df-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c8df-144">NOTES</span></span>

## <span data-ttu-id="6c8df-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c8df-145">RELATED LINKS</span></span>

[<span data-ttu-id="6c8df-146">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6c8df-146">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="6c8df-147">Stopp-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6c8df-147">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="6c8df-148">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6c8df-148">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


