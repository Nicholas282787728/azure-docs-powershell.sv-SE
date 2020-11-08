---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263117"
---
# <span data-ttu-id="19e6b-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="19e6b-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="19e6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="19e6b-103">Lägger till ett konfigurations värde för Hadoop-konfigurering och/eller en struktur för ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="19e6b-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="19e6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19e6b-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19e6b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19e6b-105">DESCRIPTION</span></span>
<span data-ttu-id="19e6b-106">Cmdleten **Add-AzHDInsightConfigValue** lägger till en konfiguration för Hadoop-konfigurationsinställningar, till exempel core-site.xml eller hive-site.xml, och/eller en struktur för att skapa ett delat bibliotek för HDInsight-konfigurationsobjekt som skapas av New-AzHDInsightClusterConfig cmdleten.</span><span class="sxs-lookup"><span data-stu-id="19e6b-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="19e6b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19e6b-107">EXAMPLES</span></span>

### <span data-ttu-id="19e6b-108">Exempel 1: lägga till ett anpassat konfigurations värde i klustrets konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="19e6b-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightConfigValue `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
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
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="19e6b-109">Det här kommandot lägger till ett Hadoop-konfigurationsdata i det kluster som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="19e6b-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="19e6b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19e6b-110">PARAMETERS</span></span>

### <span data-ttu-id="19e6b-111">-Config</span><span class="sxs-lookup"><span data-stu-id="19e6b-111">-Config</span></span>
<span data-ttu-id="19e6b-112">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="19e6b-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="19e6b-113">Det här objektet skapas av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19e6b-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="19e6b-114">-Core</span><span class="sxs-lookup"><span data-stu-id="19e6b-114">-Core</span></span>
<span data-ttu-id="19e6b-115">Anger de grundläggande webbplatskonfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e6b-116">-DefaultProfile</span></span>
<span data-ttu-id="19e6b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="19e6b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19e6b-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="19e6b-118">-HBaseEnv</span></span>
<span data-ttu-id="19e6b-119">Anger HBase för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="19e6b-120">-HBaseSite</span></span>
<span data-ttu-id="19e6b-121">Anger HBase för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-122">-HDFS</span><span class="sxs-lookup"><span data-stu-id="19e6b-122">-Hdfs</span></span>
<span data-ttu-id="19e6b-123">Anger HDFS-konfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="19e6b-124">-HiveEnv</span></span>
<span data-ttu-id="19e6b-125">Anger registrerings data filens stack-konfigurationer för detta HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="19e6b-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="19e6b-126">-HiveSite</span></span>
<span data-ttu-id="19e6b-127">Anger registrerings data filen för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="19e6b-128">-MapRed</span></span>
<span data-ttu-id="19e6b-129">Anger MapRed för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="19e6b-130">-OozieEnv</span></span>
<span data-ttu-id="19e6b-131">Anger Oozie för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="19e6b-132">-OozieSite</span></span>
<span data-ttu-id="19e6b-133">Anger Oozie för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="19e6b-134">-RServer</span></span>
<span data-ttu-id="19e6b-135">Anger RServer-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="19e6b-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="19e6b-136">Giltigt endast för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="19e6b-136">Valid only for RServer clusters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="19e6b-137">-Spark2Defaults</span></span>
<span data-ttu-id="19e6b-138">Anger Spark2 standardinställningar för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="19e6b-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="19e6b-140">Anger Spark2-Thrift SparkConf-konfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="19e6b-141">-SparkDefaults</span></span>
<span data-ttu-id="19e6b-142">Anger standardkonfigurationer för Spark-standarden för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="19e6b-143">-SparkThriftConf</span></span>
<span data-ttu-id="19e6b-144">Anger de Thrift SparkConf-konfigurationerna för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="19e6b-145">-Storm</span></span>
<span data-ttu-id="19e6b-146">Anger Storm-webbplatskonfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="19e6b-147">-Tez</span></span>
<span data-ttu-id="19e6b-148">Anger Tez för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="19e6b-149">-WebHCat</span></span>
<span data-ttu-id="19e6b-150">Anger WebHCat för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-151">-Garn</span><span class="sxs-lookup"><span data-stu-id="19e6b-151">-Yarn</span></span>
<span data-ttu-id="19e6b-152">Anger den avskärmade konfigurationen för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="19e6b-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e6b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e6b-153">CommonParameters</span></span>
<span data-ttu-id="19e6b-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19e6b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e6b-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19e6b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e6b-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19e6b-156">INPUTS</span></span>

### <span data-ttu-id="19e6b-157">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="19e6b-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="19e6b-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19e6b-158">OUTPUTS</span></span>

### <span data-ttu-id="19e6b-159">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="19e6b-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="19e6b-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19e6b-160">NOTES</span></span>

## <span data-ttu-id="19e6b-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19e6b-161">RELATED LINKS</span></span>

[<span data-ttu-id="19e6b-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="19e6b-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


