---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3B39F43D-E74A-441D-91BC-26C324C1EDF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d0ea12e873604360114b02bb89d9bde12c9e70e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093370"
---
# <span data-ttu-id="452d2-101">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="452d2-101">Get-AzureHDInsightCluster</span></span>

## <span data-ttu-id="452d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="452d2-102">SYNOPSIS</span></span>
<span data-ttu-id="452d2-103">Hämtar ett HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="452d2-103">Gets an HDInsight cluster.</span></span>

## <span data-ttu-id="452d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="452d2-104">SYNTAX</span></span>

```
Get-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="452d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="452d2-105">DESCRIPTION</span></span>
<span data-ttu-id="452d2-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="452d2-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="452d2-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="452d2-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="452d2-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="452d2-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="452d2-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="452d2-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="452d2-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="452d2-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="452d2-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="452d2-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="452d2-112">Cmdleten **Get-AzureHDInsightCluster** hämtar Azure HDInsight-tjänstens kluster för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="452d2-112">The **Get-AzureHDInsightCluster** cmdlet gets the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="452d2-113">Du kan använda parametern *Name* för att skaffa ett visst kluster.</span><span class="sxs-lookup"><span data-stu-id="452d2-113">You can use the *Name* parameter to get a specific cluster.</span></span>

## <span data-ttu-id="452d2-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="452d2-114">EXAMPLES</span></span>

### <span data-ttu-id="452d2-115">Exempel 1: skaffa klustret i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="452d2-115">Example 1: Get the clusters in a subscription</span></span>
```
PS C:\> Get-AzureHDInsightCluster
```

<span data-ttu-id="452d2-116">Med det här kommandot får du information om HDInsight-klustren i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="452d2-116">This command gets information about the HDInsight clusters in the current subscription.</span></span>

## <span data-ttu-id="452d2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="452d2-117">PARAMETERS</span></span>

### <span data-ttu-id="452d2-118">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="452d2-118">-Certificate</span></span>
<span data-ttu-id="452d2-119">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="452d2-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="452d2-120">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="452d2-120">-Endpoint</span></span>
<span data-ttu-id="452d2-121">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="452d2-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="452d2-122">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="452d2-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="452d2-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="452d2-123">-HostedService</span></span>
<span data-ttu-id="452d2-124">Anger namn området för en HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="452d2-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="452d2-125">Om du inte anger den här parametern använder denna cmdlet standard namn området.</span><span class="sxs-lookup"><span data-stu-id="452d2-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="452d2-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="452d2-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="452d2-127">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="452d2-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="452d2-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="452d2-128">-Name</span></span>
<span data-ttu-id="452d2-129">Anger namnet på ett HDInsight-kluster att hämta.</span><span class="sxs-lookup"><span data-stu-id="452d2-129">Specifies the name of an HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="452d2-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="452d2-130">-Profile</span></span>
<span data-ttu-id="452d2-131">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="452d2-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="452d2-132">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="452d2-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="452d2-133">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="452d2-133">-Subscription</span></span>
<span data-ttu-id="452d2-134">Anger den prenumeration som innehåller HDInsight-klustret att få.</span><span class="sxs-lookup"><span data-stu-id="452d2-134">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

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

### <span data-ttu-id="452d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="452d2-135">CommonParameters</span></span>
<span data-ttu-id="452d2-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="452d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="452d2-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="452d2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="452d2-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="452d2-138">INPUTS</span></span>

## <span data-ttu-id="452d2-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="452d2-139">OUTPUTS</span></span>

## <span data-ttu-id="452d2-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="452d2-140">NOTES</span></span>

## <span data-ttu-id="452d2-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="452d2-141">RELATED LINKS</span></span>

[<span data-ttu-id="452d2-142">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="452d2-142">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="452d2-143">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="452d2-143">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="452d2-144">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="452d2-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


