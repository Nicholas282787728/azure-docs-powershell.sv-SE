---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
ms.openlocfilehash: a0c534042df15d4ef999b47a5e468b1e13a8d14f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758070"
---
# <span data-ttu-id="44cf8-101">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="44cf8-101">Set-AzureRmHDInsightDefaultStorage</span></span>

## <span data-ttu-id="44cf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="44cf8-103">Anger standardinställning för lagrings konto i ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="44cf8-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44cf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44cf8-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44cf8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44cf8-105">DESCRIPTION</span></span>
<span data-ttu-id="44cf8-106">Cmdleten **set-AzureRmHDInsightDefaultStorage** anger standardinställning för lagrings konto i det kluster konfigurations objekt för Azure HDInsight som skapas av New-AzureRmHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44cf8-106">The **Set-AzureRmHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="44cf8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44cf8-107">EXAMPLES</span></span>

### <span data-ttu-id="44cf8-108">Exempel 1: Ange standard lagrings kontot för klustrets konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="44cf8-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Set-AzureRmHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="44cf8-109">Det här kommandot anger standard lagrings kontot för ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="44cf8-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="44cf8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44cf8-110">PARAMETERS</span></span>

### <span data-ttu-id="44cf8-111">-Config</span><span class="sxs-lookup"><span data-stu-id="44cf8-111">-Config</span></span>
<span data-ttu-id="44cf8-112">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="44cf8-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="44cf8-113">Det här objektet skapas av cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="44cf8-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="44cf8-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="44cf8-114">-StorageAccountKey</span></span>
<span data-ttu-id="44cf8-115">Anger den konto nycklar för standard kontot för Azure Storage som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="44cf8-115">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44cf8-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="44cf8-116">-StorageAccountName</span></span>
<span data-ttu-id="44cf8-117">Anger namnet på det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="44cf8-117">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="44cf8-118">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="44cf8-118">-StorageAccountType</span></span>
<span data-ttu-id="44cf8-119">Hämtar eller anger typen av standard lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="44cf8-119">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="44cf8-120">Standard är AzureStorage</span><span class="sxs-lookup"><span data-stu-id="44cf8-120">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44cf8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44cf8-121">-DefaultProfile</span></span>
<span data-ttu-id="44cf8-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44cf8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44cf8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44cf8-123">CommonParameters</span></span>
<span data-ttu-id="44cf8-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44cf8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44cf8-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44cf8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44cf8-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44cf8-126">INPUTS</span></span>

### <span data-ttu-id="44cf8-127">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="44cf8-127">AzureHDInsightConfig</span></span>
<span data-ttu-id="44cf8-128">Parametern ' config ' godkänner värdet av typen ' AzureHDInsightConfig ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="44cf8-128">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="44cf8-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44cf8-129">OUTPUTS</span></span>

### <span data-ttu-id="44cf8-130">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="44cf8-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="44cf8-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44cf8-131">NOTES</span></span>

## <span data-ttu-id="44cf8-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44cf8-132">RELATED LINKS</span></span>

