---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: d02dce12425015ed12e082f0bb3ba52c5b9b77c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572736"
---
# <span data-ttu-id="c51e6-101">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="c51e6-101">Add-AzureRmHDInsightClusterIdentity</span></span>

## <span data-ttu-id="c51e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c51e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c51e6-103">Lägger till en kluster identitet till ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="c51e6-103">Adds a cluster identity to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c51e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c51e6-104">SYNTAX</span></span>

### <span data-ttu-id="c51e6-105">CertificateFilePath (standard)</span><span class="sxs-lookup"><span data-stu-id="c51e6-105">CertificateFilePath (Default)</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c51e6-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c51e6-106">CertificateFileContents</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c51e6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c51e6-107">DESCRIPTION</span></span>
<span data-ttu-id="c51e6-108">Cmdleten **Add-AzureRmHDInsightClusterIdentity** lägger till en kluster identitet i Azure HDInsight-konfigurationsobjektet som skapas av New-AzureRmHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c51e6-108">The **Add-AzureRmHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="c51e6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c51e6-109">EXAMPLES</span></span>

### <span data-ttu-id="c51e6-110">Exempel 1: lägga till information om kluster identitet i konfigurationsobjektet för kluster</span><span class="sxs-lookup"><span data-stu-id="c51e6-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzureRmContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="c51e6-111">Det här kommandot lägger till information om kluster identitet till det kluster som heter din-Hadoop-001 och låter klustret komma åt Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c51e6-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="c51e6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c51e6-112">PARAMETERS</span></span>

### <span data-ttu-id="c51e6-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="c51e6-113">-AadTenantId</span></span>
<span data-ttu-id="c51e6-114">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c51e6-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c51e6-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c51e6-115">-CertificateFileContents</span></span>
<span data-ttu-id="c51e6-116">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c51e6-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c51e6-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c51e6-117">-CertificateFilePath</span></span>
<span data-ttu-id="c51e6-118">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="c51e6-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c51e6-119">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c51e6-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c51e6-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c51e6-120">-CertificatePassword</span></span>
<span data-ttu-id="c51e6-121">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="c51e6-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c51e6-122">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c51e6-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c51e6-123">-Config</span><span class="sxs-lookup"><span data-stu-id="c51e6-123">-Config</span></span>
<span data-ttu-id="c51e6-124">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="c51e6-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="c51e6-125">Det här objektet skapas av New-AzureRmHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c51e6-125">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c51e6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c51e6-126">-DefaultProfile</span></span>
<span data-ttu-id="c51e6-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c51e6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c51e6-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c51e6-128">-ObjectId</span></span>
<span data-ttu-id="c51e6-129">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="c51e6-129">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="c51e6-130">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c51e6-130">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c51e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c51e6-131">CommonParameters</span></span>
<span data-ttu-id="c51e6-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c51e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c51e6-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c51e6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c51e6-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c51e6-134">INPUTS</span></span>

### <span data-ttu-id="c51e6-135">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c51e6-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="c51e6-136">Parametrar: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c51e6-136">Parameters: Config (ByValue)</span></span>

### <span data-ttu-id="c51e6-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c51e6-137">System.Guid</span></span>
<span data-ttu-id="c51e6-138">Parametrar: ObjectId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c51e6-138">Parameters: ObjectId (ByValue)</span></span>

## <span data-ttu-id="c51e6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c51e6-139">OUTPUTS</span></span>

### <span data-ttu-id="c51e6-140">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c51e6-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c51e6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c51e6-141">NOTES</span></span>

## <span data-ttu-id="c51e6-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c51e6-142">RELATED LINKS</span></span>

[<span data-ttu-id="c51e6-143">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c51e6-143">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


