---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: f8971070851da36fb1bf72aef33085e974ef1fb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102863"
---
# <span data-ttu-id="83316-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="83316-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="83316-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83316-102">SYNOPSIS</span></span>
<span data-ttu-id="83316-103">Lägger till en SQL-databas som ska fungera som en registrerings-eller Oozie-metastore till ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="83316-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="83316-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83316-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83316-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83316-105">DESCRIPTION</span></span>
<span data-ttu-id="83316-106">Cmdleten **Add-AzHDInsightMetastore** lägger till en registrerings data fil eller ett Oozie metastore i HDInsight-konfigurationsobjektet som skapas av New-AzHDInsightClusterConfig cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83316-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="83316-107">En metastore är en SQL-databas som kan användas för att lagra metadata för Hive, Oozie eller båda.</span><span class="sxs-lookup"><span data-stu-id="83316-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="83316-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83316-108">EXAMPLES</span></span>

### <span data-ttu-id="83316-109">Exempel 1: lägga till en SQL-databas metastore i klustret</span><span class="sxs-lookup"><span data-stu-id="83316-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="83316-110">Det här kommandot lägger till en SQL-metastore till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="83316-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="83316-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83316-111">PARAMETERS</span></span>

### <span data-ttu-id="83316-112">-Config</span><span class="sxs-lookup"><span data-stu-id="83316-112">-Config</span></span>
<span data-ttu-id="83316-113">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="83316-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="83316-114">Det här objektet skapas av cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="83316-114">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="83316-115">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="83316-115">-Credential</span></span>
<span data-ttu-id="83316-116">Anger de autentiseringsuppgifter som ska användas för AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="83316-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

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

### <span data-ttu-id="83316-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="83316-117">-DatabaseName</span></span>
<span data-ttu-id="83316-118">Anger vilken databas på AzureSQL Server-instansen som ska användas för den här metastore.</span><span class="sxs-lookup"><span data-stu-id="83316-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="83316-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83316-119">-DefaultProfile</span></span>
<span data-ttu-id="83316-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="83316-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83316-121">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="83316-121">-MetastoreType</span></span>
<span data-ttu-id="83316-122">Anger typen av metastore.</span><span class="sxs-lookup"><span data-stu-id="83316-122">Specifies the type of metastore.</span></span>
<span data-ttu-id="83316-123">Möjliga värden är HiveMetastore eller OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="83316-123">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83316-124">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="83316-124">-SqlAzureServerName</span></span>
<span data-ttu-id="83316-125">Anger den AzureSQL-serverinstans som ska användas för den här metastore.</span><span class="sxs-lookup"><span data-stu-id="83316-125">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="83316-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83316-126">CommonParameters</span></span>
<span data-ttu-id="83316-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83316-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83316-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83316-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83316-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83316-129">INPUTS</span></span>

### <span data-ttu-id="83316-130">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="83316-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="83316-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83316-131">OUTPUTS</span></span>

### <span data-ttu-id="83316-132">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="83316-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="83316-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83316-133">NOTES</span></span>

## <span data-ttu-id="83316-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83316-134">RELATED LINKS</span></span>

[<span data-ttu-id="83316-135">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="83316-135">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


