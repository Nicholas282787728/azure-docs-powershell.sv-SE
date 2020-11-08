---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: b42b93bbecef5ec56495be632788bd1373ae9db1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263083"
---
# <span data-ttu-id="26e09-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="26e09-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="26e09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26e09-102">SYNOPSIS</span></span>
<span data-ttu-id="26e09-103">Skapar ett Azure HDInsight-kluster i den angivna resurs gruppen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="26e09-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="26e09-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26e09-104">SYNTAX</span></span>

### <span data-ttu-id="26e09-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="26e09-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26e09-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="26e09-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26e09-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="26e09-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26e09-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26e09-108">DESCRIPTION</span></span>
<span data-ttu-id="26e09-109">New-AzHDInsightCluster skapar ett Azure HDInsight-kluster med de angivna parametrarna eller med hjälp av ett konfigurations objekt som skapas med hjälp av cmdleten för New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="26e09-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="26e09-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26e09-110">EXAMPLES</span></span>

### <span data-ttu-id="26e09-111">Exempel 1: skapa ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="26e09-111">Example 1: Create an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="26e09-112">Det här kommandot skapar ett kluster i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="26e09-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="26e09-113">Exempel 2: skapa kluster med hanterad kryptering av nycklar</span><span class="sxs-lookup"><span data-stu-id="26e09-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
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

### <span data-ttu-id="26e09-114">Exempel 3: skapa ett Azure HDInsight-kluster som möjliggör kryptering i transit</span><span class="sxs-lookup"><span data-stu-id="26e09-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
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

### <span data-ttu-id="26e09-115">Exempel 4: skapa ett Azure HDInsight-kluster med funktionen privat länk</span><span class="sxs-lookup"><span data-stu-id="26e09-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
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
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="26e09-116">Exempel 5: skapa ett Azure HDInsight-kluster som möjliggör kryptering på värden</span><span class="sxs-lookup"><span data-stu-id="26e09-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
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

### <span data-ttu-id="26e09-117">Exempel 6: skapa ett Azure HDInsight-kluster som aktiverar Autoskala.</span><span class="sxs-lookup"><span data-stu-id="26e09-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
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

### <span data-ttu-id="26e09-118">Exempel 7: skapa ett Azure HDInsight-kluster med Kafka rest-proxy.</span><span class="sxs-lookup"><span data-stu-id="26e09-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
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

### <span data-ttu-id="26e09-119">Exempel 8: skapa ett Azure HDInsight-kluster med Azure Data Lake Gen2-lagring.</span><span class="sxs-lookup"><span data-stu-id="26e09-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
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

### <span data-ttu-id="26e09-120">Exempel 9: skapa ett Azure HDInsight-kluster med ett företags säkerhets paket (ESP) och aktivera stöd för HDInsight-ID.</span><span class="sxs-lookup"><span data-stu-id="26e09-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
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

## <span data-ttu-id="26e09-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26e09-121">PARAMETERS</span></span>

### <span data-ttu-id="26e09-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="26e09-122">-AadTenantId</span></span>
<span data-ttu-id="26e09-123">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="26e09-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="26e09-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="26e09-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="26e09-125">Anger ytterligare Azure Storage-konton för klustret.</span><span class="sxs-lookup"><span data-stu-id="26e09-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="26e09-126">Du kan också använda Add-AzHDInsightStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e09-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="26e09-127">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="26e09-127">-ApplicationId</span></span>
<span data-ttu-id="26e09-128">Hämtar eller anger tjänstens huvud program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="26e09-128">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="26e09-129">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="26e09-129">-AssignedIdentity</span></span>
<span data-ttu-id="26e09-130">Hämtar eller anger den tilldelade identiteten.</span><span class="sxs-lookup"><span data-stu-id="26e09-130">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="26e09-131">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="26e09-131">-AutoscaleConfiguration</span></span>
<span data-ttu-id="26e09-132">Hämtar eller anger den autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="26e09-132">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="26e09-133">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="26e09-133">-CertificateFileContents</span></span>
<span data-ttu-id="26e09-134">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="26e09-134">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="26e09-135">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="26e09-135">-CertificateFilePath</span></span>
<span data-ttu-id="26e09-136">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="26e09-136">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="26e09-137">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="26e09-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="26e09-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="26e09-138">-CertificatePassword</span></span>
<span data-ttu-id="26e09-139">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="26e09-139">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="26e09-140">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="26e09-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="26e09-141">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="26e09-141">-ClusterName</span></span>
<span data-ttu-id="26e09-142">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="26e09-142">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="26e09-143">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="26e09-143">-ClusterSizeInNodes</span></span>
<span data-ttu-id="26e09-144">Anger antalet arbets noder för klustret.</span><span class="sxs-lookup"><span data-stu-id="26e09-144">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="26e09-145">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="26e09-145">-ClusterTier</span></span>
<span data-ttu-id="26e09-146">Anger HDInsight-klustrets nivå.</span><span class="sxs-lookup"><span data-stu-id="26e09-146">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="26e09-147">Detta är vanligt vis standard.</span><span class="sxs-lookup"><span data-stu-id="26e09-147">By default, this is Standard.</span></span>
<span data-ttu-id="26e09-148">Premium-nivån kan bara användas med Linux-kluster och det gör att du kan använda några nya funktioner.</span><span class="sxs-lookup"><span data-stu-id="26e09-148">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="26e09-149">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="26e09-149">-ClusterType</span></span>
<span data-ttu-id="26e09-150">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="26e09-150">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="26e09-151">Alternativen är: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka och RServer</span><span class="sxs-lookup"><span data-stu-id="26e09-151">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="26e09-152">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="26e09-152">-ComponentVersion</span></span>
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

### <span data-ttu-id="26e09-153">-Config</span><span class="sxs-lookup"><span data-stu-id="26e09-153">-Config</span></span>
<span data-ttu-id="26e09-154">Anger vilket kluster objekt som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="26e09-154">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="26e09-155">Du kan skapa det här objektet med hjälp av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e09-155">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="26e09-156">-Konfigurationer</span><span class="sxs-lookup"><span data-stu-id="26e09-156">-Configurations</span></span>
<span data-ttu-id="26e09-157">Anger konfigurationerna för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="26e09-157">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="26e09-158">Du kan också använda Add-AzHDInsightConfigValues cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e09-158">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="26e09-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e09-159">-DefaultProfile</span></span>
<span data-ttu-id="26e09-160">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="26e09-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26e09-161">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="26e09-161">-DisksPerWorkerNode</span></span>
<span data-ttu-id="26e09-162">Anger antalet diskar för rollen arbets tagare i klustret.</span><span class="sxs-lookup"><span data-stu-id="26e09-162">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="26e09-163">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="26e09-163">-EdgeNodeSize</span></span>
<span data-ttu-id="26e09-164">Anger storleken på den virtuella datorn för noden Edge.</span><span class="sxs-lookup"><span data-stu-id="26e09-164">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="26e09-165">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="26e09-165">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="26e09-166">Den här parametern är endast giltig för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="26e09-166">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="26e09-167">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="26e09-167">-EnableIDBroker</span></span>
<span data-ttu-id="26e09-168">Aktiverar funktionen för HDInsight Identity Broker.</span><span class="sxs-lookup"><span data-stu-id="26e09-168">Enables HDInsight Identity Broker feature.</span></span>

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

### <span data-ttu-id="26e09-169">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="26e09-169">-EncryptionAlgorithm</span></span>
<span data-ttu-id="26e09-170">Hämtar eller anger krypteringsalgoritmen.</span><span class="sxs-lookup"><span data-stu-id="26e09-170">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="26e09-171">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="26e09-171">-EncryptionAtHost</span></span>
<span data-ttu-id="26e09-172">Hämtar eller anger flaggan som anger om Aktivera kryptering på värden eller inte.</span><span class="sxs-lookup"><span data-stu-id="26e09-172">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="26e09-173">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="26e09-173">-EncryptionInTransit</span></span>
<span data-ttu-id="26e09-174">Hämtar eller anger flaggan som anger om Aktivera kryptering i transit eller inte.</span><span class="sxs-lookup"><span data-stu-id="26e09-174">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="26e09-175">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="26e09-175">-EncryptionKeyName</span></span>
<span data-ttu-id="26e09-176">Hämtar eller anger namnet på krypterings nycklar.</span><span class="sxs-lookup"><span data-stu-id="26e09-176">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="26e09-177">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="26e09-177">-EncryptionKeyVersion</span></span>
<span data-ttu-id="26e09-178">Hämtar eller anger krypterings huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="26e09-178">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="26e09-179">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="26e09-179">-EncryptionVaultUri</span></span>
<span data-ttu-id="26e09-180">Hämtar eller anger krypterings valv-URI.</span><span class="sxs-lookup"><span data-stu-id="26e09-180">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="26e09-181">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="26e09-181">-HeadNodeSize</span></span>
<span data-ttu-id="26e09-182">Anger storleken på den virtuella datorn för Head-noden.</span><span class="sxs-lookup"><span data-stu-id="26e09-182">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="26e09-183">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="26e09-183">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="26e09-184">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="26e09-184">-HiveMetastore</span></span>
<span data-ttu-id="26e09-185">Anger SQL-databasen där registrerings data för metadata lagras.</span><span class="sxs-lookup"><span data-stu-id="26e09-185">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="26e09-186">Du kan också använda Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e09-186">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="26e09-187">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="26e09-187">-HttpCredential</span></span>
<span data-ttu-id="26e09-188">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="26e09-188">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="26e09-189">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="26e09-189">-KafkaClientGroupId</span></span>
<span data-ttu-id="26e09-190">Hämtar eller anger klient grupp-ID: t för Kafka rest-gruppåtkomst.</span><span class="sxs-lookup"><span data-stu-id="26e09-190">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="26e09-191">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="26e09-191">-KafkaClientGroupName</span></span>
<span data-ttu-id="26e09-192">Hämtar eller anger klient grupp namnet för Kafka rest-gruppåtkomst.</span><span class="sxs-lookup"><span data-stu-id="26e09-192">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="26e09-193">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="26e09-193">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="26e09-194">Hämtar eller anger storleken på Kafka.</span><span class="sxs-lookup"><span data-stu-id="26e09-194">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="26e09-195">-Plats</span><span class="sxs-lookup"><span data-stu-id="26e09-195">-Location</span></span>
<span data-ttu-id="26e09-196">Anger platsen för klustret.</span><span class="sxs-lookup"><span data-stu-id="26e09-196">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="26e09-197">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="26e09-197">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="26e09-198">Hämtar eller anger den minsta TLS-version som stöds.</span><span class="sxs-lookup"><span data-stu-id="26e09-198">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="26e09-199">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="26e09-199">-ObjectId</span></span>
<span data-ttu-id="26e09-200">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="26e09-200">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="26e09-201">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="26e09-201">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="26e09-202">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="26e09-202">-OozieMetastore</span></span>
<span data-ttu-id="26e09-203">Anger den SQL-databas där Oozie metadata ska lagras.</span><span class="sxs-lookup"><span data-stu-id="26e09-203">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="26e09-204">Du kan också använda Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e09-204">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="26e09-205">-OSType</span><span class="sxs-lookup"><span data-stu-id="26e09-205">-OSType</span></span>
<span data-ttu-id="26e09-206">Anger klustrets operativ system.</span><span class="sxs-lookup"><span data-stu-id="26e09-206">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="26e09-207">Alternativen är: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="26e09-207">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="26e09-208">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="26e09-208">-RdpAccessExpiry</span></span>
<span data-ttu-id="26e09-209">Anger förfallo datum, som ett DateTime-objekt, för RDP-åtkomst (Remote Desktop Protocol) till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="26e09-209">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="26e09-210">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="26e09-210">-RdpCredential</span></span>
<span data-ttu-id="26e09-211">Anger autentiseringsuppgifter för fjärr skrivbord (RDP) för klustret.</span><span class="sxs-lookup"><span data-stu-id="26e09-211">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="26e09-212">Det här är endast för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="26e09-212">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="26e09-213">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e09-213">-ResourceGroupName</span></span>
<span data-ttu-id="26e09-214">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="26e09-214">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="26e09-215">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="26e09-215">-ScriptActions</span></span>
<span data-ttu-id="26e09-216">Anger skript åtgärderna som ska köras på klustret när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="26e09-216">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="26e09-217">Du kan också använda Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="26e09-217">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="26e09-218">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="26e09-218">-SecurityProfile</span></span>
<span data-ttu-id="26e09-219">Anger säkerhetsrelaterade egenskaper som används för att skapa ett säkert kluster.</span><span class="sxs-lookup"><span data-stu-id="26e09-219">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="26e09-220">Du kan också använda Add-AzHDInsightSecurityProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e09-220">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="26e09-221">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="26e09-221">-SshCredential</span></span>
<span data-ttu-id="26e09-222">Anger SSH-autentiseringsuppgiften som ska användas för SSH-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="26e09-222">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="26e09-223">Det här är endast för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="26e09-223">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="26e09-224">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="26e09-224">-SshPublicKey</span></span>
<span data-ttu-id="26e09-225">Anger den offentliga nycklar som ska användas för SSH-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="26e09-225">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="26e09-226">Det här är endast för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="26e09-226">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="26e09-227">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="26e09-227">-StorageAccountKey</span></span>
<span data-ttu-id="26e09-228">Hämtar eller anger lagrings konto åtkomst för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="26e09-228">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="26e09-229">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="26e09-229">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="26e09-230">Hämtar eller anger den hanterade identiteten för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="26e09-230">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="26e09-231">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="26e09-231">-StorageAccountResourceId</span></span>
<span data-ttu-id="26e09-232">Hämtar eller anger lagrings resurs-ID för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="26e09-232">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="26e09-233">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="26e09-233">-StorageAccountType</span></span>
<span data-ttu-id="26e09-234">Hämtar eller anger typen av lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="26e09-234">Gets or sets the type of the storage account.</span></span>

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

### <span data-ttu-id="26e09-235">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="26e09-235">-StorageContainer</span></span>
<span data-ttu-id="26e09-236">Hämtar eller anger StorageContainer namn för standard kontot för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="26e09-236">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="26e09-237">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="26e09-237">-StorageFileSystem</span></span>
<span data-ttu-id="26e09-238">Hämtar eller anger fil systemet för standard-Gen2 för Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="26e09-238">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="26e09-239">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="26e09-239">-StorageRootPath</span></span>
<span data-ttu-id="26e09-240">Hämtar eller anger sökvägen till klustrets rot i standard kontot för data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="26e09-240">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="26e09-241">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="26e09-241">-SubnetName</span></span>
<span data-ttu-id="26e09-242">Hämtar eller anger under nätets namn för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="26e09-242">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="26e09-243">-Version</span><span class="sxs-lookup"><span data-stu-id="26e09-243">-Version</span></span>
<span data-ttu-id="26e09-244">Anger HDI-versionen för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="26e09-244">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="26e09-245">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="26e09-245">-VirtualNetworkId</span></span>
<span data-ttu-id="26e09-246">Anger ID för det virtuella nätverk som du vill etablera klustret med.</span><span class="sxs-lookup"><span data-stu-id="26e09-246">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="26e09-247">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="26e09-247">-WorkerNodeSize</span></span>
<span data-ttu-id="26e09-248">Anger storleken på den virtuella datorn för arbets tagaren.</span><span class="sxs-lookup"><span data-stu-id="26e09-248">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="26e09-249">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="26e09-249">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="26e09-250">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="26e09-250">-ZookeeperNodeSize</span></span>
<span data-ttu-id="26e09-251">Anger storleken på den virtuella datorn för noden Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="26e09-251">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="26e09-252">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="26e09-252">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="26e09-253">Denna parameter är endast giltig för HBase-och Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="26e09-253">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="26e09-254">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e09-254">CommonParameters</span></span>
<span data-ttu-id="26e09-255">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e09-255">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e09-256">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26e09-256">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e09-257">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26e09-257">INPUTS</span></span>

### <span data-ttu-id="26e09-258">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="26e09-258">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="26e09-259">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26e09-259">OUTPUTS</span></span>

### <span data-ttu-id="26e09-260">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="26e09-260">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="26e09-261">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26e09-261">NOTES</span></span>
<span data-ttu-id="26e09-262">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Hadoop, HDInsight, HD, insikt</span><span class="sxs-lookup"><span data-stu-id="26e09-262">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="26e09-263">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26e09-263">RELATED LINKS</span></span>

[<span data-ttu-id="26e09-264">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="26e09-264">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

