---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 66857c9d12bb23ffdccb893b8fae8bfc7c6e0f4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102305"
---
# <span data-ttu-id="a3576-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a3576-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="a3576-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3576-102">SYNOPSIS</span></span>
<span data-ttu-id="a3576-103">Skapar ett icke beständigt kluster konfigurations objekt som beskriver en Azure HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a3576-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="a3576-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3576-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>]
 [-OutboundPublicNetworkAccessType <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3576-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3576-105">DESCRIPTION</span></span>
<span data-ttu-id="a3576-106">**New-AzHDInsightClusterConfig-** cmdleten skapar ett icke bevarat objekt som beskriver en Azure HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a3576-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="a3576-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3576-107">EXAMPLES</span></span>

### <span data-ttu-id="a3576-108">Exempel 1: skapa ett kluster konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="a3576-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="a3576-109">Det här kommandot skapar ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="a3576-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="a3576-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3576-110">PARAMETERS</span></span>

### <span data-ttu-id="a3576-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="a3576-111">-AadTenantId</span></span>
<span data-ttu-id="a3576-112">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3576-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a3576-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a3576-113">-ApplicationId</span></span>
<span data-ttu-id="a3576-114">Hämtar eller anger tjänstens huvud program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a3576-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="a3576-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a3576-115">-AssignedIdentity</span></span>
<span data-ttu-id="a3576-116">Hämtar eller anger den tilldelade identiteten.</span><span class="sxs-lookup"><span data-stu-id="a3576-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="a3576-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="a3576-117">-CertificateFileContents</span></span>
<span data-ttu-id="a3576-118">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3576-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a3576-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="a3576-119">-CertificateFilePath</span></span>
<span data-ttu-id="a3576-120">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="a3576-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a3576-121">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3576-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a3576-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a3576-122">-CertificatePassword</span></span>
<span data-ttu-id="a3576-123">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="a3576-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a3576-124">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3576-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a3576-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="a3576-125">-ClusterTier</span></span>
<span data-ttu-id="a3576-126">Anger HDInsight-klustrets nivå.</span><span class="sxs-lookup"><span data-stu-id="a3576-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="a3576-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a3576-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3576-128">Standar</span><span class="sxs-lookup"><span data-stu-id="a3576-128">Standard</span></span>
- <span data-ttu-id="a3576-129">Premium är standardvärdet standard.</span><span class="sxs-lookup"><span data-stu-id="a3576-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="a3576-130">Premium-nivån kan bara användas med Linux-kluster och det gör att du kan använda några nya funktioner.</span><span class="sxs-lookup"><span data-stu-id="a3576-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="a3576-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="a3576-131">-ClusterType</span></span>
<span data-ttu-id="a3576-132">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a3576-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="a3576-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a3576-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3576-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="a3576-134">Hadoop</span></span>
- <span data-ttu-id="a3576-135">HBase</span><span class="sxs-lookup"><span data-stu-id="a3576-135">HBase</span></span>
- <span data-ttu-id="a3576-136">Tidig</span><span class="sxs-lookup"><span data-stu-id="a3576-136">Storm</span></span>
- <span data-ttu-id="a3576-137">Få verksamheten</span><span class="sxs-lookup"><span data-stu-id="a3576-137">Spark</span></span>
- <span data-ttu-id="a3576-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="a3576-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="a3576-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="a3576-139">Kafka</span></span>
- <span data-ttu-id="a3576-140">RServer</span><span class="sxs-lookup"><span data-stu-id="a3576-140">RServer</span></span>

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

### <span data-ttu-id="a3576-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3576-141">-DefaultProfile</span></span>
<span data-ttu-id="a3576-142">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a3576-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3576-143">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a3576-143">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="a3576-144">Anger den konto nycklar för standard kontot för Azure Storage som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="a3576-144">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="a3576-145">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a3576-145">-DefaultStorageAccountName</span></span>
<span data-ttu-id="a3576-146">Anger namnet på det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="a3576-146">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="a3576-147">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a3576-147">-DefaultStorageAccountType</span></span>
<span data-ttu-id="a3576-148">Anger typen för det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="a3576-148">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="a3576-149">Möjliga värden är AzureStorage och AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="a3576-149">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3576-150">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="a3576-150">-EdgeNodeSize</span></span>
<span data-ttu-id="a3576-151">Anger storleken på den virtuella datorn för noden Edge.</span><span class="sxs-lookup"><span data-stu-id="a3576-151">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="a3576-152">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="a3576-152">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="a3576-153">Den här parametern är endast giltig för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="a3576-153">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="a3576-154">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="a3576-154">-EncryptionAlgorithm</span></span>
<span data-ttu-id="a3576-155">Hämtar eller anger krypteringsalgoritmen.</span><span class="sxs-lookup"><span data-stu-id="a3576-155">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="a3576-156">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="a3576-156">-EncryptionAtHost</span></span>
<span data-ttu-id="a3576-157">Hämtar eller anger flaggan som anger om Aktivera kryptering på värden eller inte.</span><span class="sxs-lookup"><span data-stu-id="a3576-157">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="a3576-158">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="a3576-158">-EncryptionInTransit</span></span>
<span data-ttu-id="a3576-159">Hämtar eller anger flaggan som anger om Aktivera kryptering i transit eller inte.</span><span class="sxs-lookup"><span data-stu-id="a3576-159">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="a3576-160">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="a3576-160">-EncryptionKeyName</span></span>
<span data-ttu-id="a3576-161">Hämtar eller anger namnet på krypterings nycklar.</span><span class="sxs-lookup"><span data-stu-id="a3576-161">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="a3576-162">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="a3576-162">-EncryptionKeyVersion</span></span>
<span data-ttu-id="a3576-163">Hämtar eller anger krypterings huvud versionen.</span><span class="sxs-lookup"><span data-stu-id="a3576-163">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="a3576-164">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="a3576-164">-EncryptionVaultUri</span></span>
<span data-ttu-id="a3576-165">Hämtar eller anger krypterings valv-URI.</span><span class="sxs-lookup"><span data-stu-id="a3576-165">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="a3576-166">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="a3576-166">-HeadNodeSize</span></span>
<span data-ttu-id="a3576-167">Anger storleken på den virtuella datorn för Head-noden.</span><span class="sxs-lookup"><span data-stu-id="a3576-167">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="a3576-168">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="a3576-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="a3576-169">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="a3576-169">-HiveMetastore</span></span>
<span data-ttu-id="a3576-170">Anger metastore för att lagra Hive-metadata.</span><span class="sxs-lookup"><span data-stu-id="a3576-170">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="a3576-171">Du kan också använda Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3576-171">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="a3576-172">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a3576-172">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="a3576-173">Hämtar eller anger den minsta TLS-version som stöds.</span><span class="sxs-lookup"><span data-stu-id="a3576-173">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="a3576-174">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a3576-174">-ObjectId</span></span>
<span data-ttu-id="a3576-175">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="a3576-175">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="a3576-176">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3576-176">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a3576-177">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="a3576-177">-OozieMetastore</span></span>
<span data-ttu-id="a3576-178">Anger metastore för att lagra Oozie-metadata.</span><span class="sxs-lookup"><span data-stu-id="a3576-178">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="a3576-179">Du kan också använda cmdleten **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="a3576-179">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="a3576-180">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="a3576-180">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="a3576-181">Hämtar eller anger typen av utgående åtkomst till det offentliga nätverket.</span><span class="sxs-lookup"><span data-stu-id="a3576-181">Gets or sets the outbound access type to the public network.</span></span>

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

### <span data-ttu-id="a3576-182">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="a3576-182">-PublicNetworkAccessType</span></span>
<span data-ttu-id="a3576-183">Hämtar eller anger den offentliga nätverks åtkomst typen.</span><span class="sxs-lookup"><span data-stu-id="a3576-183">Gets or sets the public network access type.</span></span>

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

### <span data-ttu-id="a3576-184">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="a3576-184">-WorkerNodeSize</span></span>
<span data-ttu-id="a3576-185">Anger storleken på den virtuella datorn för arbets tagaren.</span><span class="sxs-lookup"><span data-stu-id="a3576-185">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="a3576-186">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="a3576-186">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="a3576-187">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="a3576-187">-ZookeeperNodeSize</span></span>
<span data-ttu-id="a3576-188">Anger storleken på den virtuella datorn för noden Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="a3576-188">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="a3576-189">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="a3576-189">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="a3576-190">Denna parameter är endast giltig för HBase-och Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="a3576-190">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="a3576-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3576-191">CommonParameters</span></span>
<span data-ttu-id="a3576-192">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3576-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3576-193">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3576-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3576-194">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3576-194">INPUTS</span></span>

### <span data-ttu-id="a3576-195">Ingen</span><span class="sxs-lookup"><span data-stu-id="a3576-195">None</span></span>

## <span data-ttu-id="a3576-196">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3576-196">OUTPUTS</span></span>

### <span data-ttu-id="a3576-197">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a3576-197">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a3576-198">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3576-198">NOTES</span></span>

## <span data-ttu-id="a3576-199">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3576-199">RELATED LINKS</span></span>

[<span data-ttu-id="a3576-200">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="a3576-200">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


