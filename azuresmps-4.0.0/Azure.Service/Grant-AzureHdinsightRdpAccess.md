---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 95CCEB79-EAC4-4F56-B289-5401F976E5F5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92b2c005f855ccf99e8bae4d8db8445ba7e63dad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099492"
---
# <span data-ttu-id="f124e-101">Grant-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="f124e-101">Grant-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="f124e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f124e-102">SYNOPSIS</span></span>
<span data-ttu-id="f124e-103">Ger RDP-åtkomst till ett HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="f124e-103">Grants RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="f124e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f124e-104">SYNTAX</span></span>

```
Grant-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -RdpCredential <PSCredential> -RdpAccessExpiry <DateTime> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f124e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f124e-105">DESCRIPTION</span></span>
<span data-ttu-id="f124e-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="f124e-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f124e-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="f124e-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f124e-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f124e-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f124e-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f124e-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f124e-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f124e-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f124e-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f124e-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f124e-112">Cmdleten **Grant-AzureHDInsightRdpAccess** beviljar RDP-åtkomst (Remote Desktop Protocol) till ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="f124e-112">The **Grant-AzureHDInsightRdpAccess** cmdlet grants Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f124e-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f124e-113">EXAMPLES</span></span>

## <span data-ttu-id="f124e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f124e-114">PARAMETERS</span></span>

### <span data-ttu-id="f124e-115">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="f124e-115">-Certificate</span></span>
<span data-ttu-id="f124e-116">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="f124e-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="f124e-117">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="f124e-117">-Endpoint</span></span>
<span data-ttu-id="f124e-118">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="f124e-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="f124e-119">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="f124e-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="f124e-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="f124e-120">-HostedService</span></span>
<span data-ttu-id="f124e-121">Anger namn området för en HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="f124e-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="f124e-122">Om du inte anger den här parametern använder denna cmdlet standard namn området.</span><span class="sxs-lookup"><span data-stu-id="f124e-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="f124e-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="f124e-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="f124e-124">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="f124e-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="f124e-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="f124e-125">-Location</span></span>
<span data-ttu-id="f124e-126">Anger i vilken Azure region ett kluster finns.</span><span class="sxs-lookup"><span data-stu-id="f124e-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="f124e-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="f124e-127">-Name</span></span>
<span data-ttu-id="f124e-128">Anger namnet på ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="f124e-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="f124e-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="f124e-129">-Profile</span></span>
<span data-ttu-id="f124e-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f124e-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f124e-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f124e-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f124e-132">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="f124e-132">-RdpAccessExpiry</span></span>
<span data-ttu-id="f124e-133">Anger förfallo datum, som ett **datetime** -objekt, för RDP-åtkomst (Remote Desktop Protocol) till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="f124e-133">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f124e-134">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="f124e-134">-RdpCredential</span></span>
<span data-ttu-id="f124e-135">Anger autentiseringsuppgifter för RDP-åtkomst till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="f124e-135">Specifies the credentials for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="f124e-136">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="f124e-136">-Subscription</span></span>
<span data-ttu-id="f124e-137">Anger vilken prenumeration som innehåller det HDInsight-kluster som du vill bevilja åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="f124e-137">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="f124e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f124e-138">CommonParameters</span></span>
<span data-ttu-id="f124e-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f124e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f124e-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f124e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f124e-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f124e-141">INPUTS</span></span>

## <span data-ttu-id="f124e-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f124e-142">OUTPUTS</span></span>

## <span data-ttu-id="f124e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f124e-143">NOTES</span></span>

## <span data-ttu-id="f124e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f124e-144">RELATED LINKS</span></span>

[<span data-ttu-id="f124e-145">Återkalla-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="f124e-145">Revoke-AzureHdinsightRdpAccess</span></span>](./Revoke-AzureHdinsightRdpAccess.md)


