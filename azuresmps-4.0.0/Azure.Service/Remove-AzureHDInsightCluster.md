---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 7D73D37B-17EE-4FF8-9A21-D2014D5417D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa779907648ca8e8e1288394d562c86b6102d9ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099706"
---
# <span data-ttu-id="70808-101">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="70808-101">Remove-AzureHDInsightCluster</span></span>

## <span data-ttu-id="70808-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70808-102">SYNOPSIS</span></span>
<span data-ttu-id="70808-103">Tar bort ett HDInsight-kluster från en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="70808-103">Deletes an HDInsight cluster from a subscription.</span></span>

## <span data-ttu-id="70808-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70808-104">SYNTAX</span></span>

```
Remove-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="70808-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70808-105">DESCRIPTION</span></span>
<span data-ttu-id="70808-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="70808-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="70808-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="70808-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="70808-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70808-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="70808-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="70808-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="70808-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="70808-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="70808-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="70808-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="70808-112">Cmdleten **Remove-AzureHDInsightCluster** tar bort angivet HDInsight-serverkluster från ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="70808-112">The **Remove-AzureHDInsightCluster** cmdlet deletes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="70808-113">Den här åtgärden tar också bort data som lagrats i HDFS (Hadoop Distributed File System) i klustret.</span><span class="sxs-lookup"><span data-stu-id="70808-113">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="70808-114">Data som lagras i det associerade Azure Storage-kontot tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="70808-114">Data stored in the associated Azure Storage account is not deleted.</span></span>

## <span data-ttu-id="70808-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70808-115">EXAMPLES</span></span>

### <span data-ttu-id="70808-116">Exempel 1: ta bort ett kluster</span><span class="sxs-lookup"><span data-stu-id="70808-116">Example 1: Remove a cluster</span></span>
```
PS C:\>Remove-AzureHDInsightCluster -Name "HDICluster"
```

<span data-ttu-id="70808-117">Det här kommandot tar bort HDInsight-klustret med namnet HDICluster.</span><span class="sxs-lookup"><span data-stu-id="70808-117">This command deletes the HDInsight cluster named HDICluster.</span></span>

## <span data-ttu-id="70808-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70808-118">PARAMETERS</span></span>

### <span data-ttu-id="70808-119">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="70808-119">-Certificate</span></span>
<span data-ttu-id="70808-120">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="70808-120">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="70808-121">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="70808-121">-Endpoint</span></span>
<span data-ttu-id="70808-122">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="70808-122">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="70808-123">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="70808-123">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="70808-124">-HostedService</span><span class="sxs-lookup"><span data-stu-id="70808-124">-HostedService</span></span>
<span data-ttu-id="70808-125">Anger namn området för en HDInsight-tjänst om du inte vill använda standard namn området.</span><span class="sxs-lookup"><span data-stu-id="70808-125">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="70808-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="70808-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="70808-127">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="70808-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="70808-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="70808-128">-Name</span></span>
<span data-ttu-id="70808-129">Anger namnet på HDInsight-klustret som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="70808-129">Specifies the name of the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="70808-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="70808-130">-Profile</span></span>
<span data-ttu-id="70808-131">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="70808-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="70808-132">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="70808-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="70808-133">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="70808-133">-Subscription</span></span>
<span data-ttu-id="70808-134">Anger det abonnemang som innehåller HDInsight-klustret som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="70808-134">Specifies the subscription account that contains the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="70808-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70808-135">CommonParameters</span></span>
<span data-ttu-id="70808-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70808-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70808-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70808-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70808-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70808-138">INPUTS</span></span>

## <span data-ttu-id="70808-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70808-139">OUTPUTS</span></span>

## <span data-ttu-id="70808-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70808-140">NOTES</span></span>

## <span data-ttu-id="70808-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70808-141">RELATED LINKS</span></span>

[<span data-ttu-id="70808-142">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="70808-142">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="70808-143">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="70808-143">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="70808-144">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="70808-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


