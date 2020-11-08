---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 9008cb1dba2c39a2c552b2395f4115ca50a17fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102310"
---
# <span data-ttu-id="aeead-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="aeead-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="aeead-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aeead-102">SYNOPSIS</span></span>
<span data-ttu-id="aeead-103">Skapar ett Azure HDInsight-kluster i den angivna resurs gruppen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="aeead-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="aeead-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aeead-104">SYNTAX</span></span>

### <span data-ttu-id="aeead-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="aeead-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>]
 [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aeead-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="aeead-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aeead-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="aeead-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aeead-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aeead-108">DESCRIPTION</span></span>
<span data-ttu-id="aeead-109">New-AzHDInsightCluster skapar ett Azure HDInsight-kluster med de angivna parametrarna eller med hjälp av ett konfigurations objekt som skapas med hjälp av cmdleten för New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="aeead-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="aeead-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aeead-110">EXAMPLES</span></span>

### <span data-ttu-id="aeead-111">Exempel 1: skapa ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="aeead-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="aeead-112">Det här kommandot skapar ett kluster i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="aeead-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="aeead-113">Exempel 2: skapa kluster med hanterad kryptering av nycklar</span><span class="sxs-lookup"><span data-stu-id="aeead-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"
        $clusterCreds = Get-Credential

        # Customer-managed Key info
        $assignedIdentity = "your-ami-resource-id"
        $encryptionKeyName = "new-key"
        $encryptionVaultUri = "https://MyKeyVault.vault.azure.net"
        $encryptionKeyVersion = "00000000000000000000000000000000"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Spark `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="aeead-114">Exempel 3: skapa ett Azure HDInsight-kluster som möjliggör kryptering i transit</span><span class="sxs-lookup"><span data-stu-id="aeead-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="aeead-115">Exempel 4: skapa ett Azure HDInsight-kluster med funktionen privat länk</span><span class="sxs-lookup"><span data-stu-id="aeead-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Virtual network info
        $virtualNetworkId="yourvnetresourceid"
        $subnetName="yoursubnetresourceid"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="aeead-116">Exempel 5: skapa ett Azure HDInsight-kluster som möjliggör kryptering på värden</span><span class="sxs-lookup"><span data-stu-id="aeead-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="aeead-117">Exempel 6: skapa ett Azure HDInsight-kluster som aktiverar Autoskala.</span><span class="sxs-lookup"><span data-stu-id="aeead-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create autoscale configuration
        $autoscaleConfiguration=New-AzHDInsightClusterAutoscaleConfiguration `
            -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

## <span data-ttu-id="aeead-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aeead-118">PARAMETERS</span></span>

### <span data-ttu-id="aeead-119">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="aeead-119">-AadTenantId</span></span>
<span data-ttu-id="aeead-120">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aeead-120">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="aeead-121">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="aeead-121">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="aeead-122">Anger ytterligare Azure Storage-konton för klustret.</span><span class="sxs-lookup"><span data-stu-id="aeead-122">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="aeead-123">Du kan också använda Add-AzHDInsightStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeead-123">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="aeead-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="aeead-124">-ApplicationId</span></span>
<span data-ttu-id="aeead-125">Hämtar eller anger tjänstens huvud program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="aeead-125">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="aeead-126">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="aeead-126">-AssignedIdentity</span></span>
<span data-ttu-id="aeead-127">Hämtar eller anger den tilldelade identiteten.</span><span class="sxs-lookup"><span data-stu-id="aeead-127">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="aeead-128">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="aeead-128">-AutoscaleConfiguration</span></span>
<span data-ttu-id="aeead-129">Hämtar eller anger den autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="aeead-129">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeead-130">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="aeead-130">-CertificateFileContents</span></span>
<span data-ttu-id="aeead-131">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aeead-131">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="aeead-132">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="aeead-132">-CertificateFilePath</span></span>
<span data-ttu-id="aeead-133">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="aeead-133">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="aeead-134">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aeead-134">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="aeead-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="aeead-135">-CertificatePassword</span></span>
<span data-ttu-id="aeead-136">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="aeead-136">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="aeead-137">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aeead-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="aeead-138">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="aeead-138">-ClusterName</span></span>
<span data-ttu-id="aeead-139">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="aeead-139">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="aeead-140">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="aeead-140">-ClusterSizeInNodes</span></span>
<span data-ttu-id="aeead-141">Anger antalet arbets noder för klustret.</span><span class="sxs-lookup"><span data-stu-id="aeead-141">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="aeead-142">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="aeead-142">-ClusterTier</span></span>
<span data-ttu-id="aeead-143">Anger HDInsight-klustrets nivå.</span><span class="sxs-lookup"><span data-stu-id="aeead-143">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="aeead-144">Detta är vanligt vis standard.</span><span class="sxs-lookup"><span data-stu-id="aeead-144">By default, this is Standard.</span></span>
<span data-ttu-id="aeead-145">Premium-nivån kan bara användas med Linux-kluster och det gör att du kan använda några nya funktioner.</span><span class="sxs-lookup"><span data-stu-id="aeead-145">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="aeead-146">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="aeead-146">-ClusterType</span></span>
<span data-ttu-id="aeead-147">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="aeead-147">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="aeead-148">Alternativen är: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka och RServer</span><span class="sxs-lookup"><span data-stu-id="aeead-148">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="aeead-149">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="aeead-149">-ComponentVersion</span></span>
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

### <span data-ttu-id="aeead-150">-Config</span><span class="sxs-lookup"><span data-stu-id="aeead-150">-Config</span></span>
<span data-ttu-id="aeead-151">Anger vilket kluster objekt som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="aeead-151">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="aeead-152">Du kan skapa det här objektet med hjälp av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeead-152">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="aeead-153">-Konfigurationer</span><span class="sxs-lookup"><span data-stu-id="aeead-153">-Configurations</span></span>
<span data-ttu-id="aeead-154">Anger konfigurationerna för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="aeead-154">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="aeead-155">Du kan också använda Add-AzHDInsightConfigValues cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeead-155">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="aeead-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeead-156">-DefaultProfile</span></span>
<span data-ttu-id="aeead-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aeead-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeead-158">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="aeead-158">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="aeead-159">Anger den konto nycklar för standard kontot för Azure Storage som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="aeead-159">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="aeead-160">Du kan också använda Set-AzHDInsightDefaultStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeead-160">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="aeead-161">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aeead-161">-DefaultStorageAccountName</span></span>
<span data-ttu-id="aeead-162">Anger namnet på det standardiserade Azure Storage-kontot som HDInsight-klustret ska använda.</span><span class="sxs-lookup"><span data-stu-id="aeead-162">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="aeead-163">Du kan också använda Set-AzHDInsightDefaultStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeead-163">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="aeead-164">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="aeead-164">-DefaultStorageAccountType</span></span>
<span data-ttu-id="aeead-165">Anger typen för det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="aeead-165">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="aeead-166">Möjliga värden är AzureStorage och AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="aeead-166">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="aeead-167">Standardvärdet är AzureStorage om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="aeead-167">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="aeead-168">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="aeead-168">-DefaultStorageContainer</span></span>
<span data-ttu-id="aeead-169">Anger namnet på standard behållaren i det standardiserade Azure Storage-kontot som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="aeead-169">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="aeead-170">Du kan också använda Set-AzHDInsightDefaultStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeead-170">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="aeead-171">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="aeead-171">-DefaultStorageRootPath</span></span>
<span data-ttu-id="aeead-172">Anger sökvägen-prefix i data Lake Store-kontot som HDInsight-klustret ska använda som standard fil system.</span><span class="sxs-lookup"><span data-stu-id="aeead-172">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="aeead-173">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="aeead-173">-DisksPerWorkerNode</span></span>
<span data-ttu-id="aeead-174">Anger antalet diskar för rollen arbets tagare i klustret.</span><span class="sxs-lookup"><span data-stu-id="aeead-174">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="aeead-175">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="aeead-175">-EdgeNodeSize</span></span>
<span data-ttu-id="aeead-176">Anger storleken på den virtuella datorn för noden Edge.</span><span class="sxs-lookup"><span data-stu-id="aeead-176">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="aeead-177">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="aeead-177">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="aeead-178">Den här parametern är endast giltig för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="aeead-178">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="aeead-179">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="aeead-179">-EncryptionAlgorithm</span></span>
<span data-ttu-id="aeead-180">Hämtar eller anger krypteringsalgoritmen.</span><span class="sxs-lookup"><span data-stu-id="aeead-180">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeead-181">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="aeead-181">-EncryptionAtHost</span></span>
<span data-ttu-id="aeead-182">Hämtar eller anger flaggan som anger om Aktivera kryptering på värden eller inte.</span><span class="sxs-lookup"><span data-stu-id="aeead-182">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeead-183">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="aeead-183">-EncryptionInTransit</span></span>
<span data-ttu-id="aeead-184">Hämtar eller anger flaggan som anger om Aktivera kryptering i transit eller inte.</span><span class="sxs-lookup"><span data-stu-id="aeead-184">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeead-185">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="aeead-185">-EncryptionKeyName</span></span>
<span data-ttu-id="aeead-186">Hämtar eller anger namnet på krypterings nycklar.</span><span class="sxs-lookup"><span data-stu-id="aeead-186">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="aeead-187">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="aeead-187">-EncryptionKeyVersion</span></span>
<span data-ttu-id="aeead-188">Hämtar eller anger krypterings huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="aeead-188">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="aeead-189">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="aeead-189">-EncryptionVaultUri</span></span>
<span data-ttu-id="aeead-190">Hämtar eller anger krypterings valv-URI.</span><span class="sxs-lookup"><span data-stu-id="aeead-190">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="aeead-191">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="aeead-191">-HeadNodeSize</span></span>
<span data-ttu-id="aeead-192">Anger storleken på den virtuella datorn för Head-noden.</span><span class="sxs-lookup"><span data-stu-id="aeead-192">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="aeead-193">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="aeead-193">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="aeead-194">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="aeead-194">-HiveMetastore</span></span>
<span data-ttu-id="aeead-195">Anger SQL-databasen där registrerings data för metadata lagras.</span><span class="sxs-lookup"><span data-stu-id="aeead-195">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="aeead-196">Du kan också använda Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeead-196">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="aeead-197">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="aeead-197">-HttpCredential</span></span>
<span data-ttu-id="aeead-198">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="aeead-198">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="aeead-199">-Plats</span><span class="sxs-lookup"><span data-stu-id="aeead-199">-Location</span></span>
<span data-ttu-id="aeead-200">Anger platsen för klustret.</span><span class="sxs-lookup"><span data-stu-id="aeead-200">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="aeead-201">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="aeead-201">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="aeead-202">Hämtar eller anger den minsta TLS-version som stöds.</span><span class="sxs-lookup"><span data-stu-id="aeead-202">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="aeead-203">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="aeead-203">-ObjectId</span></span>
<span data-ttu-id="aeead-204">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="aeead-204">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="aeead-205">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aeead-205">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="aeead-206">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="aeead-206">-OozieMetastore</span></span>
<span data-ttu-id="aeead-207">Anger den SQL-databas där Oozie metadata ska lagras.</span><span class="sxs-lookup"><span data-stu-id="aeead-207">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="aeead-208">Du kan också använda Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeead-208">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="aeead-209">-OSType</span><span class="sxs-lookup"><span data-stu-id="aeead-209">-OSType</span></span>
<span data-ttu-id="aeead-210">Anger klustrets operativ system.</span><span class="sxs-lookup"><span data-stu-id="aeead-210">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="aeead-211">Alternativen är: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="aeead-211">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="aeead-212">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="aeead-212">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="aeead-213">Hämtar eller anger typen av utgående åtkomst till det offentliga nätverket.</span><span class="sxs-lookup"><span data-stu-id="aeead-213">Gets or sets the outbound access type to the public network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeead-214">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="aeead-214">-PublicNetworkAccessType</span></span>
<span data-ttu-id="aeead-215">Hämtar eller anger den offentliga nätverks åtkomst typen.</span><span class="sxs-lookup"><span data-stu-id="aeead-215">Gets or sets the public network access type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeead-216">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="aeead-216">-RdpAccessExpiry</span></span>
<span data-ttu-id="aeead-217">Anger förfallo datum, som ett DateTime-objekt, för RDP-åtkomst (Remote Desktop Protocol) till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="aeead-217">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="aeead-218">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="aeead-218">-RdpCredential</span></span>
<span data-ttu-id="aeead-219">Anger autentiseringsuppgifter för fjärr skrivbord (RDP) för klustret.</span><span class="sxs-lookup"><span data-stu-id="aeead-219">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="aeead-220">Det här är endast för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="aeead-220">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="aeead-221">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeead-221">-ResourceGroupName</span></span>
<span data-ttu-id="aeead-222">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="aeead-222">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="aeead-223">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="aeead-223">-ScriptActions</span></span>
<span data-ttu-id="aeead-224">Anger skript åtgärderna som ska köras på klustret när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="aeead-224">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="aeead-225">Du kan också använda Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="aeead-225">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="aeead-226">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="aeead-226">-SecurityProfile</span></span>
<span data-ttu-id="aeead-227">Anger säkerhetsrelaterade egenskaper som används för att skapa ett säkert kluster.</span><span class="sxs-lookup"><span data-stu-id="aeead-227">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="aeead-228">Du kan också använda Add-AzHDInsightSecurityProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeead-228">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="aeead-229">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="aeead-229">-SshCredential</span></span>
<span data-ttu-id="aeead-230">Anger SSH-autentiseringsuppgiften som ska användas för SSH-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="aeead-230">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="aeead-231">Det här är endast för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="aeead-231">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="aeead-232">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="aeead-232">-SshPublicKey</span></span>
<span data-ttu-id="aeead-233">Anger den offentliga nycklar som ska användas för SSH-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="aeead-233">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="aeead-234">Det här är endast för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="aeead-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="aeead-235">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="aeead-235">-SubnetName</span></span>
<span data-ttu-id="aeead-236">Anger namnet på ett under nätverk i det valda virtuella nätverket för klustret.</span><span class="sxs-lookup"><span data-stu-id="aeead-236">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="aeead-237">-Version</span><span class="sxs-lookup"><span data-stu-id="aeead-237">-Version</span></span>
<span data-ttu-id="aeead-238">Anger HDI-versionen för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="aeead-238">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="aeead-239">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="aeead-239">-VirtualNetworkId</span></span>
<span data-ttu-id="aeead-240">Anger ID för det virtuella nätverk som du vill etablera klustret med.</span><span class="sxs-lookup"><span data-stu-id="aeead-240">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="aeead-241">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="aeead-241">-WorkerNodeSize</span></span>
<span data-ttu-id="aeead-242">Anger storleken på den virtuella datorn för arbets tagaren.</span><span class="sxs-lookup"><span data-stu-id="aeead-242">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="aeead-243">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="aeead-243">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="aeead-244">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="aeead-244">-ZookeeperNodeSize</span></span>
<span data-ttu-id="aeead-245">Anger storleken på den virtuella datorn för noden Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="aeead-245">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="aeead-246">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="aeead-246">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="aeead-247">Denna parameter är endast giltig för HBase-och Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="aeead-247">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="aeead-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeead-248">CommonParameters</span></span>
<span data-ttu-id="aeead-249">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeead-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeead-250">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aeead-250">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeead-251">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aeead-251">INPUTS</span></span>

### <span data-ttu-id="aeead-252">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="aeead-252">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="aeead-253">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aeead-253">OUTPUTS</span></span>

### <span data-ttu-id="aeead-254">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="aeead-254">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="aeead-255">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aeead-255">NOTES</span></span>
<span data-ttu-id="aeead-256">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Hadoop, HDInsight, HD, insikt</span><span class="sxs-lookup"><span data-stu-id="aeead-256">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="aeead-257">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aeead-257">RELATED LINKS</span></span>

[<span data-ttu-id="aeead-258">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="aeead-258">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

