---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: 8102a9ce8ef1117822426d6896edf95d21c46607
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523609"
---
# <span data-ttu-id="98e9b-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="98e9b-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="98e9b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="98e9b-103">Lägger till en SQL-databas som ska fungera som en registrerings-eller Oozie-metastore till ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="98e9b-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="98e9b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98e9b-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98e9b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98e9b-105">DESCRIPTION</span></span>
<span data-ttu-id="98e9b-106">Cmdleten **Add-AzHDInsightMetastore** lägger till en registrerings data fil eller ett Oozie metastore i HDInsight-konfigurationsobjektet som skapas av New-AzHDInsightClusterConfig cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98e9b-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="98e9b-107">En metastore är en SQL-databas som kan användas för att lagra metadata för Hive, Oozie eller båda.</span><span class="sxs-lookup"><span data-stu-id="98e9b-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="98e9b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98e9b-108">EXAMPLES</span></span>

### <span data-ttu-id="98e9b-109">Exempel 1: lägga till en SQL-databas metastore i klustret</span><span class="sxs-lookup"><span data-stu-id="98e9b-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
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

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
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

<span data-ttu-id="98e9b-110">Det här kommandot lägger till en SQL-metastore till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="98e9b-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

### <span data-ttu-id="98e9b-111">Exempel 2: lägga till en anpassad Ambari-databas i ett kluster konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="98e9b-111">Example 2: Add a custom Ambari database to the cluster configuration object</span></span>
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
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Custom Amari database info
PS C:\> $ambariSqlServer = "your-sqlserver-001"
PS C:\> $ambariDb = "your-sqldb-003"
PS C:\> $ambariCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$ambariSqlServer.database.contoso.net" `
                -DatabaseName $ambariDb `
                -Credential $ambariCreds `
                -MetastoreType AmbariDatabase `
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

<span data-ttu-id="98e9b-112">Det här kommandot lägger till en anpassad Ambari-databas till det kluster som heter ditt-Hadoop-002.</span><span class="sxs-lookup"><span data-stu-id="98e9b-112">This command adds a custom Ambari database to the cluster named your-hadoop-002.</span></span>

## <span data-ttu-id="98e9b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98e9b-113">PARAMETERS</span></span>

### <span data-ttu-id="98e9b-114">-Config</span><span class="sxs-lookup"><span data-stu-id="98e9b-114">-Config</span></span>
<span data-ttu-id="98e9b-115">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="98e9b-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="98e9b-116">Det här objektet skapas av cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="98e9b-116">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="98e9b-117">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="98e9b-117">-Credential</span></span>
<span data-ttu-id="98e9b-118">Anger de autentiseringsuppgifter som ska användas för AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="98e9b-118">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e9b-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="98e9b-119">-DatabaseName</span></span>
<span data-ttu-id="98e9b-120">Anger vilken databas på AzureSQL Server-instansen som ska användas för den här metastore.</span><span class="sxs-lookup"><span data-stu-id="98e9b-120">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="98e9b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e9b-121">-DefaultProfile</span></span>
<span data-ttu-id="98e9b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="98e9b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98e9b-123">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="98e9b-123">-MetastoreType</span></span>
<span data-ttu-id="98e9b-124">Anger typen av metastore.</span><span class="sxs-lookup"><span data-stu-id="98e9b-124">Specifies the type of metastore.</span></span>
<span data-ttu-id="98e9b-125">Möjliga värden är HiveMetastore eller OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="98e9b-125">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore, AmbariDatabase

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e9b-126">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="98e9b-126">-SqlAzureServerName</span></span>
<span data-ttu-id="98e9b-127">Anger den AzureSQL-serverinstans som ska användas för den här metastore.</span><span class="sxs-lookup"><span data-stu-id="98e9b-127">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="98e9b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e9b-128">CommonParameters</span></span>
<span data-ttu-id="98e9b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98e9b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e9b-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98e9b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e9b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98e9b-131">INPUTS</span></span>

### <span data-ttu-id="98e9b-132">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="98e9b-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="98e9b-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98e9b-133">OUTPUTS</span></span>

### <span data-ttu-id="98e9b-134">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="98e9b-134">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="98e9b-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98e9b-135">NOTES</span></span>

## <span data-ttu-id="98e9b-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98e9b-136">RELATED LINKS</span></span>

[<span data-ttu-id="98e9b-137">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="98e9b-137">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


