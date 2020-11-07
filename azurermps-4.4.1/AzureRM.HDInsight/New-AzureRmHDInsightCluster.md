---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: bc89dff9fa6feecf38f0d9f81efb3bdc18c70641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758075"
---
# <span data-ttu-id="fe347-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fe347-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="fe347-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe347-102">SYNOPSIS</span></span>
<span data-ttu-id="fe347-103">Skapar ett Azure HDInsight-kluster i den angivna resurs gruppen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe347-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe347-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe347-104">SYNTAX</span></span>

### <span data-ttu-id="fe347-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="fe347-105">Default (Default)</span></span>
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
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe347-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="fe347-106">CertificateFilePath</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe347-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="fe347-107">CertificateFileContents</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe347-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe347-108">DESCRIPTION</span></span>
<span data-ttu-id="fe347-109">New-AzureHDInsightCluster skapar ett Azure HDInsight-kluster med de angivna parametrarna eller med hjälp av ett konfigurations objekt som skapas med hjälp av cmdleten för New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="fe347-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="fe347-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe347-110">EXAMPLES</span></span>

### <span data-ttu-id="fe347-111">--------------------------Exempel 1: skapa ett Azure HDInsight-kluster--------------------------</span><span class="sxs-lookup"><span data-stu-id="fe347-111">--------------------------  Example 1: Create an Azure HDInsight cluster  --------------------------</span></span>
<span data-ttu-id="fe347-112">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="fe347-112">@{paragraph=PS C:\\\>}</span></span>









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

<span data-ttu-id="fe347-113">Det här kommandot skapar ett kluster i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe347-113">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="fe347-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe347-114">PARAMETERS</span></span>

### <span data-ttu-id="fe347-115">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="fe347-115">-AadTenantId</span></span>
<span data-ttu-id="fe347-116">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fe347-116">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="fe347-117">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="fe347-117">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="fe347-118">Anger ytterligare Azure Storage-konton för klustret.</span><span class="sxs-lookup"><span data-stu-id="fe347-118">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="fe347-119">Du kan också använda Add-AzureRmHDInsightStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe347-119">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="fe347-120">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="fe347-120">-CertificateFileContents</span></span>
<span data-ttu-id="fe347-121">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fe347-121">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="fe347-122">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="fe347-122">-CertificateFilePath</span></span>
<span data-ttu-id="fe347-123">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="fe347-123">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="fe347-124">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fe347-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="fe347-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="fe347-125">-CertificatePassword</span></span>
<span data-ttu-id="fe347-126">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="fe347-126">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="fe347-127">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fe347-127">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="fe347-128">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="fe347-128">-ClusterName</span></span>
<span data-ttu-id="fe347-129">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="fe347-129">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="fe347-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="fe347-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="fe347-131">Anger antalet arbets noder för klustret.</span><span class="sxs-lookup"><span data-stu-id="fe347-131">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="fe347-132">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="fe347-132">-ClusterTier</span></span>
<span data-ttu-id="fe347-133">Anger HDInsight-klustrets nivå.</span><span class="sxs-lookup"><span data-stu-id="fe347-133">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="fe347-134">Detta är vanligt vis standard.</span><span class="sxs-lookup"><span data-stu-id="fe347-134">By default, this is Standard.</span></span>
<span data-ttu-id="fe347-135">Premium-nivån kan bara användas med Linux-kluster och det gör att du kan använda några nya funktioner.</span><span class="sxs-lookup"><span data-stu-id="fe347-135">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="fe347-136">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="fe347-136">-ClusterType</span></span>
<span data-ttu-id="fe347-137">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="fe347-137">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="fe347-138">Alternativen är: Hadoop, HBase, Storm, Spark</span><span class="sxs-lookup"><span data-stu-id="fe347-138">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="fe347-139">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="fe347-139">-ComponentVersion</span></span>
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

### <span data-ttu-id="fe347-140">-Config</span><span class="sxs-lookup"><span data-stu-id="fe347-140">-Config</span></span>
<span data-ttu-id="fe347-141">Anger vilket kluster objekt som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="fe347-141">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="fe347-142">Du kan skapa det här objektet med hjälp av New-AzureRmHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe347-142">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="fe347-143">-Konfigurationer</span><span class="sxs-lookup"><span data-stu-id="fe347-143">-Configurations</span></span>
<span data-ttu-id="fe347-144">Anger konfigurationerna för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="fe347-144">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="fe347-145">Du kan också använda Add-AzureRmHDInsightConfigValues cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe347-145">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="fe347-146">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fe347-146">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="fe347-147">Anger den konto nycklar för standard kontot för Azure Storage som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="fe347-147">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="fe347-148">Du kan också använda Set-AzureRmHDInsightDefaultStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe347-148">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="fe347-149">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fe347-149">-DefaultStorageAccountName</span></span>
<span data-ttu-id="fe347-150">Anger namnet på det standardiserade Azure Storage-kontot som HDInsight-klustret ska använda.</span><span class="sxs-lookup"><span data-stu-id="fe347-150">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="fe347-151">Du kan också använda Set-AzureRmHDInsightDefaultStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe347-151">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="fe347-152">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="fe347-152">-DefaultStorageAccountType</span></span>
<span data-ttu-id="fe347-153">Anger typen för det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="fe347-153">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="fe347-154">Möjliga värden är AzureStorage och AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="fe347-154">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="fe347-155">Standardvärdet är AzureStorage om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="fe347-155">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="fe347-156">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fe347-156">-DefaultStorageContainer</span></span>
<span data-ttu-id="fe347-157">Anger namnet på standard behållaren i det standardiserade Azure Storage-kontot som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="fe347-157">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="fe347-158">Du kan också använda Set-AzureRmHDInsightDefaultStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe347-158">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="fe347-159">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="fe347-159">-DefaultStorageRootPath</span></span>
<span data-ttu-id="fe347-160">Anger sökvägen-prefix i data Lake Store-kontot som HDInsight-klustret ska använda som standard fil system.</span><span class="sxs-lookup"><span data-stu-id="fe347-160">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="fe347-161">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="fe347-161">-EdgeNodeSize</span></span>
<span data-ttu-id="fe347-162">Anger storleken på den virtuella datorn för noden Edge.</span><span class="sxs-lookup"><span data-stu-id="fe347-162">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="fe347-163">Använd Get-AzureRmVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="fe347-163">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="fe347-164">Den här parametern är endast giltig för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="fe347-164">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="fe347-165">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="fe347-165">-HeadNodeSize</span></span>
<span data-ttu-id="fe347-166">Anger storleken på den virtuella datorn för Head-noden.</span><span class="sxs-lookup"><span data-stu-id="fe347-166">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="fe347-167">Använd Get-AzureRmVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="fe347-167">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="fe347-168">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="fe347-168">-HiveMetastore</span></span>
<span data-ttu-id="fe347-169">Anger SQL-databasen där registrerings data för metadata lagras.</span><span class="sxs-lookup"><span data-stu-id="fe347-169">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="fe347-170">Du kan också använda Add-AzureRmHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe347-170">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="fe347-171">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="fe347-171">-HttpCredential</span></span>
<span data-ttu-id="fe347-172">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="fe347-172">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="fe347-173">-Plats</span><span class="sxs-lookup"><span data-stu-id="fe347-173">-Location</span></span>
<span data-ttu-id="fe347-174">Anger platsen för klustret.</span><span class="sxs-lookup"><span data-stu-id="fe347-174">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="fe347-175">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fe347-175">-ObjectId</span></span>
<span data-ttu-id="fe347-176">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="fe347-176">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="fe347-177">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fe347-177">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="fe347-178">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="fe347-178">-OozieMetastore</span></span>
<span data-ttu-id="fe347-179">Anger den SQL-databas där Oozie metadata ska lagras.</span><span class="sxs-lookup"><span data-stu-id="fe347-179">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="fe347-180">Du kan också använda Add-AzureRmHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe347-180">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="fe347-181">-OSType</span><span class="sxs-lookup"><span data-stu-id="fe347-181">-OSType</span></span>
<span data-ttu-id="fe347-182">Anger klustrets operativ system.</span><span class="sxs-lookup"><span data-stu-id="fe347-182">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="fe347-183">Alternativen är: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="fe347-183">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="fe347-184">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="fe347-184">-RdpAccessExpiry</span></span>
<span data-ttu-id="fe347-185">Anger förfallo datum, som ett DateTime-objekt, för RDP-åtkomst (Remote Desktop Protocol) till ett kluster.</span><span class="sxs-lookup"><span data-stu-id="fe347-185">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="fe347-186">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="fe347-186">-RdpCredential</span></span>
<span data-ttu-id="fe347-187">Anger autentiseringsuppgifter för fjärr skrivbord (RDP) för klustret.</span><span class="sxs-lookup"><span data-stu-id="fe347-187">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="fe347-188">Det här är endast för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="fe347-188">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="fe347-189">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe347-189">-ResourceGroupName</span></span>
<span data-ttu-id="fe347-190">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fe347-190">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fe347-191">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="fe347-191">-ScriptActions</span></span>
<span data-ttu-id="fe347-192">Anger skript åtgärderna som ska köras på klustret när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="fe347-192">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="fe347-193">Du kan också använda Add-AzureRmHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="fe347-193">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="fe347-194">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="fe347-194">-SecurityProfile</span></span>
<span data-ttu-id="fe347-195">Anger säkerhetsrelaterade egenskaper som används för att skapa ett säkert kluster.</span><span class="sxs-lookup"><span data-stu-id="fe347-195">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="fe347-196">Du kan också använda Add-AzureRmHDInsightSecurityProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe347-196">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="fe347-197">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="fe347-197">-SshCredential</span></span>
<span data-ttu-id="fe347-198">Anger SSH-autentiseringsuppgiften som ska användas för SSH-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="fe347-198">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="fe347-199">Det här är endast för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="fe347-199">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="fe347-200">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="fe347-200">-SshPublicKey</span></span>
<span data-ttu-id="fe347-201">Anger den offentliga nycklar som ska användas för SSH-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="fe347-201">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="fe347-202">Det här är endast för Linux-kluster.</span><span class="sxs-lookup"><span data-stu-id="fe347-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="fe347-203">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="fe347-203">-SubnetName</span></span>
<span data-ttu-id="fe347-204">Anger namnet på ett under nätverk i det valda virtuella nätverket för klustret.</span><span class="sxs-lookup"><span data-stu-id="fe347-204">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="fe347-205">-Version</span><span class="sxs-lookup"><span data-stu-id="fe347-205">-Version</span></span>
<span data-ttu-id="fe347-206">Anger HDI-versionen för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="fe347-206">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="fe347-207">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="fe347-207">-VirtualNetworkId</span></span>
<span data-ttu-id="fe347-208">Anger ID för det virtuella nätverk som du vill etablera klustret med.</span><span class="sxs-lookup"><span data-stu-id="fe347-208">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="fe347-209">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="fe347-209">-WorkerNodeSize</span></span>
<span data-ttu-id="fe347-210">Anger storleken på den virtuella datorn för arbets tagaren.</span><span class="sxs-lookup"><span data-stu-id="fe347-210">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="fe347-211">Använd Get-AzureRmVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="fe347-211">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="fe347-212">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="fe347-212">-ZookeeperNodeSize</span></span>
<span data-ttu-id="fe347-213">Anger storleken på den virtuella datorn för noden Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="fe347-213">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="fe347-214">Använd Get-AzureRmVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="fe347-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="fe347-215">Denna parameter är endast giltig för HBase-och Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="fe347-215">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="fe347-216">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe347-216">-DefaultProfile</span></span>
<span data-ttu-id="fe347-217">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe347-217">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe347-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe347-218">CommonParameters</span></span>
<span data-ttu-id="fe347-219">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe347-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe347-220">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe347-220">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe347-221">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe347-221">INPUTS</span></span>

### <span data-ttu-id="fe347-222">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="fe347-222">AzureHDInsightConfig</span></span>
<span data-ttu-id="fe347-223">Parametern ' config ' godkänner värdet av typen ' AzureHDInsightConfig ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fe347-223">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="fe347-224">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe347-224">OUTPUTS</span></span>

### <span data-ttu-id="fe347-225">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fe347-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="fe347-226">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe347-226">NOTES</span></span>
<span data-ttu-id="fe347-227">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Hadoop, HDInsight, HD, insikt</span><span class="sxs-lookup"><span data-stu-id="fe347-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="fe347-228">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe347-228">RELATED LINKS</span></span>

[<span data-ttu-id="fe347-229">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="fe347-229">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

