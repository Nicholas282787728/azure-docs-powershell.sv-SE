---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 771B7CB2-88F6-4FC5-9DB0-E623D231E51A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdbf7778ca2d7498d7f33586f7e9e50e0955c521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099192"
---
# <span data-ttu-id="7701b-101">Set-AzureHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="7701b-101">Set-AzureHDInsightClusterSize</span></span>

## <span data-ttu-id="7701b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7701b-102">SYNOPSIS</span></span>
<span data-ttu-id="7701b-103">Anger antalet datanoder för ett HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="7701b-103">Sets the number of data nodes for an HDInsight cluster.</span></span>

## <span data-ttu-id="7701b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7701b-104">SYNTAX</span></span>

### <span data-ttu-id="7701b-105">Ange kluster storlek i noder med namn.</span><span class="sxs-lookup"><span data-stu-id="7701b-105">Set cluster size in nodes with name.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> -Name <String> [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7701b-106">Ange kluster storlek i noder med kluster från pipeline.</span><span class="sxs-lookup"><span data-stu-id="7701b-106">Set cluster size in nodes with cluster from pipeline.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> [-Force] -Cluster <AzureHDInsightCluster>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7701b-107">Kluster efter namn (med specifik prenumerations uppgifter)</span><span class="sxs-lookup"><span data-stu-id="7701b-107">Cluster By Name (with Specific Subscription Credential)</span></span>
```
Set-AzureHDInsightClusterSize [-Certificate <X509Certificate2>] [-Subscription <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7701b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7701b-108">DESCRIPTION</span></span>
<span data-ttu-id="7701b-109">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="7701b-109">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="7701b-110">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="7701b-110">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="7701b-111">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7701b-111">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="7701b-112">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="7701b-112">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="7701b-113">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="7701b-113">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="7701b-114">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7701b-114">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="7701b-115">Cmdleten **set-AzureHDInsightClusterSize** anger antalet datanoder för ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="7701b-115">The **Set-AzureHDInsightClusterSize** cmdlet sets the number of data nodes for an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7701b-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7701b-116">EXAMPLES</span></span>

## <span data-ttu-id="7701b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7701b-117">PARAMETERS</span></span>

### <span data-ttu-id="7701b-118">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="7701b-118">-Certificate</span></span>
<span data-ttu-id="7701b-119">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="7701b-119">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7701b-120">-Kluster</span><span class="sxs-lookup"><span data-stu-id="7701b-120">-Cluster</span></span>
<span data-ttu-id="7701b-121">Anger vilket kluster du vill ändra storlek på.</span><span class="sxs-lookup"><span data-stu-id="7701b-121">Specifies the cluster to resize.</span></span>

```yaml
Type: AzureHDInsightCluster
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7701b-122">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="7701b-122">-ClusterSizeInNodes</span></span>
<span data-ttu-id="7701b-123">Anger hur många datanoder som ska skapas för ett kluster.</span><span class="sxs-lookup"><span data-stu-id="7701b-123">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with name.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7701b-124">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="7701b-124">-Endpoint</span></span>
<span data-ttu-id="7701b-125">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="7701b-125">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="7701b-126">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="7701b-126">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7701b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="7701b-127">-Force</span></span>
<span data-ttu-id="7701b-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7701b-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Set cluster size in nodes with name., Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7701b-129">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="7701b-129">-IgnoreSslErrors</span></span>
<span data-ttu-id="7701b-130">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="7701b-130">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7701b-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="7701b-131">-Name</span></span>
<span data-ttu-id="7701b-132">Anger namnet på HDInsight-klustret att ändra storlek på.</span><span class="sxs-lookup"><span data-stu-id="7701b-132">Specifies the name of the HDInsight cluster to resize.</span></span>

```yaml
Type: String
Parameter Sets: Set cluster size in nodes with name.
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7701b-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="7701b-133">-Profile</span></span>
<span data-ttu-id="7701b-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7701b-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7701b-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7701b-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7701b-136">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="7701b-136">-Subscription</span></span>
<span data-ttu-id="7701b-137">Anger ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="7701b-137">Specifies a subscription.</span></span>
<span data-ttu-id="7701b-138">Denna cmdlet anger kluster storleken för det abonnemang som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7701b-138">This cmdlet sets the cluster size for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7701b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7701b-139">CommonParameters</span></span>
<span data-ttu-id="7701b-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7701b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7701b-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7701b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7701b-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7701b-142">INPUTS</span></span>

## <span data-ttu-id="7701b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7701b-143">OUTPUTS</span></span>

## <span data-ttu-id="7701b-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7701b-144">NOTES</span></span>

## <span data-ttu-id="7701b-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7701b-145">RELATED LINKS</span></span>

