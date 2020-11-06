---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 381143b356202a7b6b76e173b233f2fffe87f6a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585560"
---
# <span data-ttu-id="06237-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="06237-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="06237-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06237-102">SYNOPSIS</span></span>
<span data-ttu-id="06237-103">Skapar ett icke beständigt kluster konfigurations objekt som beskriver en Azure HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="06237-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06237-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06237-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06237-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06237-105">DESCRIPTION</span></span>
<span data-ttu-id="06237-106">**New-AzureRmHDInsightClusterConfig-** cmdleten skapar ett icke bevarat objekt som beskriver en Azure HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="06237-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="06237-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06237-107">EXAMPLES</span></span>

### <span data-ttu-id="06237-108">Exempel 1: skapa ett kluster konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="06237-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="06237-109">Det här kommandot skapar ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="06237-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="06237-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06237-110">PARAMETERS</span></span>

### <span data-ttu-id="06237-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="06237-111">-AadTenantId</span></span>
<span data-ttu-id="06237-112">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="06237-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="06237-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="06237-113">-CertificateFileContents</span></span>
<span data-ttu-id="06237-114">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="06237-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="06237-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="06237-115">-CertificateFilePath</span></span>
<span data-ttu-id="06237-116">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="06237-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="06237-117">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="06237-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="06237-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="06237-118">-CertificatePassword</span></span>
<span data-ttu-id="06237-119">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="06237-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="06237-120">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="06237-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="06237-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="06237-121">-ClusterTier</span></span>
<span data-ttu-id="06237-122">Anger HDInsight-klustrets nivå.</span><span class="sxs-lookup"><span data-stu-id="06237-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="06237-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="06237-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06237-124">Standar</span><span class="sxs-lookup"><span data-stu-id="06237-124">Standard</span></span>
- <span data-ttu-id="06237-125">Beta</span><span class="sxs-lookup"><span data-stu-id="06237-125">Premium</span></span>

<span data-ttu-id="06237-126">Standardvärdet är standard.</span><span class="sxs-lookup"><span data-stu-id="06237-126">The default value is Standard.</span></span>
<span data-ttu-id="06237-127">Premium-nivån kan bara användas med Linux-kluster och det gör att du kan använda några nya funktioner.</span><span class="sxs-lookup"><span data-stu-id="06237-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="06237-128">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="06237-128">-ClusterType</span></span>
<span data-ttu-id="06237-129">Anger vilken typ av kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="06237-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="06237-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="06237-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06237-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="06237-131">Hadoop</span></span>
- <span data-ttu-id="06237-132">HBase</span><span class="sxs-lookup"><span data-stu-id="06237-132">HBase</span></span>
- <span data-ttu-id="06237-133">Tidig</span><span class="sxs-lookup"><span data-stu-id="06237-133">Storm</span></span>
- <span data-ttu-id="06237-134">Få verksamheten</span><span class="sxs-lookup"><span data-stu-id="06237-134">Spark</span></span>

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

### <span data-ttu-id="06237-135">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="06237-135">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="06237-136">Anger den konto nycklar för standard kontot för Azure Storage som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="06237-136">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="06237-137">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="06237-137">-DefaultStorageAccountName</span></span>
<span data-ttu-id="06237-138">Anger namnet på det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="06237-138">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="06237-139">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="06237-139">-DefaultStorageAccountType</span></span>
<span data-ttu-id="06237-140">Anger typen för det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="06237-140">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="06237-141">Möjliga värden är AzureStorage och AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="06237-141">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="06237-142">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="06237-142">-EdgeNodeSize</span></span>
<span data-ttu-id="06237-143">Anger storleken på den virtuella datorn för noden Edge.</span><span class="sxs-lookup"><span data-stu-id="06237-143">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="06237-144">Använd Get-AzureRmVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="06237-144">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="06237-145">Den här parametern är endast giltig för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="06237-145">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="06237-146">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="06237-146">-HeadNodeSize</span></span>
<span data-ttu-id="06237-147">Anger storleken på den virtuella datorn för Head-noden.</span><span class="sxs-lookup"><span data-stu-id="06237-147">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="06237-148">Använd Get-AzureRMVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="06237-148">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="06237-149">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="06237-149">-HiveMetastore</span></span>
<span data-ttu-id="06237-150">Anger metastore för att lagra Hive-metadata.</span><span class="sxs-lookup"><span data-stu-id="06237-150">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="06237-151">Du kan också använda Add-AzureRmHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06237-151">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="06237-152">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="06237-152">-ObjectId</span></span>
<span data-ttu-id="06237-153">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="06237-153">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="06237-154">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="06237-154">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="06237-155">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="06237-155">-OozieMetastore</span></span>
<span data-ttu-id="06237-156">Anger metastore för att lagra Oozie-metadata.</span><span class="sxs-lookup"><span data-stu-id="06237-156">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="06237-157">Du kan också använda cmdleten **Add-AzureRmHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="06237-157">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="06237-158">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="06237-158">-WorkerNodeSize</span></span>
<span data-ttu-id="06237-159">Anger storleken på den virtuella datorn för arbets tagaren.</span><span class="sxs-lookup"><span data-stu-id="06237-159">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="06237-160">Använd Get-AzureRMVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="06237-160">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="06237-161">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="06237-161">-ZookeeperNodeSize</span></span>
<span data-ttu-id="06237-162">Anger storleken på den virtuella datorn för noden Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="06237-162">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="06237-163">Använd Get-AzureRMVMSize för acceptabla virtuella dator storlekar och se HDInsight-sidans prissättning.</span><span class="sxs-lookup"><span data-stu-id="06237-163">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="06237-164">Denna parameter är endast giltig för HBase-och Storm-kluster.</span><span class="sxs-lookup"><span data-stu-id="06237-164">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="06237-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06237-165">-DefaultProfile</span></span>
<span data-ttu-id="06237-166">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06237-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06237-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06237-167">CommonParameters</span></span>
<span data-ttu-id="06237-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06237-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06237-169">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06237-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06237-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06237-170">INPUTS</span></span>

## <span data-ttu-id="06237-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06237-171">OUTPUTS</span></span>

### <span data-ttu-id="06237-172">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="06237-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="06237-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06237-173">NOTES</span></span>

## <span data-ttu-id="06237-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06237-174">RELATED LINKS</span></span>

[<span data-ttu-id="06237-175">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="06237-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


