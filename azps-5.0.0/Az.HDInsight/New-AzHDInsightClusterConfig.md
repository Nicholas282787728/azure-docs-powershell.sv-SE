---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271071"
---
# <span data-ttu-id="c4f13-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c4f13-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="c4f13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4f13-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f13-103">Skapar ett icke beständigt kluster konfigurations objekt som beskriver en Azure HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4f13-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="c4f13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4f13-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4f13-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4f13-105">DESCRIPTION</span></span>
<span data-ttu-id="c4f13-106">**New-AzHDInsightClusterConfig-** cmdleten skapar ett icke bevarat objekt som beskriver en Azure HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4f13-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="c4f13-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4f13-107">EXAMPLES</span></span>

### <span data-ttu-id="c4f13-108">Exempel 1: skapa ett kluster konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="c4f13-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="c4f13-109">Det här kommandot skapar ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="c4f13-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="c4f13-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4f13-110">PARAMETERS</span></span>

### <span data-ttu-id="c4f13-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="c4f13-111">-AadTenantId</span></span>
<span data-ttu-id="c4f13-112">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c4f13-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c4f13-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c4f13-113">-ApplicationId</span></span>
<span data-ttu-id="c4f13-114">Hämtar eller anger tjänstens huvud program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="c4f13-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="c4f13-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c4f13-115">-AssignedIdentity</span></span>
<span data-ttu-id="c4f13-116">Hämtar eller anger den tilldelade identiteten.</span><span class="sxs-lookup"><span data-stu-id="c4f13-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="c4f13-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c4f13-117">-CertificateFileContents</span></span>
<span data-ttu-id="c4f13-118">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c4f13-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f13-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c4f13-119">-CertificateFilePath</span></span>
<span data-ttu-id="c4f13-120">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="c4f13-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c4f13-121">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c4f13-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c4f13-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c4f13-122">-CertificatePassword</span></span>
<span data-ttu-id="c4f13-123">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="c4f13-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c4f13-124">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c4f13-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c4f13-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="c4f13-125">-ClusterTier</span></span>
<span data-ttu-id="c4f13-126">Anger HDInsight-klustrets nivå.</span><span class="sxs-lookup"><span data-stu-id="c4f13-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="c4f13-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c4f13-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4f13-128">Standar</span><span class="sxs-lookup"><span data-stu-id="c4f13-128">Standard</span></span>
- <span data-ttu-id="c4f13-129">Premium är standardvärdet standard.</span><span class="sxs-lookup"><span data-stu-id="c4f13-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="c4f13-130">Premium-nivån kan bara användas med Linux-kluster och det gör att du kan använda några nya funktioner.</span><span class="sxs-lookup"><span data-stu-id="c4f13-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="c4f13-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="c4f13-131">-ClusterType</span></span>
<span data-ttu-id="c4f13-132">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="c4f13-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="c4f13-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c4f13-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4f13-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="c4f13-134">Hadoop</span></span>
- <span data-ttu-id="c4f13-135">HBase</span><span class="sxs-lookup"><span data-stu-id="c4f13-135">HBase</span></span>
- <span data-ttu-id="c4f13-136">Tidig</span><span class="sxs-lookup"><span data-stu-id="c4f13-136">Storm</span></span>
- <span data-ttu-id="c4f13-137">Få verksamheten</span><span class="sxs-lookup"><span data-stu-id="c4f13-137">Spark</span></span>
- <span data-ttu-id="c4f13-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="c4f13-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="c4f13-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="c4f13-139">Kafka</span></span>
- <span data-ttu-id="c4f13-140">RServer</span><span class="sxs-lookup"><span data-stu-id="c4f13-140">RServer</span></span>

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

### <span data-ttu-id="c4f13-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f13-141">-DefaultProfile</span></span>
<span data-ttu-id="c4f13-142">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c4f13-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4f13-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="c4f13-143">-EdgeNodeSize</span></span>
<span data-ttu-id="c4f13-144">Anger storleken på den virtuella datorn för noden Edge.</span><span class="sxs-lookup"><span data-stu-id="c4f13-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="c4f13-145">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="c4f13-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="c4f13-146">Den här parametern är endast giltig för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="c4f13-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="c4f13-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c4f13-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="c4f13-148">Hämtar eller anger krypteringsalgoritmen.</span><span class="sxs-lookup"><span data-stu-id="c4f13-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="c4f13-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="c4f13-149">-EncryptionAtHost</span></span>
<span data-ttu-id="c4f13-150">Hämtar eller anger flaggan som anger om Aktivera kryptering på värden eller inte.</span><span class="sxs-lookup"><span data-stu-id="c4f13-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="c4f13-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="c4f13-151">-EncryptionInTransit</span></span>
<span data-ttu-id="c4f13-152">Hämtar eller anger flaggan som anger om Aktivera kryptering i transit eller inte.</span><span class="sxs-lookup"><span data-stu-id="c4f13-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="c4f13-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="c4f13-153">-EncryptionKeyName</span></span>
<span data-ttu-id="c4f13-154">Hämtar eller anger namnet på krypterings nycklar.</span><span class="sxs-lookup"><span data-stu-id="c4f13-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="c4f13-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c4f13-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="c4f13-156">Hämtar eller anger krypterings huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="c4f13-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="c4f13-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="c4f13-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="c4f13-158">Hämtar eller anger krypterings valv-URI.</span><span class="sxs-lookup"><span data-stu-id="c4f13-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="c4f13-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="c4f13-159">-HeadNodeSize</span></span>
<span data-ttu-id="c4f13-160">Anger storleken på den virtuella datorn för Head-noden.</span><span class="sxs-lookup"><span data-stu-id="c4f13-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="c4f13-161">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="c4f13-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c4f13-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="c4f13-162">-HiveMetastore</span></span>
<span data-ttu-id="c4f13-163">Anger metastore för att lagra Hive-metadata.</span><span class="sxs-lookup"><span data-stu-id="c4f13-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="c4f13-164">Du kan också använda Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4f13-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="c4f13-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c4f13-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="c4f13-166">Hämtar eller anger den minsta TLS-version som stöds.</span><span class="sxs-lookup"><span data-stu-id="c4f13-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="c4f13-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c4f13-167">-ObjectId</span></span>
<span data-ttu-id="c4f13-168">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="c4f13-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="c4f13-169">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c4f13-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c4f13-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="c4f13-170">-OozieMetastore</span></span>
<span data-ttu-id="c4f13-171">Anger metastore för att lagra Oozie-metadata.</span><span class="sxs-lookup"><span data-stu-id="c4f13-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="c4f13-172">Du kan också använda cmdleten **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="c4f13-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="c4f13-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c4f13-173">-StorageAccountKey</span></span>
<span data-ttu-id="c4f13-174">Hämtar eller anger åtkomst till lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="c4f13-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="c4f13-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c4f13-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="c4f13-176">Hämtar eller anger resurs-ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c4f13-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="c4f13-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c4f13-177">-StorageAccountType</span></span>
<span data-ttu-id="c4f13-178">Hämtar eller anger typen av standard lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c4f13-178">Gets or sets the type of the default storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f13-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="c4f13-179">-WorkerNodeSize</span></span>
<span data-ttu-id="c4f13-180">Anger storleken på den virtuella datorn för arbets tagaren.</span><span class="sxs-lookup"><span data-stu-id="c4f13-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="c4f13-181">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="c4f13-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c4f13-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="c4f13-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="c4f13-183">Anger storleken på den virtuella datorn för noden Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="c4f13-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="c4f13-184">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="c4f13-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="c4f13-185">Denna parameter är endast giltig för HBase-och Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="c4f13-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="c4f13-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f13-186">CommonParameters</span></span>
<span data-ttu-id="c4f13-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4f13-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f13-188">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4f13-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f13-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4f13-189">INPUTS</span></span>

### <span data-ttu-id="c4f13-190">Ingen</span><span class="sxs-lookup"><span data-stu-id="c4f13-190">None</span></span>

## <span data-ttu-id="c4f13-191">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4f13-191">OUTPUTS</span></span>

### <span data-ttu-id="c4f13-192">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c4f13-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c4f13-193">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4f13-193">NOTES</span></span>

## <span data-ttu-id="c4f13-194">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4f13-194">RELATED LINKS</span></span>

[<span data-ttu-id="c4f13-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="c4f13-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)

