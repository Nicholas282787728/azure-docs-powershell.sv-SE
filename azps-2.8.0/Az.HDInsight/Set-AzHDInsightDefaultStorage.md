---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 6815e697376f51d70782885485541debb209ecf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744053"
---
# <span data-ttu-id="cf2cb-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="cf2cb-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="cf2cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2cb-103">Anger standardinställning för lagrings konto i ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="cf2cb-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="cf2cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf2cb-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf2cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf2cb-105">DESCRIPTION</span></span>
<span data-ttu-id="cf2cb-106">Cmdleten **set-AzHDInsightDefaultStorage** anger standardinställning för lagrings konto i det kluster konfigurations objekt för Azure HDInsight som skapas av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf2cb-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="cf2cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf2cb-107">EXAMPLES</span></span>

### <span data-ttu-id="cf2cb-108">Exempel 1: Ange standard lagrings kontot för klustrets konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="cf2cb-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Set-AzHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="cf2cb-109">Det här kommandot anger standard lagrings kontot för ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="cf2cb-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="cf2cb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf2cb-110">PARAMETERS</span></span>

### <span data-ttu-id="cf2cb-111">-Config</span><span class="sxs-lookup"><span data-stu-id="cf2cb-111">-Config</span></span>
<span data-ttu-id="cf2cb-112">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="cf2cb-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="cf2cb-113">Det här objektet skapas av cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="cf2cb-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="cf2cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2cb-114">-DefaultProfile</span></span>
<span data-ttu-id="cf2cb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cf2cb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf2cb-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cf2cb-116">-StorageAccountKey</span></span>
<span data-ttu-id="cf2cb-117">Anger den konto nycklar för standard kontot för Azure Storage som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="cf2cb-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="cf2cb-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cf2cb-118">-StorageAccountName</span></span>
<span data-ttu-id="cf2cb-119">Anger namnet på det standard lagrings konto som HDInsight-klustret kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="cf2cb-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="cf2cb-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="cf2cb-120">-StorageAccountType</span></span>
<span data-ttu-id="cf2cb-121">Hämtar eller anger typen av standard lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="cf2cb-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="cf2cb-122">Standard är AzureStorage</span><span class="sxs-lookup"><span data-stu-id="cf2cb-122">Defaults to AzureStorage</span></span>

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

### <span data-ttu-id="cf2cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2cb-123">CommonParameters</span></span>
<span data-ttu-id="cf2cb-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf2cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2cb-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf2cb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2cb-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf2cb-126">INPUTS</span></span>

### <span data-ttu-id="cf2cb-127">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="cf2cb-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="cf2cb-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf2cb-128">OUTPUTS</span></span>

### <span data-ttu-id="cf2cb-129">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="cf2cb-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="cf2cb-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf2cb-130">NOTES</span></span>

## <span data-ttu-id="cf2cb-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf2cb-131">RELATED LINKS</span></span>