---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A1DFA523-B532-4902-838D-74C8CA97A335
online version: ''
schema: 2.0.0
ms.openlocfilehash: f85d12100eb5b2b093eea252ac308e8a45cf1c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099664"
---
# <span data-ttu-id="66910-101">Revoke-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="66910-101">Revoke-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="66910-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66910-102">SYNOPSIS</span></span>
<span data-ttu-id="66910-103">Inaktiverar HTTP-åtkomst till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="66910-103">Disables HTTP access to a cluster.</span></span>

## <span data-ttu-id="66910-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66910-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 [-IgnoreSslErrors <Boolean>] [-Endpoint <Uri>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="66910-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66910-105">DESCRIPTION</span></span>
<span data-ttu-id="66910-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="66910-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="66910-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="66910-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="66910-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="66910-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="66910-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="66910-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="66910-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="66910-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="66910-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="66910-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="66910-112">Med cmdleten **REVOKE-AzureHDInsightHttpServicesAccess** inaktive ras http-åtkomst till ett kluster för ODBC-, Ambari-, Oozie-och WebHCatalog webb tjänster.</span><span class="sxs-lookup"><span data-stu-id="66910-112">The **Revoke-AzureHDInsightHttpServicesAccess** cmdlet disables HTTP access to a cluster for ODBC, Ambari, Oozie and WebHCatalog web services.</span></span>

## <span data-ttu-id="66910-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66910-113">EXAMPLES</span></span>

## <span data-ttu-id="66910-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66910-114">PARAMETERS</span></span>

### <span data-ttu-id="66910-115">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="66910-115">-Certificate</span></span>
<span data-ttu-id="66910-116">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="66910-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="66910-117">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="66910-117">-Endpoint</span></span>
<span data-ttu-id="66910-118">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="66910-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="66910-119">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="66910-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="66910-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="66910-120">-HostedService</span></span>
<span data-ttu-id="66910-121">Anger namn området för en HDInsight-tjänst om du inte vill använda standard namn området.</span><span class="sxs-lookup"><span data-stu-id="66910-121">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="66910-122">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="66910-122">-IgnoreSslErrors</span></span>
<span data-ttu-id="66910-123">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="66910-123">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="66910-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="66910-124">-Location</span></span>
<span data-ttu-id="66910-125">Anger den region där ett HDInsight-kluster finns.</span><span class="sxs-lookup"><span data-stu-id="66910-125">Specifies the region in which an HDInsight cluster is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66910-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="66910-126">-Name</span></span>
<span data-ttu-id="66910-127">Anger namnet på ett kluster.</span><span class="sxs-lookup"><span data-stu-id="66910-127">Specifies the name of a cluster.</span></span>
<span data-ttu-id="66910-128">Denna cmdlet inaktiverar HTTP-åtkomst till det kluster som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="66910-128">This cmdlet disables HTTP access to the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66910-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="66910-129">-Profile</span></span>
<span data-ttu-id="66910-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="66910-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66910-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="66910-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66910-132">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="66910-132">-Subscription</span></span>
<span data-ttu-id="66910-133">Anger det abonnemang som innehåller HDInsight-klustret att återkalla.</span><span class="sxs-lookup"><span data-stu-id="66910-133">Specifies the subscription account that contains the HDInsight cluster to revoke.</span></span>

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

### <span data-ttu-id="66910-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66910-134">CommonParameters</span></span>
<span data-ttu-id="66910-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66910-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66910-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66910-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66910-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66910-137">INPUTS</span></span>

## <span data-ttu-id="66910-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66910-138">OUTPUTS</span></span>

## <span data-ttu-id="66910-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66910-139">NOTES</span></span>

## <span data-ttu-id="66910-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66910-140">RELATED LINKS</span></span>

[<span data-ttu-id="66910-141">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="66910-141">Grant-AzureHDInsightHttpServicesAccess</span></span>](./Grant-AzureHDInsightHttpServicesAccess.md)


