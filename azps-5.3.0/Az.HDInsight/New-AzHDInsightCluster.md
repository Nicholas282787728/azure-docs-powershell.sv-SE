---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: f4592a371e528c7779e07251bf79677dac47e6df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520607"
---
# <span data-ttu-id="e31d1-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e31d1-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="e31d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e31d1-102">SYNOPSIS</span></span>
<span data-ttu-id="e31d1-103">Skapar ett Azure HDInsight-kluster i den angivna resurs gruppen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e31d1-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="e31d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e31d1-104">SYNTAX</span></span>

### <span data-ttu-id="e31d1-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="e31d1-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-StorageAccountManagedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker] [-KafkaClientGroupId <String>]
 [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>] [-PrivateLink <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e31d1-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e31d1-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e31d1-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e31d1-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e31d1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e31d1-108">DESCRIPTION</span></span>
<span data-ttu-id="e31d1-109">New-AzHDInsightCluster skapar ett Azure HDInsight-kluster med de angivna parametrarna eller med hjälp av ett konfigurations objekt som skapas med hjälp av cmdleten för New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="e31d1-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="e31d1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e31d1-110">EXAMPLES</span></span>

### <span data-ttu-id="e31d1-111">Exempel 1: skapa ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="e31d1-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="e31d1-112">Det här kommandot skapar ett kluster i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e31d1-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="e31d1-113">Exempel 2: skapa kluster med hanterad kryptering av nycklar</span><span class="sxs-lookup"><span data-stu-id="e31d1-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="e31d1-114">Exempel 3: skapa ett Azure HDInsight-kluster som möjliggör kryptering i transit</span><span class="sxs-lookup"><span data-stu-id="e31d1-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="e31d1-115">Exempel 4: skapa ett Azure HDInsight-kluster med funktionen för utgående och ta bort relä</span><span class="sxs-lookup"><span data-stu-id="e31d1-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
        $subnetName="yoursubnetname"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -ResourceProviderConnection Outbound -PrivateLink Enabled `
```

### <span data-ttu-id="e31d1-116">Exempel 5: skapa ett Azure HDInsight-kluster som möjliggör kryptering på värden</span><span class="sxs-lookup"><span data-stu-id="e31d1-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="e31d1-117">Exempel 6: skapa ett Azure HDInsight-kluster som aktiverar Autoskala.</span><span class="sxs-lookup"><span data-stu-id="e31d1-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

### <span data-ttu-id="e31d1-118">Exempel 7: skapa ett Azure HDInsight-kluster med Kafka rest-proxy.</span><span class="sxs-lookup"><span data-stu-id="e31d1-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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

        # Kafka Rest Proxy configuration info
        $kafkaClientGroupName = "yourclientgroupname"
        $kafkaClientGroupId = "yourclientgroupid"
        $kafkaManagementNodeSize = "Standard_D4_v2"
        $disksPerWorkerNode = 2

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Kafka `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -KafkaClientGroupId  $kafkaClientGroupId -KafkaClientGroupName $kafkaClientGroupName `
            -KafkaManagementNodeSize $kafkaManagementNodeSize -DisksPerWorkerNode $disksPerWorkerNode
```

### <span data-ttu-id="e31d1-119">Exempel 8: skapa ett Azure HDInsight-kluster med Azure Data Lake Gen2-lagring.</span><span class="sxs-lookup"><span data-stu-id="e31d1-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageManagedIdentity = "yourstorageusermanagedidentity"
        $storageFileSystem = "filesystem01"
        $storageAccountType=AzureDataLakeStorageGen2

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
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountManagedIdentity $storageManagedIdentity `
            -StorageFileSystem $storageFileSystem `
            -StorageAccountType $storageAccountType `
            -SshCredential $clusterCreds
```

### <span data-ttu-id="e31d1-120">Exempel 9: skapa ett Azure HDInsight-kluster med ett företags säkerhets paket (ESP) och aktivera stöd för HDInsight-ID.</span><span class="sxs-lookup"><span data-stu-id="e31d1-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = "yourstorageaccountaccesskey"
        $storageContainer = "yourcontainer01"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # ESP configuration
        $domainResourceId = "your Azure AD Domin Service resource id"
        $domainUser = "yourdomainuser"
        $domainPassword = "yourdoaminpasswd"
        $domainPassword = ConvertTo-SecureString $domainPassword -AsPlainText -Force
        $domainCredential = New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
        $clusterUserGroupDns = "dominusergroup"
        $ldapUrls = "ldaps://{your domain name}:636"

        $clusterTier = Premium
        $vnetId = "yourvnetid"
        $subnetName = "yoursubnetname"
        $assignedIdentity = "your user managed assigned identity resourcee id"

        #Create security profile
        $config= New-AzHDInsightClusterConfig|Add-AzHDInsightSecurityProfile -DomainResourceId $domainResourceId -DomainUserCredential $domainCredential -LdapsUrls $ldapUrls -ClusterUsersGroupDNs $clusterUserGroupDns

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusteTier $clusterTier `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $vnetId -SubnetName $subnetName `
            -AssignedIdentity $assignedIdentity `
            -SecurityProfile $config.SecurityProfile -EnableIDBroker
```

## <span data-ttu-id="e31d1-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e31d1-121">PARAMETERS</span></span>

### <span data-ttu-id="e31d1-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="e31d1-122">-AadTenantId</span></span>
<span data-ttu-id="e31d1-123">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e31d1-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e31d1-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e31d1-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="e31d1-125">Anger ytterligare Azure Storage-konton för klustret.</span><span class="sxs-lookup"><span data-stu-id="e31d1-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="e31d1-126">Du kan också använda Add-AzHDInsightStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e31d1-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="e31d1-127">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="e31d1-127">-AmbariDatabase</span></span>
<span data-ttu-id="e31d1-128">Hämtar eller anger databasen för Ambari.</span><span class="sxs-lookup"><span data-stu-id="e31d1-128">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="e31d1-129">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e31d1-129">-ApplicationId</span></span>
<span data-ttu-id="e31d1-130">Hämtar eller anger tjänstens huvud program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="e31d1-130">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="e31d1-131">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e31d1-131">-AssignedIdentity</span></span>
<span data-ttu-id="e31d1-132">Hämtar eller anger den tilldelade identiteten.</span><span class="sxs-lookup"><span data-stu-id="e31d1-132">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="e31d1-133">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e31d1-133">-AutoscaleConfiguration</span></span>
<span data-ttu-id="e31d1-134">Hämtar eller anger den autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="e31d1-134">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="e31d1-135">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e31d1-135">-CertificateFileContents</span></span>
<span data-ttu-id="e31d1-136">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e31d1-136">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e31d1-137">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e31d1-137">-CertificateFilePath</span></span>
<span data-ttu-id="e31d1-138">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="e31d1-138">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e31d1-139">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e31d1-139">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e31d1-140">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e31d1-140">-CertificatePassword</span></span>
<span data-ttu-id="e31d1-141">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="e31d1-141">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e31d1-142">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e31d1-142">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e31d1-143">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="e31d1-143">-ClusterName</span></span>
<span data-ttu-id="e31d1-144">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="e31d1-144">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e31d1-145">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="e31d1-145">-ClusterSizeInNodes</span></span>
<span data-ttu-id="e31d1-146">Anger antalet arbets noder för klustret.</span><span class="sxs-lookup"><span data-stu-id="e31d1-146">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="e31d1-147">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="e31d1-147">-ClusterTier</span></span>
<span data-ttu-id="e31d1-148">Anger HDInsight-klustrets nivå.</span><span class="sxs-lookup"><span data-stu-id="e31d1-148">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="e31d1-149">Detta är vanligt vis standard.</span><span class="sxs-lookup"><span data-stu-id="e31d1-149">By default, this is Standard.</span></span>
<span data-ttu-id="e31d1-150">Premium-nivån kan bara användas med Linux-kluster och det gör att du kan använda några nya funktioner.</span><span class="sxs-lookup"><span data-stu-id="e31d1-150">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="e31d1-151">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="e31d1-151">-ClusterType</span></span>
<span data-ttu-id="e31d1-152">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e31d1-152">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="e31d1-153">Alternativen är: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka och RServer</span><span class="sxs-lookup"><span data-stu-id="e31d1-153">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="e31d1-154">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="e31d1-154">-ComponentVersion</span></span>
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

### <span data-ttu-id="e31d1-155">-Config</span><span class="sxs-lookup"><span data-stu-id="e31d1-155">-Config</span></span>
<span data-ttu-id="e31d1-156">Anger vilket kluster objekt som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="e31d1-156">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="e31d1-157">Du kan skapa det här objektet med hjälp av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e31d1-157">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="e31d1-158">-Konfigurationer</span><span class="sxs-lookup"><span data-stu-id="e31d1-158">-Configurations</span></span>
<span data-ttu-id="e31d1-159">Anger konfigurationerna för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="e31d1-159">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="e31d1-160">Du kan också använda Add-AzHDInsightConfigValues cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e31d1-160">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="e31d1-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e31d1-161">-DefaultProfile</span></span>
<span data-ttu-id="e31d1-162">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e31d1-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e31d1-163">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="e31d1-163">-DisksPerWorkerNode</span></span>
<span data-ttu-id="e31d1-164">Anger antalet diskar för rollen arbets tagare i klustret.</span><span class="sxs-lookup"><span data-stu-id="e31d1-164">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="e31d1-165">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="e31d1-165">-EdgeNodeSize</span></span>
<span data-ttu-id="e31d1-166">Anger storleken på den virtuella datorn för noden Edge.</span><span class="sxs-lookup"><span data-stu-id="e31d1-166">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="e31d1-167">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="e31d1-167">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="e31d1-168">Den här parametern är endast giltig för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="e31d1-168">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="e31d1-169">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="e31d1-169">-EnableIDBroker</span></span>
<span data-ttu-id="e31d1-170">Aktiverar funktionen för HDInsight Identity Broker.</span><span class="sxs-lookup"><span data-stu-id="e31d1-170">Enables HDInsight Identity Broker feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e31d1-171">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e31d1-171">-EncryptionAlgorithm</span></span>
<span data-ttu-id="e31d1-172">Hämtar eller anger krypteringsalgoritmen.</span><span class="sxs-lookup"><span data-stu-id="e31d1-172">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="e31d1-173">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="e31d1-173">-EncryptionAtHost</span></span>
<span data-ttu-id="e31d1-174">Hämtar eller anger flaggan som anger om Aktivera kryptering på värden eller inte.</span><span class="sxs-lookup"><span data-stu-id="e31d1-174">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="e31d1-175">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="e31d1-175">-EncryptionInTransit</span></span>
<span data-ttu-id="e31d1-176">Hämtar eller anger flaggan som anger om Aktivera kryptering i transit eller inte.</span><span class="sxs-lookup"><span data-stu-id="e31d1-176">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="e31d1-177">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="e31d1-177">-EncryptionKeyName</span></span>
<span data-ttu-id="e31d1-178">Hämtar eller anger namnet på krypterings nycklar.</span><span class="sxs-lookup"><span data-stu-id="e31d1-178">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="e31d1-179">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e31d1-179">-EncryptionKeyVersion</span></span>
<span data-ttu-id="e31d1-180">Hämtar eller anger krypterings huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="e31d1-180">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="e31d1-181">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="e31d1-181">-EncryptionVaultUri</span></span>
<span data-ttu-id="e31d1-182">Hämtar eller anger krypterings valv-URI.</span><span class="sxs-lookup"><span data-stu-id="e31d1-182">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="e31d1-183">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="e31d1-183">-HeadNodeSize</span></span>
<span data-ttu-id="e31d1-184">Anger storleken på den virtuella datorn för Head-noden.</span><span class="sxs-lookup"><span data-stu-id="e31d1-184">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="e31d1-185">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="e31d1-185">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e31d1-186">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="e31d1-186">-HiveMetastore</span></span>
<span data-ttu-id="e31d1-187">Anger SQL-databasen där registrerings data för metadata lagras.</span><span class="sxs-lookup"><span data-stu-id="e31d1-187">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="e31d1-188">Du kan också använda Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e31d1-188">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="e31d1-189">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e31d1-189">-HttpCredential</span></span>
<span data-ttu-id="e31d1-190">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="e31d1-190">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="e31d1-191">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="e31d1-191">-KafkaClientGroupId</span></span>
<span data-ttu-id="e31d1-192">Hämtar eller anger klient grupp-ID: t för Kafka rest-gruppåtkomst.</span><span class="sxs-lookup"><span data-stu-id="e31d1-192">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="e31d1-193">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="e31d1-193">-KafkaClientGroupName</span></span>
<span data-ttu-id="e31d1-194">Hämtar eller anger klient grupp namnet för Kafka rest-gruppåtkomst.</span><span class="sxs-lookup"><span data-stu-id="e31d1-194">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="e31d1-195">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="e31d1-195">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="e31d1-196">Hämtar eller anger storleken på Kafka.</span><span class="sxs-lookup"><span data-stu-id="e31d1-196">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="e31d1-197">-Plats</span><span class="sxs-lookup"><span data-stu-id="e31d1-197">-Location</span></span>
<span data-ttu-id="e31d1-198">Anger platsen för klustret.</span><span class="sxs-lookup"><span data-stu-id="e31d1-198">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="e31d1-199">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e31d1-199">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="e31d1-200">Hämtar eller anger den minsta TLS-version som stöds.</span><span class="sxs-lookup"><span data-stu-id="e31d1-200">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="e31d1-201">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e31d1-201">-ObjectId</span></span>
<span data-ttu-id="e31d1-202">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="e31d1-202">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="e31d1-203">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e31d1-203">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e31d1-204">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="e31d1-204">-OozieMetastore</span></span>
<span data-ttu-id="e31d1-205">Anger den SQL-databas där Oozie metadata ska lagras.</span><span class="sxs-lookup"><span data-stu-id="e31d1-205">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="e31d1-206">Du kan också använda Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e31d1-206">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="e31d1-207">-OSType</span><span class="sxs-lookup"><span data-stu-id="e31d1-207">-OSType</span></span>
<span data-ttu-id="e31d1-208">Anger klustrets operativ system.</span><span class="sxs-lookup"><span data-stu-id="e31d1-208">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="e31d1-209">Alternativen är: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="e31d1-209">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="e31d1-210">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="e31d1-210">-PrivateLink</span></span>
<span data-ttu-id="e31d1-211">Hämtar eller anger den privata länk typen.</span><span class="sxs-lookup"><span data-stu-id="e31d1-211">Gets or sets the private link type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e31d1-212">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="e31d1-212">-RdpAccessExpiry</span></span>
<span data-ttu-id="e31d1-213">Anger förfallo datum, som ett DateTime-objekt, för RDP-åtkomst (Remote Desktop Protocol) till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="e31d1-213">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="e31d1-214">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="e31d1-214">-RdpCredential</span></span>
<span data-ttu-id="e31d1-215">Anger autentiseringsuppgifter för fjärr skrivbord (RDP) för klustret.</span><span class="sxs-lookup"><span data-stu-id="e31d1-215">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="e31d1-216">Det här är endast för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="e31d1-216">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="e31d1-217">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e31d1-217">-ResourceGroupName</span></span>
<span data-ttu-id="e31d1-218">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e31d1-218">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e31d1-219">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="e31d1-219">-ResourceProviderConnection</span></span>
<span data-ttu-id="e31d1-220">Hämtar eller anger anslutnings typen för resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="e31d1-220">Gets or sets the resource provider connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e31d1-221">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="e31d1-221">-ScriptActions</span></span>
<span data-ttu-id="e31d1-222">Anger skript åtgärderna som ska köras på klustret när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="e31d1-222">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="e31d1-223">Du kan också använda Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="e31d1-223">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="e31d1-224">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="e31d1-224">-SecurityProfile</span></span>
<span data-ttu-id="e31d1-225">Anger säkerhetsrelaterade egenskaper som används för att skapa ett säkert kluster.</span><span class="sxs-lookup"><span data-stu-id="e31d1-225">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="e31d1-226">Du kan också använda Add-AzHDInsightSecurityProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e31d1-226">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="e31d1-227">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="e31d1-227">-SshCredential</span></span>
<span data-ttu-id="e31d1-228">Anger SSH-autentiseringsuppgiften som ska användas för SSH-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="e31d1-228">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="e31d1-229">Det här är endast för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="e31d1-229">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="e31d1-230">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e31d1-230">-SshPublicKey</span></span>
<span data-ttu-id="e31d1-231">Anger den offentliga nycklar som ska användas för SSH-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="e31d1-231">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="e31d1-232">Det här är endast för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="e31d1-232">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="e31d1-233">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e31d1-233">-StorageAccountKey</span></span>
<span data-ttu-id="e31d1-234">Hämtar eller anger lagrings konto åtkomst för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e31d1-234">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="e31d1-235">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e31d1-235">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="e31d1-236">Hämtar eller anger den hanterade identiteten för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e31d1-236">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="e31d1-237">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e31d1-237">-StorageAccountResourceId</span></span>
<span data-ttu-id="e31d1-238">Hämtar eller anger lagrings resurs-ID för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="e31d1-238">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="e31d1-239">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e31d1-239">-StorageAccountType</span></span>
<span data-ttu-id="e31d1-240">Hämtar eller anger typen av lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e31d1-240">Gets or sets the type of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e31d1-241">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="e31d1-241">-StorageContainer</span></span>
<span data-ttu-id="e31d1-242">Hämtar eller anger StorageContainer namn för standard kontot för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="e31d1-242">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="e31d1-243">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="e31d1-243">-StorageFileSystem</span></span>
<span data-ttu-id="e31d1-244">Hämtar eller anger fil systemet för standard-Gen2 för Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="e31d1-244">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="e31d1-245">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="e31d1-245">-StorageRootPath</span></span>
<span data-ttu-id="e31d1-246">Hämtar eller anger sökvägen till klustrets rot i standard kontot för data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e31d1-246">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="e31d1-247">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e31d1-247">-SubnetName</span></span>
<span data-ttu-id="e31d1-248">Hämtar eller anger under nätets namn för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="e31d1-248">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="e31d1-249">-Version</span><span class="sxs-lookup"><span data-stu-id="e31d1-249">-Version</span></span>
<span data-ttu-id="e31d1-250">Anger HDI-versionen för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="e31d1-250">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="e31d1-251">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e31d1-251">-VirtualNetworkId</span></span>
<span data-ttu-id="e31d1-252">Anger ID för det virtuella nätverk som du vill etablera klustret med.</span><span class="sxs-lookup"><span data-stu-id="e31d1-252">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="e31d1-253">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="e31d1-253">-WorkerNodeSize</span></span>
<span data-ttu-id="e31d1-254">Anger storleken på den virtuella datorn för arbets tagaren.</span><span class="sxs-lookup"><span data-stu-id="e31d1-254">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="e31d1-255">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="e31d1-255">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e31d1-256">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="e31d1-256">-ZookeeperNodeSize</span></span>
<span data-ttu-id="e31d1-257">Anger storleken på den virtuella datorn för noden Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="e31d1-257">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="e31d1-258">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="e31d1-258">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="e31d1-259">Denna parameter är endast giltig för HBase-och Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="e31d1-259">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="e31d1-260">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e31d1-260">CommonParameters</span></span>
<span data-ttu-id="e31d1-261">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e31d1-261">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e31d1-262">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e31d1-262">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e31d1-263">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e31d1-263">INPUTS</span></span>

### <span data-ttu-id="e31d1-264">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e31d1-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e31d1-265">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e31d1-265">OUTPUTS</span></span>

### <span data-ttu-id="e31d1-266">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e31d1-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="e31d1-267">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e31d1-267">NOTES</span></span>
<span data-ttu-id="e31d1-268">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Hadoop, HDInsight, HD, insikt</span><span class="sxs-lookup"><span data-stu-id="e31d1-268">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="e31d1-269">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e31d1-269">RELATED LINKS</span></span>

[<span data-ttu-id="e31d1-270">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e31d1-270">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

