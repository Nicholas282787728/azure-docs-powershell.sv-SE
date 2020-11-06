---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
ms.openlocfilehash: f70403f70e116a0e6addc569942f927aca0dcf0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580619"
---
# <span data-ttu-id="1471c-101">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="1471c-101">Add-AzureRmHDInsightStorage</span></span>

## <span data-ttu-id="1471c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1471c-102">SYNOPSIS</span></span>
<span data-ttu-id="1471c-103">Lägger till en Azure-lagringsenhet till ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="1471c-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1471c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1471c-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1471c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1471c-105">DESCRIPTION</span></span>
<span data-ttu-id="1471c-106">Cmdleten **Add-AzureRmHDInsightStorage** lägger till en Azure Storage-loggpost i Azure HDInsight-konfigurationsobjektet som skapas av New-AzureRmHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1471c-106">The **Add-AzureRmHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="1471c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1471c-107">EXAMPLES</span></span>

### <span data-ttu-id="1471c-108">Exempel 1: lägga till en Azure Storage-plats i klustrets konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="1471c-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzureRmStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="1471c-109">Det här kommandot lägger till en post för en BLOB-lagringsenhet i HDInsight-konfigurationen som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="1471c-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="1471c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1471c-110">PARAMETERS</span></span>

### <span data-ttu-id="1471c-111">-Config</span><span class="sxs-lookup"><span data-stu-id="1471c-111">-Config</span></span>
<span data-ttu-id="1471c-112">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="1471c-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="1471c-113">Det här objektet skapas av cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="1471c-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="1471c-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1471c-114">-StorageAccountKey</span></span>
<span data-ttu-id="1471c-115">Anger lagrings konto för lagrings konto som ska läggas till i det nya klustret.</span><span class="sxs-lookup"><span data-stu-id="1471c-115">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="1471c-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1471c-116">-StorageAccountName</span></span>
<span data-ttu-id="1471c-117">Anger namnet på lagrings kontot för det lagrings konto som ska läggas till i klustret.</span><span class="sxs-lookup"><span data-stu-id="1471c-117">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="1471c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1471c-118">-DefaultProfile</span></span>
<span data-ttu-id="1471c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1471c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1471c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1471c-120">CommonParameters</span></span>
<span data-ttu-id="1471c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1471c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1471c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1471c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1471c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1471c-123">INPUTS</span></span>

### <span data-ttu-id="1471c-124">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="1471c-124">AzureHDInsightConfig</span></span>
<span data-ttu-id="1471c-125">Parametern ' config ' godkänner värdet av typen ' AzureHDInsightConfig ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="1471c-125">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="1471c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1471c-126">OUTPUTS</span></span>

### <span data-ttu-id="1471c-127">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="1471c-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="1471c-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1471c-128">NOTES</span></span>

## <span data-ttu-id="1471c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1471c-129">RELATED LINKS</span></span>

[<span data-ttu-id="1471c-130">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="1471c-130">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


