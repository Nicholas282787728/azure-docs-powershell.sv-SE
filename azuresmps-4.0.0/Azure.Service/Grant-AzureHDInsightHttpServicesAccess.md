---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E3D22B03-2997-4F2C-895E-AE0993FD7C92
online version: ''
schema: 2.0.0
ms.openlocfilehash: bfd3e1f2bb5d057dec8a7bee5929ba5c67c8d53d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099728"
---
# <span data-ttu-id="4ca3a-101">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4ca3a-101">Grant-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="4ca3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ca3a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca3a-103">Ger HTTP-åtkomst till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-103">Grants HTTP access to a cluster.</span></span>

## <span data-ttu-id="4ca3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ca3a-104">SYNTAX</span></span>

```
Grant-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Credential <PSCredential> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4ca3a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ca3a-105">DESCRIPTION</span></span>
<span data-ttu-id="4ca3a-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="4ca3a-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="4ca3a-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="4ca3a-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="4ca3a-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="4ca3a-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="4ca3a-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="4ca3a-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4ca3a-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="4ca3a-112">**Grant-AzureHDInsightHttpServicesAccess** cmdlet beviljar http-åtkomst till ett Azure HDInsight-kluster med ODBC, Ambari, Oozie och webb tjänster.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-112">The **Grant-AzureHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie, and web services.</span></span>

## <span data-ttu-id="4ca3a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ca3a-113">EXAMPLES</span></span>

## <span data-ttu-id="4ca3a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ca3a-114">PARAMETERS</span></span>

### <span data-ttu-id="4ca3a-115">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="4ca3a-115">-Certificate</span></span>
<span data-ttu-id="4ca3a-116">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="4ca3a-117">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="4ca3a-117">-Credential</span></span>
<span data-ttu-id="4ca3a-118">Anger ett användar namn och lösen ord för HTTP-åtkomst.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-118">Specifies a user name and password for HTTP access.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca3a-119">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="4ca3a-119">-Endpoint</span></span>
<span data-ttu-id="4ca3a-120">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-120">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="4ca3a-121">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-121">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="4ca3a-122">-HostedService</span><span class="sxs-lookup"><span data-stu-id="4ca3a-122">-HostedService</span></span>
<span data-ttu-id="4ca3a-123">Anger namn området för en HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-123">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="4ca3a-124">Om du inte anger den här parametern använder denna cmdlet standard namn området.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-124">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="4ca3a-125">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="4ca3a-125">-IgnoreSslErrors</span></span>
<span data-ttu-id="4ca3a-126">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-126">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="4ca3a-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="4ca3a-127">-Location</span></span>
<span data-ttu-id="4ca3a-128">Anger i vilken Azure region ett kluster finns.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-128">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="4ca3a-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ca3a-129">-Name</span></span>
<span data-ttu-id="4ca3a-130">Anger namnet på ett kluster.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-130">Specifies the name of a cluster.</span></span>
<span data-ttu-id="4ca3a-131">Denna cmdlet beviljar HTTP-åtkomst till det kluster som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-131">This cmdlet grants HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ca3a-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="4ca3a-132">-Profile</span></span>
<span data-ttu-id="4ca3a-133">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4ca3a-134">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4ca3a-135">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="4ca3a-135">-Subscription</span></span>
<span data-ttu-id="4ca3a-136">Anger vilken prenumeration som innehåller det HDInsight-kluster som du vill bevilja åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-136">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="4ca3a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca3a-137">CommonParameters</span></span>
<span data-ttu-id="4ca3a-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca3a-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca3a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca3a-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ca3a-140">INPUTS</span></span>

## <span data-ttu-id="4ca3a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ca3a-141">OUTPUTS</span></span>

## <span data-ttu-id="4ca3a-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ca3a-142">NOTES</span></span>

## <span data-ttu-id="4ca3a-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ca3a-143">RELATED LINKS</span></span>

[<span data-ttu-id="4ca3a-144">Återkalla-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4ca3a-144">Revoke-AzureHDInsightHttpServicesAccess</span></span>](./Revoke-AzureHDInsightHttpServicesAccess.md)


