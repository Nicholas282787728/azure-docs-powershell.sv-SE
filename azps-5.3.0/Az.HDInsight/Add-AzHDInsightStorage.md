---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 6db3c5b5d899f9b7a32e6dbb20c280590bea93c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520644"
---
# <span data-ttu-id="5033e-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="5033e-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="5033e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5033e-102">SYNOPSIS</span></span>
<span data-ttu-id="5033e-103">Lägger till en Azure-lagringsenhet till ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="5033e-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="5033e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5033e-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5033e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5033e-105">DESCRIPTION</span></span>
<span data-ttu-id="5033e-106">Cmdleten **Add-AzHDInsightStorage** lägger till en Azure Storage-loggpost i Azure HDInsight-konfigurationsobjektet som skapas av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5033e-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="5033e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5033e-107">EXAMPLES</span></span>

### <span data-ttu-id="5033e-108">Exempel 1: lägga till en Azure Storage-plats i klustrets konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="5033e-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="5033e-109">Det här kommandot lägger till en post för en BLOB-lagringsenhet i HDInsight-konfigurationen som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="5033e-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="5033e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5033e-110">PARAMETERS</span></span>

### <span data-ttu-id="5033e-111">-Config</span><span class="sxs-lookup"><span data-stu-id="5033e-111">-Config</span></span>
<span data-ttu-id="5033e-112">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="5033e-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="5033e-113">Det här objektet skapas av cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="5033e-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="5033e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5033e-114">-DefaultProfile</span></span>
<span data-ttu-id="5033e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5033e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5033e-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5033e-116">-StorageAccountKey</span></span>
<span data-ttu-id="5033e-117">Anger lagrings konto för lagrings konto som ska läggas till i det nya klustret.</span><span class="sxs-lookup"><span data-stu-id="5033e-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="5033e-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5033e-118">-StorageAccountName</span></span>
<span data-ttu-id="5033e-119">Anger namnet på lagrings kontot för det lagrings konto som ska läggas till i klustret.</span><span class="sxs-lookup"><span data-stu-id="5033e-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="5033e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5033e-120">CommonParameters</span></span>
<span data-ttu-id="5033e-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5033e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5033e-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5033e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5033e-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5033e-123">INPUTS</span></span>

### <span data-ttu-id="5033e-124">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="5033e-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="5033e-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5033e-125">OUTPUTS</span></span>

### <span data-ttu-id="5033e-126">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="5033e-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="5033e-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5033e-127">NOTES</span></span>

## <span data-ttu-id="5033e-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5033e-128">RELATED LINKS</span></span>

[<span data-ttu-id="5033e-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="5033e-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


