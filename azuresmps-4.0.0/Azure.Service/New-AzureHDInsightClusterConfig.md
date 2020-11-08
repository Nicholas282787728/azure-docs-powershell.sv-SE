---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF8AA7DE-1E0F-4F5B-95F6-7820AAF789F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: c36931af0b6927ef4fee26b9f8ade7db77d17db2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099150"
---
# <span data-ttu-id="8c275-101">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="8c275-101">New-AzureHDInsightClusterConfig</span></span>

## <span data-ttu-id="8c275-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c275-102">SYNOPSIS</span></span>
<span data-ttu-id="8c275-103">Skapar en icke beständig HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8c275-103">Creates a non-persisted HDInsight cluster configuration.</span></span>

## <span data-ttu-id="8c275-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c275-104">SYNTAX</span></span>

```
New-AzureHDInsightClusterConfig -ClusterSizeInNodes <Int32> [-HeadNodeVMSize <String>]
 [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>] [-DataNodeVMSize <String>]
 [-ZookeeperNodeVMSize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8c275-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c275-105">DESCRIPTION</span></span>
<span data-ttu-id="8c275-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="8c275-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="8c275-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="8c275-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="8c275-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8c275-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="8c275-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="8c275-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="8c275-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="8c275-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="8c275-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8c275-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="8c275-112">Cmdleten **New-AzureHDInsightClusterConfig** skapar en icke-beständig Azure HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8c275-112">The **New-AzureHDInsightClusterConfig** cmdlet creates a non-persisted Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="8c275-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c275-113">EXAMPLES</span></span>

### <span data-ttu-id="8c275-114">Exempel 1: skapa en kluster konfiguration</span><span class="sxs-lookup"><span data-stu-id="8c275-114">Example 1: Create a cluster configuration</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyBlobStorage.blob.core.windows.net -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="8c275-115">I det första kommandot används cmdleten **Get-AzureSubscription** för att hämta aktuellt ABONNEMANGS-ID och det sparas sedan i $SubId variabel.</span><span class="sxs-lookup"><span data-stu-id="8c275-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="8c275-116">I det andra och tredje kommandot används cmdleten **Get-AzureStorageKey** för att hämta primär lagrings nycklar för MyBlobStorage och MySecondBlobStorage, och sedan sparas nycklarna i $Key 1-och $Key 2-variabler.</span><span class="sxs-lookup"><span data-stu-id="8c275-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="8c275-117">De fjärde, femte och sjätte kommandona använder cmdleten **Get-Credential** för att få autentiseringsuppgifter för det aktuella abonnemanget och för Oozie och Hive och sedan lagra autentiseringsuppgifterna i variabler.</span><span class="sxs-lookup"><span data-stu-id="8c275-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="8c275-118">Det slutliga kommandot utför en sekvens med operationer genom att använda dessa cmdletar:</span><span class="sxs-lookup"><span data-stu-id="8c275-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="8c275-119">**New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8c275-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="8c275-120">**Set-AzureHDInsightDefaultStorage** för att ange standard lagrings kontot för konfigurationen till MyBlobStorage.blob.Core.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="8c275-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="8c275-121">**Add-AzureHDInsightStorage** om du vill lägga till ett andra lagrings konto med namnet MySecondBlobStorage.blob.Core.Windows.net i konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8c275-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="8c275-122">**Add-AzureHDInsightMetastore** om du vill lägga till en metastore för Oozie och en metastore för struktur till konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8c275-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="8c275-123">**New-AzureHDInsightCluster** för att skapa ett HDInsight-kluster med den nya konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8c275-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="8c275-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c275-124">PARAMETERS</span></span>

### <span data-ttu-id="8c275-125">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="8c275-125">-ClusterSizeInNodes</span></span>
<span data-ttu-id="8c275-126">Anger hur många datanoder som ska skapas för ett kluster.</span><span class="sxs-lookup"><span data-stu-id="8c275-126">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c275-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="8c275-127">-ClusterType</span></span>
<span data-ttu-id="8c275-128">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="8c275-128">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c275-129">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="8c275-129">-DataNodeVMSize</span></span>
<span data-ttu-id="8c275-130">Anger storleken på den virtuella datorn för datanoden.</span><span class="sxs-lookup"><span data-stu-id="8c275-130">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c275-131">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="8c275-131">-HeadNodeVMSize</span></span>
<span data-ttu-id="8c275-132">Anger den virtuella dator storleken på huvudnoden för klustret.</span><span class="sxs-lookup"><span data-stu-id="8c275-132">Specifies the virtual machine size of the head node for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c275-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="8c275-133">-Profile</span></span>
<span data-ttu-id="8c275-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="8c275-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c275-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="8c275-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c275-136">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="8c275-136">-SubnetName</span></span>
<span data-ttu-id="8c275-137">Anger namnet på ett undernät.</span><span class="sxs-lookup"><span data-stu-id="8c275-137">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c275-138">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8c275-138">-VirtualNetworkId</span></span>
<span data-ttu-id="8c275-139">Anger ID för det virtuella nätverk som du vill etablera klustret med.</span><span class="sxs-lookup"><span data-stu-id="8c275-139">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c275-140">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="8c275-140">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="8c275-141">Anger storleken på den virtuella datorn för ZooKeeper-noden för ett HBase-eller Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="8c275-141">Specifies the size of the virtual machine for the ZooKeeper node for an HBase or Storm cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c275-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c275-142">CommonParameters</span></span>
<span data-ttu-id="8c275-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c275-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c275-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c275-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c275-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c275-145">INPUTS</span></span>

## <span data-ttu-id="8c275-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c275-146">OUTPUTS</span></span>

## <span data-ttu-id="8c275-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c275-147">NOTES</span></span>

## <span data-ttu-id="8c275-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c275-148">RELATED LINKS</span></span>

[<span data-ttu-id="8c275-149">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="8c275-149">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="8c275-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="8c275-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="8c275-151">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8c275-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="8c275-152">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="8c275-152">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


