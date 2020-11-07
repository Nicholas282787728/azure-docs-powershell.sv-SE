---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 035b21684c3d8fc64cee7ee78b7b4cb2adf21f01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916677"
---
# <span data-ttu-id="9f67e-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="9f67e-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="9f67e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f67e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f67e-103">Lägger till en kluster identitet till ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="9f67e-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="9f67e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f67e-104">SYNTAX</span></span>

### <span data-ttu-id="9f67e-105">CertificateFilePath (standard)</span><span class="sxs-lookup"><span data-stu-id="9f67e-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f67e-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="9f67e-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f67e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f67e-107">DESCRIPTION</span></span>
<span data-ttu-id="9f67e-108">Cmdleten **Add-AzHDInsightClusterIdentity** lägger till en kluster identitet i Azure HDInsight-konfigurationsobjektet som skapas av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f67e-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="9f67e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f67e-109">EXAMPLES</span></span>

### <span data-ttu-id="9f67e-110">Exempel 1: lägga till information om kluster identitet i konfigurationsobjektet för kluster</span><span class="sxs-lookup"><span data-stu-id="9f67e-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
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

<span data-ttu-id="9f67e-111">Det här kommandot lägger till information om kluster identitet till det kluster som heter din-Hadoop-001 och låter klustret komma åt Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9f67e-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="9f67e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f67e-112">PARAMETERS</span></span>

### <span data-ttu-id="9f67e-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="9f67e-113">-AadTenantId</span></span>
<span data-ttu-id="9f67e-114">Anger det Azure AD Tenant-ID som kommer att användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9f67e-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="9f67e-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="9f67e-115">-CertificateFileContents</span></span>
<span data-ttu-id="9f67e-116">Anger fil innehållet för det certifikat som ska användas vid åtkomst till Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9f67e-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="9f67e-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="9f67e-117">-CertificateFilePath</span></span>
<span data-ttu-id="9f67e-118">Anger sökvägen till det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="9f67e-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="9f67e-119">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9f67e-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="9f67e-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="9f67e-120">-CertificatePassword</span></span>
<span data-ttu-id="9f67e-121">Anger lösen ordet för det certifikat som ska användas för att autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="9f67e-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="9f67e-122">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9f67e-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="9f67e-123">-Config</span><span class="sxs-lookup"><span data-stu-id="9f67e-123">-Config</span></span>
<span data-ttu-id="9f67e-124">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="9f67e-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="9f67e-125">Det här objektet skapas av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f67e-125">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="9f67e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f67e-126">-DefaultProfile</span></span>
<span data-ttu-id="9f67e-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9f67e-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f67e-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9f67e-128">-ObjectId</span></span>
<span data-ttu-id="9f67e-129">Anger Azure AD-huvudobjekt-ID (ett GUID) för Azure AD-huvudtjänstens huvud namn som representerar klustret.</span><span class="sxs-lookup"><span data-stu-id="9f67e-129">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="9f67e-130">Klustret använder det här när du använder Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9f67e-130">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="9f67e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f67e-131">CommonParameters</span></span>
<span data-ttu-id="9f67e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f67e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f67e-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f67e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f67e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f67e-134">INPUTS</span></span>

### <span data-ttu-id="9f67e-135">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="9f67e-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="9f67e-136">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9f67e-136">System.Guid</span></span>

## <span data-ttu-id="9f67e-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f67e-137">OUTPUTS</span></span>

### <span data-ttu-id="9f67e-138">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="9f67e-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="9f67e-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f67e-139">NOTES</span></span>

## <span data-ttu-id="9f67e-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f67e-140">RELATED LINKS</span></span>

[<span data-ttu-id="9f67e-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="9f67e-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


