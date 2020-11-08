---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099153"
---
# <span data-ttu-id="96896-101">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="96896-101">New-AzureHDInsightCluster</span></span>

## <span data-ttu-id="96896-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96896-102">SYNOPSIS</span></span>
<span data-ttu-id="96896-103">Skapar ett HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="96896-103">Creates an HDInsight cluster.</span></span>

## <span data-ttu-id="96896-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96896-104">SYNTAX</span></span>

### <span data-ttu-id="96896-105">Cluster by config (med specifik prenumerations uppgifter) (standard)</span><span class="sxs-lookup"><span data-stu-id="96896-105">Cluster By Config (with Specific Subscription Credential) (Default)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="96896-106">Kluster efter namn (med specifik prenumerations uppgifter)</span><span class="sxs-lookup"><span data-stu-id="96896-106">Cluster By Name (with Specific Subscription Credential)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="96896-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96896-107">DESCRIPTION</span></span>
<span data-ttu-id="96896-108">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="96896-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="96896-109">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="96896-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="96896-110">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="96896-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="96896-111">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="96896-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="96896-112">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="96896-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="96896-113">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="96896-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="96896-114">Cmdleten **New-AzureHDInsightCluster** skapar ett Azure HDInsight-kluster med hjälp av de angivna parametrarna eller genom att använda ett konfigurations objekt som skapas med cmdleten **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="96896-114">The **New-AzureHDInsightCluster** cmdlet creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

## <span data-ttu-id="96896-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96896-115">EXAMPLES</span></span>

### <span data-ttu-id="96896-116">Exempel 1: skapa ett HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="96896-116">Example 1: Create an HDInsight cluster</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential 
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="96896-117">I det här exemplet skapas ett HDInsight-kluster för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="96896-117">This example creates an HDInsight cluster for the current subscription.</span></span>

<span data-ttu-id="96896-118">I det första kommandot används cmdleten **Get-AzureSubscription** för att hämta aktuellt ABONNEMANGS-ID och det sparas sedan i $SubId variabel.</span><span class="sxs-lookup"><span data-stu-id="96896-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="96896-119">I det andra och tredje kommandot används cmdleten **Get-AzureStorageKey** för att hämta primär lagrings nycklar för MyBlobStorage och MySecondBlobStorage, och sedan sparas nycklarna i $Key 1-och $Key 2-variabler.</span><span class="sxs-lookup"><span data-stu-id="96896-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="96896-120">De fjärde, femte och sjätte kommandona använder cmdleten **Get-Credential** för att få autentiseringsuppgifter för det aktuella abonnemanget och för Oozie och Hive och sedan lagra autentiseringsuppgifterna i variabler.</span><span class="sxs-lookup"><span data-stu-id="96896-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="96896-121">Det slutliga kommandot utför en sekvens med operationer genom att använda dessa cmdletar:</span><span class="sxs-lookup"><span data-stu-id="96896-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="96896-122">**New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="96896-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="96896-123">**Set-AzureHDInsightDefaultStorage** för att ange standard lagrings kontot för konfigurationen till MyBlobStorage.blob.Core.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="96896-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="96896-124">**Add-AzureHDInsightStorage** om du vill lägga till ett andra lagrings konto med namnet MySecondBlobStorage.blob.Core.Windows.net i konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="96896-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="96896-125">**Add-AzureHDInsightMetastore** om du vill lägga till en metastore för Oozie och en metastore för struktur till konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="96896-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="96896-126">**New-AzureHDInsightCluster** för att skapa ett HDInsight-kluster med den nya konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="96896-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="96896-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96896-127">PARAMETERS</span></span>

### <span data-ttu-id="96896-128">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="96896-128">-Certificate</span></span>
<span data-ttu-id="96896-129">Anger hanterings certifikatet för en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="96896-129">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="96896-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="96896-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="96896-131">Anger hur många datanoder som ska skapas för ett kluster.</span><span class="sxs-lookup"><span data-stu-id="96896-131">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-132">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="96896-132">-ClusterType</span></span>
<span data-ttu-id="96896-133">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="96896-133">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-134">-Config</span><span class="sxs-lookup"><span data-stu-id="96896-134">-Config</span></span>
<span data-ttu-id="96896-135">Anger ett konfigurations objekt som skapas med cmdleten **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="96896-135">Specifies a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96896-136">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="96896-136">-Credential</span></span>
<span data-ttu-id="96896-137">Anger de användarautentiseringsuppgifter för HDInsight som ska användas för standard kontot som används för att fjärrans luta till ett Hadoop-kluster.</span><span class="sxs-lookup"><span data-stu-id="96896-137">Specifies the user credentials for HDInsight to use for the default account that is used to remotely access a Hadoop cluster.</span></span>
<span data-ttu-id="96896-138">Dessa autentiseringsuppgifter skiljer sig från användarens autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="96896-138">These credentials are distinct from the subscription credentials of the user.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-139">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="96896-139">-DataNodeVMSize</span></span>
<span data-ttu-id="96896-140">Anger storleken på den virtuella datorn för datanoden.</span><span class="sxs-lookup"><span data-stu-id="96896-140">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="96896-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="96896-142">Anger konto nycklar för det standard lagrings konto som HDInsight-klustret använder.</span><span class="sxs-lookup"><span data-stu-id="96896-142">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="96896-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="96896-144">Anger namnet på det standard lagrings konto som HDInsight-klustret använder.</span><span class="sxs-lookup"><span data-stu-id="96896-144">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-145">-DefaultStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="96896-145">-DefaultStorageContainerName</span></span>
<span data-ttu-id="96896-146">Anger namnet på standard behållaren i det standardiserade Azure Storage-kontot som ett HDInsight-kluster använder.</span><span class="sxs-lookup"><span data-stu-id="96896-146">Specifies the name of the default container in the default Azure storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-147">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="96896-147">-EndPoint</span></span>
<span data-ttu-id="96896-148">Anger slut punkten som används för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="96896-148">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="96896-149">Om du inte anger den här parametern använder denna cmdlet standard slut punkten.</span><span class="sxs-lookup"><span data-stu-id="96896-149">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="96896-150">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="96896-150">-HeadNodeVMSize</span></span>
<span data-ttu-id="96896-151">Anger storleken på den virtuella datorn för Head-noden.</span><span class="sxs-lookup"><span data-stu-id="96896-151">Specifies the size of the virtual machine for the head node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-152">-HostedService</span><span class="sxs-lookup"><span data-stu-id="96896-152">-HostedService</span></span>
<span data-ttu-id="96896-153">Anger namn området för en HDInsight-tjänst.</span><span class="sxs-lookup"><span data-stu-id="96896-153">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="96896-154">Om du inte anger den här parametern använder denna cmdlet standard namn området.</span><span class="sxs-lookup"><span data-stu-id="96896-154">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="96896-155">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="96896-155">-IgnoreSslErrors</span></span>
<span data-ttu-id="96896-156">Anger om SSL-fel (Secure Sockets Layer) ignoreras.</span><span class="sxs-lookup"><span data-stu-id="96896-156">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="96896-157">-Plats</span><span class="sxs-lookup"><span data-stu-id="96896-157">-Location</span></span>
<span data-ttu-id="96896-158">Anger den region som du vill skapa ett HDInsight-kluster för.</span><span class="sxs-lookup"><span data-stu-id="96896-158">Specifies the region in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-159">-Namn</span><span class="sxs-lookup"><span data-stu-id="96896-159">-Name</span></span>
<span data-ttu-id="96896-160">Anger namnet på Azure HDInsight-klustret som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="96896-160">Specifies the name of the Azure HDInsight cluster to create.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-161">-OSType</span><span class="sxs-lookup"><span data-stu-id="96896-161">-OSType</span></span>
<span data-ttu-id="96896-162">Anger operativ system för ett kluster.</span><span class="sxs-lookup"><span data-stu-id="96896-162">Specifies the operating system for a cluster.</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-163">-Profil</span><span class="sxs-lookup"><span data-stu-id="96896-163">-Profile</span></span>
<span data-ttu-id="96896-164">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="96896-164">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="96896-165">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="96896-165">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="96896-166">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="96896-166">-RdpAccessExpiry</span></span>
<span data-ttu-id="96896-167">Anger förfallo datum, som ett **datetime** -objekt, för RDP-åtkomst (Remote Desktop Protocol) till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="96896-167">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-168">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="96896-168">-RdpCredential</span></span>
<span data-ttu-id="96896-169">Anger autentiseringsuppgifter för RDP-åtkomst till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="96896-169">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-170">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="96896-170">-SshCredential</span></span>
<span data-ttu-id="96896-171">Anger det säkra gränssnittets användar namn och lösen ord för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="96896-171">Specifies the Secure Shell (SSH) user name and password for the HDInsight cluster.</span></span>
<span data-ttu-id="96896-172">Den här parametern är endast giltig för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="96896-172">This parameter is valid only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-173">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="96896-173">-SshPublicKey</span></span>
<span data-ttu-id="96896-174">Anger den offentliga SSH-tangenten för ett HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="96896-174">Specifies the SSH public key for an HDInsight cluster.</span></span>
<span data-ttu-id="96896-175">Den här parametern är endast giltig för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="96896-175">This parameter is valid only for Linux clusters.</span></span>

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

### <span data-ttu-id="96896-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="96896-176">-SubnetName</span></span>
<span data-ttu-id="96896-177">Anger namnet på ett undernät.</span><span class="sxs-lookup"><span data-stu-id="96896-177">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-178">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="96896-178">-Subscription</span></span>
<span data-ttu-id="96896-179">Anger den Azure-prenumeration som du vill skapa ett HDInsight-kluster för.</span><span class="sxs-lookup"><span data-stu-id="96896-179">Specifies the Azure subscription in which to create an HDInsight cluster.</span></span>

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

### <span data-ttu-id="96896-180">-Version</span><span class="sxs-lookup"><span data-stu-id="96896-180">-Version</span></span>
<span data-ttu-id="96896-181">Anger vilken HDInsight-kluster version som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="96896-181">Specifies the HDInsight cluster version to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-182">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="96896-182">-VirtualNetworkId</span></span>
<span data-ttu-id="96896-183">Anger ID för det virtuella nätverk som du vill etablera klustret med.</span><span class="sxs-lookup"><span data-stu-id="96896-183">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-184">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="96896-184">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="96896-185">Anger storleken på den virtuella datorn för noden ZooKeeper.</span><span class="sxs-lookup"><span data-stu-id="96896-185">Specifies the size of the virtual machine for the ZooKeeper node.</span></span>
<span data-ttu-id="96896-186">Denna parameter är endast giltig för HBase-och Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="96896-186">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96896-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96896-187">CommonParameters</span></span>
<span data-ttu-id="96896-188">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96896-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96896-189">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96896-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96896-190">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96896-190">INPUTS</span></span>

## <span data-ttu-id="96896-191">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96896-191">OUTPUTS</span></span>

## <span data-ttu-id="96896-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96896-192">NOTES</span></span>

## <span data-ttu-id="96896-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96896-193">RELATED LINKS</span></span>

[<span data-ttu-id="96896-194">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="96896-194">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="96896-195">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="96896-195">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="96896-196">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="96896-196">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="96896-197">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="96896-197">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="96896-198">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="96896-198">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="96896-199">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="96896-199">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)

[<span data-ttu-id="96896-200">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="96896-200">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


