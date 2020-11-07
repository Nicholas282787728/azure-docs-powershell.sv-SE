---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
ms.openlocfilehash: bc9b5a05111fff64b41400093d1f9c1ba3c2df8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576520"
---
# <span data-ttu-id="d88f1-101">Add-AzureRmHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="d88f1-101">Add-AzureRmHDInsightMetastore</span></span>

## <span data-ttu-id="d88f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d88f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d88f1-103">Lägger till en SQL-databas som ska fungera som en registrerings-eller Oozie-metastore till ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="d88f1-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d88f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d88f1-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d88f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d88f1-105">DESCRIPTION</span></span>
<span data-ttu-id="d88f1-106">Cmdleten **Add-AzureRmHDInsightMetastore** lägger till en registrerings data fil eller ett Oozie metastore i HDInsight-konfigurationsobjektet som skapas av New-AzureRmHDInsightClusterConfig cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d88f1-106">The **Add-AzureRmHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="d88f1-107">En metastore är en SQL-databas som kan användas för att lagra metadata för Hive, Oozie eller båda.</span><span class="sxs-lookup"><span data-stu-id="d88f1-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="d88f1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d88f1-108">EXAMPLES</span></span>

### <span data-ttu-id="d88f1-109">Exempel 1: lägga till en SQL-databas metastore i klustret</span><span class="sxs-lookup"><span data-stu-id="d88f1-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
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

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
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

<span data-ttu-id="d88f1-110">Det här kommandot lägger till en SQL-metastore till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="d88f1-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d88f1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d88f1-111">PARAMETERS</span></span>

### <span data-ttu-id="d88f1-112">-Config</span><span class="sxs-lookup"><span data-stu-id="d88f1-112">-Config</span></span>
<span data-ttu-id="d88f1-113">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="d88f1-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="d88f1-114">Det här objektet skapas av cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="d88f1-114">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d88f1-115">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="d88f1-115">-Credential</span></span>
<span data-ttu-id="d88f1-116">Anger de autentiseringsuppgifter som ska användas för AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="d88f1-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88f1-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d88f1-117">-DatabaseName</span></span>
<span data-ttu-id="d88f1-118">Anger vilken databas på AzureSQL Server-instansen som ska användas för den här metastore.</span><span class="sxs-lookup"><span data-stu-id="d88f1-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88f1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d88f1-119">-DefaultProfile</span></span>
<span data-ttu-id="d88f1-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d88f1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88f1-121">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="d88f1-121">-MetastoreType</span></span>
<span data-ttu-id="d88f1-122">Anger typen av metastore.</span><span class="sxs-lookup"><span data-stu-id="d88f1-122">Specifies the type of metastore.</span></span>
<span data-ttu-id="d88f1-123">Möjliga värden är HiveMetastore eller OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="d88f1-123">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88f1-124">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="d88f1-124">-SqlAzureServerName</span></span>
<span data-ttu-id="d88f1-125">Anger den AzureSQL-serverinstans som ska användas för den här metastore.</span><span class="sxs-lookup"><span data-stu-id="d88f1-125">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88f1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88f1-126">CommonParameters</span></span>
<span data-ttu-id="d88f1-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d88f1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88f1-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d88f1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88f1-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d88f1-129">INPUTS</span></span>

### <span data-ttu-id="d88f1-130">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d88f1-130">AzureHDInsightConfig</span></span>
<span data-ttu-id="d88f1-131">Parametern ' config ' godkänner värdet av typen ' AzureHDInsightConfig ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d88f1-131">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="d88f1-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d88f1-132">OUTPUTS</span></span>

### <span data-ttu-id="d88f1-133">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d88f1-133">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d88f1-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d88f1-134">NOTES</span></span>

## <span data-ttu-id="d88f1-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d88f1-135">RELATED LINKS</span></span>

[<span data-ttu-id="d88f1-136">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d88f1-136">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

