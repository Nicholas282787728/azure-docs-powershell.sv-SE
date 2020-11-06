---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: b10fe80fb0a58267212912f554d044b2715fd1d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576998"
---
# <span data-ttu-id="20ed1-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="20ed1-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="20ed1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20ed1-102">SYNOPSIS</span></span>
<span data-ttu-id="20ed1-103">Skapar ett Azure HDInsight-kluster i den angivna resurs gruppen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="20ed1-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20ed1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20ed1-104">SYNTAX</span></span>

### <span data-ttu-id="20ed1-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="20ed1-105">Default (Default)</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20ed1-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="20ed1-106">CertificateFilePath</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20ed1-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="20ed1-107">CertificateFileContents</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20ed1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20ed1-108">DESCRIPTION</span></span>
<span data-ttu-id="20ed1-109">New-AzureHDInsightCluster skapar ett Azure HDInsight-kluster med de angivna parametrarna eller med hjälp av ett konfigurations objekt som skapas med hjälp av cmdleten för New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="20ed1-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="20ed1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20ed1-110">EXAMPLES</span></span>

### <span data-ttu-id="20ed1-111">Exempel 1: skapa ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="20ed1-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightCluster `
            -ClusterType Hadoop `
            -OSType Windows `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="20ed1-112">Det här kommandot skapar ett kluster i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="20ed1-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="20ed1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20ed1-113">PARAMETERS</span></span>

### <span data-ttu-id="20ed1-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="20ed1-114">-AadTenantId</span></span>
<span data-ttu-id="20ed1-115">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20ed1-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="20ed1-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="20ed1-117">Anger ytterligare Azure Storage-konton för klustret.</span><span class="sxs-lookup"><span data-stu-id="20ed1-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="20ed1-118">Du kan också använda Add-AzureRmHDInsightStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-118">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="20ed1-119">-CertificateFileContents</span></span>
<span data-ttu-id="20ed1-120">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20ed1-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="20ed1-121">-CertificateFilePath</span></span>
<span data-ttu-id="20ed1-122">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="20ed1-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="20ed1-123">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20ed1-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="20ed1-124">-CertificatePassword</span></span>
<span data-ttu-id="20ed1-125">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="20ed1-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="20ed1-126">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20ed1-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-127">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="20ed1-127">-ClusterName</span></span>
<span data-ttu-id="20ed1-128">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="20ed1-128">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="20ed1-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="20ed1-130">Anger antalet arbets noder för klustret.</span><span class="sxs-lookup"><span data-stu-id="20ed1-130">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="20ed1-131">-ClusterTier</span></span>
<span data-ttu-id="20ed1-132">Anger HDInsight-klustrets nivå.</span><span class="sxs-lookup"><span data-stu-id="20ed1-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="20ed1-133">Detta är vanligt vis standard.</span><span class="sxs-lookup"><span data-stu-id="20ed1-133">By default, this is Standard.</span></span>
<span data-ttu-id="20ed1-134">Premium-nivån kan bara användas med Linux-kluster och det gör att du kan använda några nya funktioner.</span><span class="sxs-lookup"><span data-stu-id="20ed1-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="20ed1-135">-ClusterType</span></span>
<span data-ttu-id="20ed1-136">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="20ed1-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="20ed1-137">Alternativen är: Hadoop, HBase, Storm, Spark</span><span class="sxs-lookup"><span data-stu-id="20ed1-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="20ed1-138">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-139">-Config</span><span class="sxs-lookup"><span data-stu-id="20ed1-139">-Config</span></span>
<span data-ttu-id="20ed1-140">Anger vilket kluster objekt som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="20ed1-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="20ed1-141">Du kan skapa det här objektet med hjälp av New-AzureRmHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-141">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-142">-Konfigurationer</span><span class="sxs-lookup"><span data-stu-id="20ed1-142">-Configurations</span></span>
<span data-ttu-id="20ed1-143">Anger konfigurationerna för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="20ed1-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="20ed1-144">Du kan också använda Add-AzureRmHDInsightConfigValues cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-144">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ed1-145">-DefaultProfile</span></span>
<span data-ttu-id="20ed1-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="20ed1-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="20ed1-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="20ed1-148">Anger den konto nycklar för standard kontot för Azure Storage som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="20ed1-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="20ed1-149">Du kan också använda Set-AzureRmHDInsightDefaultStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-149">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="20ed1-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="20ed1-151">Anger namnet på det standardiserade Azure Storage-kontot som HDInsight-klustret ska använda.</span><span class="sxs-lookup"><span data-stu-id="20ed1-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="20ed1-152">Du kan också använda Set-AzureRmHDInsightDefaultStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-152">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="20ed1-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="20ed1-154">Anger typen för det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="20ed1-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="20ed1-155">Möjliga värden är AzureStorage och AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="20ed1-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="20ed1-156">Standardvärdet är AzureStorage om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="20ed1-156">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="20ed1-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="20ed1-158">Anger namnet på standard behållaren i det standardiserade Azure Storage-kontot som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="20ed1-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="20ed1-159">Du kan också använda Set-AzureRmHDInsightDefaultStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-159">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="20ed1-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="20ed1-161">Anger sökvägen-prefix i data Lake Store-kontot som HDInsight-klustret ska använda som standard fil system.</span><span class="sxs-lookup"><span data-stu-id="20ed1-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="20ed1-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="20ed1-163">Anger antalet diskar för rollen arbets tagare i klustret.</span><span class="sxs-lookup"><span data-stu-id="20ed1-163">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="20ed1-164">-EdgeNodeSize</span></span>
<span data-ttu-id="20ed1-165">Anger storleken på den virtuella datorn för noden Edge.</span><span class="sxs-lookup"><span data-stu-id="20ed1-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="20ed1-166">Använd Get-AzureRmVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="20ed1-166">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="20ed1-167">Den här parametern är endast giltig för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="20ed1-167">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="20ed1-168">-HeadNodeSize</span></span>
<span data-ttu-id="20ed1-169">Anger storleken på den virtuella datorn för Head-noden.</span><span class="sxs-lookup"><span data-stu-id="20ed1-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="20ed1-170">Använd Get-AzureRmVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="20ed1-170">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="20ed1-171">-HiveMetastore</span></span>
<span data-ttu-id="20ed1-172">Anger SQL-databasen där registrerings data för metadata lagras.</span><span class="sxs-lookup"><span data-stu-id="20ed1-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="20ed1-173">Du kan också använda Add-AzureRmHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-173">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="20ed1-174">-HttpCredential</span></span>
<span data-ttu-id="20ed1-175">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="20ed1-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-176">-Plats</span><span class="sxs-lookup"><span data-stu-id="20ed1-176">-Location</span></span>
<span data-ttu-id="20ed1-177">Anger platsen för klustret.</span><span class="sxs-lookup"><span data-stu-id="20ed1-177">Specifies the location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="20ed1-178">-ObjectId</span></span>
<span data-ttu-id="20ed1-179">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="20ed1-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="20ed1-180">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20ed1-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="20ed1-181">-OozieMetastore</span></span>
<span data-ttu-id="20ed1-182">Anger den SQL-databas där Oozie metadata ska lagras.</span><span class="sxs-lookup"><span data-stu-id="20ed1-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="20ed1-183">Du kan också använda Add-AzureRmHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-183">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="20ed1-184">-OSType</span></span>
<span data-ttu-id="20ed1-185">Anger klustrets operativ system.</span><span class="sxs-lookup"><span data-stu-id="20ed1-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="20ed1-186">Alternativen är: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="20ed1-186">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="20ed1-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="20ed1-188">Anger förfallo datum, som ett DateTime-objekt, för RDP-åtkomst (Remote Desktop Protocol) till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="20ed1-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="20ed1-189">-RdpCredential</span></span>
<span data-ttu-id="20ed1-190">Anger autentiseringsuppgifter för fjärr skrivbord (RDP) för klustret.</span><span class="sxs-lookup"><span data-stu-id="20ed1-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="20ed1-191">Det här är endast för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="20ed1-191">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ed1-192">-ResourceGroupName</span></span>
<span data-ttu-id="20ed1-193">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="20ed1-193">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="20ed1-194">-ScriptActions</span></span>
<span data-ttu-id="20ed1-195">Anger skript åtgärderna som ska köras på klustret när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="20ed1-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="20ed1-196">Du kan också använda Add-AzureRmHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="20ed1-196">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="20ed1-197">-SecurityProfile</span></span>
<span data-ttu-id="20ed1-198">Anger säkerhetsrelaterade egenskaper som används för att skapa ett säkert kluster.</span><span class="sxs-lookup"><span data-stu-id="20ed1-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="20ed1-199">Du kan också använda Add-AzureRmHDInsightSecurityProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-199">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="20ed1-200">-SshCredential</span></span>
<span data-ttu-id="20ed1-201">Anger SSH-autentiseringsuppgiften som ska användas för SSH-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="20ed1-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="20ed1-202">Det här är endast för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="20ed1-202">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="20ed1-203">-SshPublicKey</span></span>
<span data-ttu-id="20ed1-204">Anger den offentliga nycklar som ska användas för SSH-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="20ed1-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="20ed1-205">Det här är endast för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="20ed1-205">This is only for Linux clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="20ed1-206">-SubnetName</span></span>
<span data-ttu-id="20ed1-207">Anger namnet på ett under nätverk i det valda virtuella nätverket för klustret.</span><span class="sxs-lookup"><span data-stu-id="20ed1-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-208">-Version</span><span class="sxs-lookup"><span data-stu-id="20ed1-208">-Version</span></span>
<span data-ttu-id="20ed1-209">Anger HDI-versionen för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="20ed1-209">Specifies the HDI version of the HDInsight cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="20ed1-210">-VirtualNetworkId</span></span>
<span data-ttu-id="20ed1-211">Anger ID för det virtuella nätverk som du vill etablera klustret med.</span><span class="sxs-lookup"><span data-stu-id="20ed1-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="20ed1-212">-WorkerNodeSize</span></span>
<span data-ttu-id="20ed1-213">Anger storleken på den virtuella datorn för arbets tagaren.</span><span class="sxs-lookup"><span data-stu-id="20ed1-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="20ed1-214">Använd Get-AzureRmVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="20ed1-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="20ed1-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="20ed1-216">Anger storleken på den virtuella datorn för noden Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="20ed1-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="20ed1-217">Använd Get-AzureRmVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="20ed1-217">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="20ed1-218">Denna parameter är endast giltig för HBase-och Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="20ed1-218">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ed1-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ed1-219">CommonParameters</span></span>
<span data-ttu-id="20ed1-220">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20ed1-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ed1-221">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20ed1-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ed1-222">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20ed1-222">INPUTS</span></span>

### <span data-ttu-id="20ed1-223">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="20ed1-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="20ed1-224">Parametrar: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="20ed1-224">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="20ed1-225">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20ed1-225">OUTPUTS</span></span>

### <span data-ttu-id="20ed1-226">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="20ed1-226">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="20ed1-227">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20ed1-227">NOTES</span></span>
<span data-ttu-id="20ed1-228">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Hadoop, HDInsight, HD, insikt</span><span class="sxs-lookup"><span data-stu-id="20ed1-228">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="20ed1-229">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20ed1-229">RELATED LINKS</span></span>

[<span data-ttu-id="20ed1-230">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="20ed1-230">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

