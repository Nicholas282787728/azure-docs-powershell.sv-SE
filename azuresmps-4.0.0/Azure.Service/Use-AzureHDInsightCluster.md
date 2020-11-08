---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0BF58D9C-814E-4276-823F-D566DC99391C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 773af58d0ae9b4ca940240875b5cf9a8d3a0ffe7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099067"
---
# <span data-ttu-id="b05b4-101">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b05b4-101">Use-AzureHDInsightCluster</span></span>

## <span data-ttu-id="b05b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b05b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b05b4-103">Väljer ett HDInsight-kluster för den Invoke-AzureHDInsightHiveJob-cmdlet som ska användas för att skicka jobb.</span><span class="sxs-lookup"><span data-stu-id="b05b4-103">Selects an HDInsight cluster for the Invoke-AzureHDInsightHiveJob cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="b05b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b05b4-104">SYNTAX</span></span>

```
Use-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b05b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b05b4-105">DESCRIPTION</span></span>
<span data-ttu-id="b05b4-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="b05b4-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="b05b4-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="b05b4-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="b05b4-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b05b4-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="b05b4-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="b05b4-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="b05b4-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="b05b4-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="b05b4-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b05b4-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="b05b4-112">Cmdleten **use-AzureHDInsightCluster** väljer Azure HDInsight-klustret för cmdleten **Invoke-AzureHDInsightHiveJob** för att skicka jobb.</span><span class="sxs-lookup"><span data-stu-id="b05b4-112">The **Use-AzureHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the **Invoke-AzureHDInsightHiveJob** cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="b05b4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b05b4-113">EXAMPLES</span></span>

## <span data-ttu-id="b05b4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b05b4-114">PARAMETERS</span></span>

### <span data-ttu-id="b05b4-115">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="b05b4-115">-Certificate</span></span>
<span data-ttu-id="b05b4-116">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b05b4-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="b05b4-117">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="b05b4-117">-Endpoint</span></span>
<span data-ttu-id="b05b4-118">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="b05b4-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="b05b4-119">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="b05b4-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="b05b4-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="b05b4-120">-HostedService</span></span>
<span data-ttu-id="b05b4-121">Anger namn området för en HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="b05b4-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="b05b4-122">Om du inte anger den här parametern används standard namn området.</span><span class="sxs-lookup"><span data-stu-id="b05b4-122">If you do not specify this parameter, the default namespace is used.</span></span>

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

### <span data-ttu-id="b05b4-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="b05b4-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="b05b4-124">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="b05b4-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="b05b4-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="b05b4-125">-Name</span></span>
<span data-ttu-id="b05b4-126">Anger namnet på det kluster som används av cmdleten **Invoke-AzureHDInsightHiveJob** .</span><span class="sxs-lookup"><span data-stu-id="b05b4-126">Specifies the name of the cluster that is used by the **Invoke-AzureHDInsightHiveJob** cmdlet.</span></span>

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

### <span data-ttu-id="b05b4-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="b05b4-127">-Profile</span></span>
<span data-ttu-id="b05b4-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b05b4-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b05b4-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b05b4-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b05b4-130">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="b05b4-130">-Subscription</span></span>
<span data-ttu-id="b05b4-131">Anger den prenumeration som innehåller de HDInsight-kluster som ska användas.</span><span class="sxs-lookup"><span data-stu-id="b05b4-131">Specifies the subscription that contains the HDInsight clusters to use.</span></span>

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

### <span data-ttu-id="b05b4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05b4-132">CommonParameters</span></span>
<span data-ttu-id="b05b4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b05b4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05b4-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b05b4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05b4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b05b4-135">INPUTS</span></span>

## <span data-ttu-id="b05b4-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b05b4-136">OUTPUTS</span></span>

## <span data-ttu-id="b05b4-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b05b4-137">NOTES</span></span>

## <span data-ttu-id="b05b4-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b05b4-138">RELATED LINKS</span></span>

[<span data-ttu-id="b05b4-139">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b05b4-139">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="b05b4-140">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b05b4-140">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="b05b4-141">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b05b4-141">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)


