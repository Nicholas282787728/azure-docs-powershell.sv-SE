---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 38dc23c2bebe3c608833e55bcb4ffb2d687f9041
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928125"
---
# <span data-ttu-id="92623-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="92623-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="92623-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92623-102">SYNOPSIS</span></span>
<span data-ttu-id="92623-103">Skapar ett icke beständigt kluster konfigurations objekt som beskriver en Azure HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="92623-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="92623-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92623-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [[-DefaultStorageAccountType] <StorageType>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>] [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>]
 [[-EdgeNodeSize] <String>] [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>] [[-ClusterTier] <Tier>]
 [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>] [[-CertificateFileContents] <Byte[]>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92623-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92623-105">DESCRIPTION</span></span>
<span data-ttu-id="92623-106">**New-AzHDInsightClusterConfig-** cmdleten skapar ett icke bevarat objekt som beskriver en Azure HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="92623-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="92623-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92623-107">EXAMPLES</span></span>

### <span data-ttu-id="92623-108">Exempel 1: skapa ett kluster konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="92623-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="92623-109">Det här kommandot skapar ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="92623-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="92623-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92623-110">PARAMETERS</span></span>

### <span data-ttu-id="92623-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="92623-111">-AadTenantId</span></span>
<span data-ttu-id="92623-112">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92623-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="92623-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="92623-113">-ApplicationId</span></span>
<span data-ttu-id="92623-114">Hämtar eller anger tjänstens huvud program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="92623-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="92623-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="92623-115">-CertificateFileContents</span></span>
<span data-ttu-id="92623-116">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92623-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="92623-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="92623-117">-CertificateFilePath</span></span>
<span data-ttu-id="92623-118">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="92623-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="92623-119">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92623-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="92623-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="92623-120">-CertificatePassword</span></span>
<span data-ttu-id="92623-121">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="92623-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="92623-122">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92623-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="92623-123">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="92623-123">-ClusterTier</span></span>
<span data-ttu-id="92623-124">Anger HDInsight-klustrets nivå.</span><span class="sxs-lookup"><span data-stu-id="92623-124">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="92623-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="92623-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92623-126">Standar</span><span class="sxs-lookup"><span data-stu-id="92623-126">Standard</span></span>
- <span data-ttu-id="92623-127">Premium är standardvärdet standard.</span><span class="sxs-lookup"><span data-stu-id="92623-127">Premium The default value is Standard.</span></span>
<span data-ttu-id="92623-128">Premium-nivån kan bara användas med Linux-kluster och det gör att du kan använda några nya funktioner.</span><span class="sxs-lookup"><span data-stu-id="92623-128">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="92623-129">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="92623-129">-ClusterType</span></span>
<span data-ttu-id="92623-130">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="92623-130">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="92623-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="92623-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92623-132">Hadoop</span><span class="sxs-lookup"><span data-stu-id="92623-132">Hadoop</span></span>
- <span data-ttu-id="92623-133">HBase</span><span class="sxs-lookup"><span data-stu-id="92623-133">HBase</span></span>
- <span data-ttu-id="92623-134">Tidig</span><span class="sxs-lookup"><span data-stu-id="92623-134">Storm</span></span>
- <span data-ttu-id="92623-135">Få verksamheten</span><span class="sxs-lookup"><span data-stu-id="92623-135">Spark</span></span>
- <span data-ttu-id="92623-136">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="92623-136">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="92623-137">Kafka</span><span class="sxs-lookup"><span data-stu-id="92623-137">Kafka</span></span>
- <span data-ttu-id="92623-138">RServer</span><span class="sxs-lookup"><span data-stu-id="92623-138">RServer</span></span>

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

### <span data-ttu-id="92623-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92623-139">-DefaultProfile</span></span>
<span data-ttu-id="92623-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="92623-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92623-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="92623-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="92623-142">Anger den konto nycklar för standard kontot för Azure Storage som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="92623-142">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="92623-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="92623-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="92623-144">Anger namnet på det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="92623-144">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="92623-145">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="92623-145">-DefaultStorageAccountType</span></span>
<span data-ttu-id="92623-146">Anger typen för det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="92623-146">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="92623-147">Möjliga värden är AzureStorage och AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="92623-147">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="92623-148">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="92623-148">-EdgeNodeSize</span></span>
<span data-ttu-id="92623-149">Anger storleken på den virtuella datorn för noden Edge.</span><span class="sxs-lookup"><span data-stu-id="92623-149">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="92623-150">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="92623-150">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="92623-151">Den här parametern är endast giltig för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="92623-151">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="92623-152">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="92623-152">-HeadNodeSize</span></span>
<span data-ttu-id="92623-153">Anger storleken på den virtuella datorn för Head-noden.</span><span class="sxs-lookup"><span data-stu-id="92623-153">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="92623-154">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="92623-154">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="92623-155">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="92623-155">-HiveMetastore</span></span>
<span data-ttu-id="92623-156">Anger metastore för att lagra Hive-metadata.</span><span class="sxs-lookup"><span data-stu-id="92623-156">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="92623-157">Du kan också använda Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92623-157">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="92623-158">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="92623-158">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="92623-159">Hämtar eller anger den minsta TLS-version som stöds.</span><span class="sxs-lookup"><span data-stu-id="92623-159">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="92623-160">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="92623-160">-ObjectId</span></span>
<span data-ttu-id="92623-161">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="92623-161">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="92623-162">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92623-162">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="92623-163">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="92623-163">-OozieMetastore</span></span>
<span data-ttu-id="92623-164">Anger metastore för att lagra Oozie-metadata.</span><span class="sxs-lookup"><span data-stu-id="92623-164">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="92623-165">Du kan också använda cmdleten **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="92623-165">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="92623-166">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="92623-166">-WorkerNodeSize</span></span>
<span data-ttu-id="92623-167">Anger storleken på den virtuella datorn för arbets tagaren.</span><span class="sxs-lookup"><span data-stu-id="92623-167">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="92623-168">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="92623-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="92623-169">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="92623-169">-ZookeeperNodeSize</span></span>
<span data-ttu-id="92623-170">Anger storleken på den virtuella datorn för noden Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="92623-170">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="92623-171">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="92623-171">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="92623-172">Denna parameter är endast giltig för HBase-och Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="92623-172">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="92623-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92623-173">CommonParameters</span></span>
<span data-ttu-id="92623-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92623-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92623-175">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92623-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92623-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92623-176">INPUTS</span></span>

### <span data-ttu-id="92623-177">Ingen</span><span class="sxs-lookup"><span data-stu-id="92623-177">None</span></span>

## <span data-ttu-id="92623-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92623-178">OUTPUTS</span></span>

### <span data-ttu-id="92623-179">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="92623-179">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="92623-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92623-180">NOTES</span></span>

## <span data-ttu-id="92623-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92623-181">RELATED LINKS</span></span>

[<span data-ttu-id="92623-182">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="92623-182">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


