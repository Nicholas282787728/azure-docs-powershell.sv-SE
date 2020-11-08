---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 325DE85D-B9CB-4584-8C61-DA417736ABBF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55992408c1376c9456157387456b114c292b44c2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099581"
---
# <span data-ttu-id="86083-101">Get-AzureHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="86083-101">Get-AzureHDInsightProperties</span></span>

## <span data-ttu-id="86083-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86083-102">SYNOPSIS</span></span>
<span data-ttu-id="86083-103">Hämtar egenskaper som är specifika för en HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="86083-103">Gets properties specific to an HDInsight service.</span></span>

## <span data-ttu-id="86083-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86083-104">SYNTAX</span></span>

```
Get-AzureHDInsightProperties [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Locations] [-Subscription <String>] [-Versions] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="86083-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86083-105">DESCRIPTION</span></span>
<span data-ttu-id="86083-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="86083-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="86083-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="86083-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="86083-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="86083-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="86083-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="86083-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="86083-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="86083-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="86083-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="86083-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="86083-112">Cmdleten **Get-AzureHDInsightProperties** hämtar egenskaper som är specifika för en Azure HDInsight-tjänst, till exempel en lista över tillgängliga Azure-regioner, HDInsight-kluster versioner och tillgänglig beräknings kapacitet.</span><span class="sxs-lookup"><span data-stu-id="86083-112">The **Get-AzureHDInsightProperties** cmdlet gets properties specific to an Azure HDInsight service, such as a list of available Azure regions, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="86083-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86083-113">EXAMPLES</span></span>

### <span data-ttu-id="86083-114">Exempel 1: Hämta HDInsight-egenskaper för en prenumeration</span><span class="sxs-lookup"><span data-stu-id="86083-114">Example 1: Get HDInsight properties for a subscription</span></span>
```
PS C:\>$SubName = Get-AzureSubscription -Current | %{ $_.SubscriptionName }
PS C:\> Get-AzureHDInsightProperties -Subscription $SubName
```

<span data-ttu-id="86083-115">Det första kommandot får namnet på det aktuella Azure-abonnemanget och lagrar det sedan i $SubName variabel.</span><span class="sxs-lookup"><span data-stu-id="86083-115">The first command gets the name of the current Azure subscription, and then stores it in the $SubName variable.</span></span>

<span data-ttu-id="86083-116">Det andra kommandot får HDInsight-egenskaperna för prenumerationen i $SubName.</span><span class="sxs-lookup"><span data-stu-id="86083-116">The second command gets the HDInsight properties for the subscription in $SubName.</span></span>

## <span data-ttu-id="86083-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86083-117">PARAMETERS</span></span>

### <span data-ttu-id="86083-118">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="86083-118">-Certificate</span></span>
<span data-ttu-id="86083-119">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="86083-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="86083-120">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="86083-120">-Endpoint</span></span>
<span data-ttu-id="86083-121">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="86083-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="86083-122">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="86083-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="86083-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="86083-123">-HostedService</span></span>
<span data-ttu-id="86083-124">Anger namn området för en HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="86083-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="86083-125">Om du inte anger den här parametern använder denna cmdlet standard namn området.</span><span class="sxs-lookup"><span data-stu-id="86083-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="86083-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="86083-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="86083-127">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="86083-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="86083-128">-Platser</span><span class="sxs-lookup"><span data-stu-id="86083-128">-Locations</span></span>
<span data-ttu-id="86083-129">Anger att denna cmdlet hämtar listan med Azure-regioner där HDInsight-tjänsten är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="86083-129">Indicates that this cmdlet gets the list of Azure regions where the HDInsight service is available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86083-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="86083-130">-Profile</span></span>
<span data-ttu-id="86083-131">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="86083-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86083-132">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="86083-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86083-133">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="86083-133">-Subscription</span></span>
<span data-ttu-id="86083-134">Anger det abonnemang som innehåller de HDInsight-egenskaper du kan hämta.</span><span class="sxs-lookup"><span data-stu-id="86083-134">Specifies the subscription that contains the HDInsight properties to get.</span></span>

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

### <span data-ttu-id="86083-135">-Versioner</span><span class="sxs-lookup"><span data-stu-id="86083-135">-Versions</span></span>
<span data-ttu-id="86083-136">Anger att den här cmdleten får en lista över de HDInsight-kluster versioner som är tillgängliga i tjänsten för en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="86083-136">Indicates that this cmdlet gets the list of HDInsight cluster versions that are available in the service for a subscription.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86083-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86083-137">CommonParameters</span></span>
<span data-ttu-id="86083-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86083-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86083-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86083-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86083-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86083-140">INPUTS</span></span>

## <span data-ttu-id="86083-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86083-141">OUTPUTS</span></span>

## <span data-ttu-id="86083-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86083-142">NOTES</span></span>

## <span data-ttu-id="86083-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86083-143">RELATED LINKS</span></span>

