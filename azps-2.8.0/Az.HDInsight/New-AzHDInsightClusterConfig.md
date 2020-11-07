---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: fad988977cf5fe24e440d654206e0f1a212be6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744075"
---
# <span data-ttu-id="4f088-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4f088-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="4f088-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f088-102">SYNOPSIS</span></span>
<span data-ttu-id="4f088-103">Skapar ett icke beständigt kluster konfigurations objekt som beskriver en Azure HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4f088-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="4f088-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f088-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f088-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f088-105">DESCRIPTION</span></span>
<span data-ttu-id="4f088-106">**New-AzHDInsightClusterConfig-** cmdleten skapar ett icke bevarat objekt som beskriver en Azure HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4f088-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="4f088-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f088-107">EXAMPLES</span></span>

### <span data-ttu-id="4f088-108">Exempel 1: skapa ett kluster konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="4f088-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="4f088-109">Det här kommandot skapar ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="4f088-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="4f088-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f088-110">PARAMETERS</span></span>

### <span data-ttu-id="4f088-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="4f088-111">-AadTenantId</span></span>
<span data-ttu-id="4f088-112">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4f088-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4f088-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4f088-113">-CertificateFileContents</span></span>
<span data-ttu-id="4f088-114">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4f088-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4f088-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4f088-115">-CertificateFilePath</span></span>
<span data-ttu-id="4f088-116">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="4f088-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4f088-117">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4f088-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4f088-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4f088-118">-CertificatePassword</span></span>
<span data-ttu-id="4f088-119">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="4f088-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4f088-120">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4f088-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4f088-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="4f088-121">-ClusterTier</span></span>
<span data-ttu-id="4f088-122">Anger HDInsight-klustrets nivå.</span><span class="sxs-lookup"><span data-stu-id="4f088-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="4f088-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4f088-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f088-124">Standar</span><span class="sxs-lookup"><span data-stu-id="4f088-124">Standard</span></span>
- <span data-ttu-id="4f088-125">Premium är standardvärdet standard.</span><span class="sxs-lookup"><span data-stu-id="4f088-125">Premium The default value is Standard.</span></span>
<span data-ttu-id="4f088-126">Premium-nivån kan bara användas med Linux-kluster och det gör att du kan använda några nya funktioner.</span><span class="sxs-lookup"><span data-stu-id="4f088-126">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="4f088-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="4f088-127">-ClusterType</span></span>
<span data-ttu-id="4f088-128">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4f088-128">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="4f088-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4f088-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f088-130">Hadoop</span><span class="sxs-lookup"><span data-stu-id="4f088-130">Hadoop</span></span>
- <span data-ttu-id="4f088-131">HBase</span><span class="sxs-lookup"><span data-stu-id="4f088-131">HBase</span></span>
- <span data-ttu-id="4f088-132">Tidig</span><span class="sxs-lookup"><span data-stu-id="4f088-132">Storm</span></span>
- <span data-ttu-id="4f088-133">Få verksamheten</span><span class="sxs-lookup"><span data-stu-id="4f088-133">Spark</span></span>

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

### <span data-ttu-id="4f088-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f088-134">-DefaultProfile</span></span>
<span data-ttu-id="4f088-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4f088-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f088-136">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4f088-136">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="4f088-137">Anger den konto nycklar för standard kontot för Azure Storage som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="4f088-137">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="4f088-138">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4f088-138">-DefaultStorageAccountName</span></span>
<span data-ttu-id="4f088-139">Anger namnet på det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="4f088-139">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="4f088-140">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4f088-140">-DefaultStorageAccountType</span></span>
<span data-ttu-id="4f088-141">Anger typen för det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="4f088-141">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="4f088-142">Möjliga värden är AzureStorage och AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="4f088-142">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="4f088-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="4f088-143">-EdgeNodeSize</span></span>
<span data-ttu-id="4f088-144">Anger storleken på den virtuella datorn för noden Edge.</span><span class="sxs-lookup"><span data-stu-id="4f088-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="4f088-145">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="4f088-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="4f088-146">Den här parametern är endast giltig för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="4f088-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="4f088-147">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="4f088-147">-HeadNodeSize</span></span>
<span data-ttu-id="4f088-148">Anger storleken på den virtuella datorn för Head-noden.</span><span class="sxs-lookup"><span data-stu-id="4f088-148">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="4f088-149">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="4f088-149">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4f088-150">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="4f088-150">-HiveMetastore</span></span>
<span data-ttu-id="4f088-151">Anger metastore för att lagra Hive-metadata.</span><span class="sxs-lookup"><span data-stu-id="4f088-151">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="4f088-152">Du kan också använda Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f088-152">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="4f088-153">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4f088-153">-ObjectId</span></span>
<span data-ttu-id="4f088-154">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="4f088-154">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="4f088-155">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4f088-155">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4f088-156">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="4f088-156">-OozieMetastore</span></span>
<span data-ttu-id="4f088-157">Anger metastore för att lagra Oozie-metadata.</span><span class="sxs-lookup"><span data-stu-id="4f088-157">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="4f088-158">Du kan också använda cmdleten **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="4f088-158">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="4f088-159">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="4f088-159">-WorkerNodeSize</span></span>
<span data-ttu-id="4f088-160">Anger storleken på den virtuella datorn för arbets tagaren.</span><span class="sxs-lookup"><span data-stu-id="4f088-160">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="4f088-161">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="4f088-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4f088-162">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="4f088-162">-ZookeeperNodeSize</span></span>
<span data-ttu-id="4f088-163">Anger storleken på den virtuella datorn för noden Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="4f088-163">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="4f088-164">Använd Get-AzVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="4f088-164">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="4f088-165">Denna parameter är endast giltig för HBase-och Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="4f088-165">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="4f088-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f088-166">CommonParameters</span></span>
<span data-ttu-id="4f088-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f088-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f088-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f088-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f088-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f088-169">INPUTS</span></span>

### <span data-ttu-id="4f088-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="4f088-170">None</span></span>

## <span data-ttu-id="4f088-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f088-171">OUTPUTS</span></span>

### <span data-ttu-id="4f088-172">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4f088-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4f088-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f088-173">NOTES</span></span>

## <span data-ttu-id="4f088-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f088-174">RELATED LINKS</span></span>

[<span data-ttu-id="4f088-175">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="4f088-175">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


