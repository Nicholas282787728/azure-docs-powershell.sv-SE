---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 6482c6e6804b9d59ddbd752d20f39d3316b75f8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102864"
---
# <span data-ttu-id="a4a06-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="a4a06-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="a4a06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4a06-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a06-103">Lägger till ett konfigurations värde för Hadoop-konfigurering och/eller en struktur för ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="a4a06-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="a4a06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4a06-104">SYNTAX</span></span>

### <span data-ttu-id="a4a06-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="a4a06-105">Spark1</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4a06-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="a4a06-106">Spark2</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4a06-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4a06-107">DESCRIPTION</span></span>
<span data-ttu-id="a4a06-108">Cmdleten **Add-AzHDInsightConfigValue** lägger till en konfiguration för Hadoop-konfigurationsinställningar, till exempel core-site.xml eller hive-site.xml, och/eller en struktur för att skapa ett delat bibliotek för HDInsight-konfigurationsobjekt som skapas av New-AzHDInsightClusterConfig cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4a06-108">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="a4a06-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4a06-109">EXAMPLES</span></span>

### <span data-ttu-id="a4a06-110">Exempel 1: lägga till ett anpassat konfigurations värde i klustrets konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="a4a06-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="a4a06-111">Det här kommandot lägger till ett Hadoop-konfigurationsdata i det kluster som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a4a06-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a4a06-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4a06-112">PARAMETERS</span></span>

### <span data-ttu-id="a4a06-113">-Config</span><span class="sxs-lookup"><span data-stu-id="a4a06-113">-Config</span></span>
<span data-ttu-id="a4a06-114">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a4a06-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="a4a06-115">Det här objektet skapas av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4a06-115">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="a4a06-116">-Core</span><span class="sxs-lookup"><span data-stu-id="a4a06-116">-Core</span></span>
<span data-ttu-id="a4a06-117">Anger de grundläggande webbplatskonfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a06-118">-DefaultProfile</span></span>
<span data-ttu-id="a4a06-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a4a06-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4a06-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="a4a06-120">-HBaseEnv</span></span>
<span data-ttu-id="a4a06-121">Anger HBase för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="a4a06-122">-HBaseSite</span></span>
<span data-ttu-id="a4a06-123">Anger HBase för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-124">-HDFS</span><span class="sxs-lookup"><span data-stu-id="a4a06-124">-Hdfs</span></span>
<span data-ttu-id="a4a06-125">Anger HDFS-konfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="a4a06-126">-HiveEnv</span></span>
<span data-ttu-id="a4a06-127">Anger registrerings data filens stack-konfigurationer för detta HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="a4a06-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="a4a06-128">-HiveSite</span></span>
<span data-ttu-id="a4a06-129">Anger registrerings data filen för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="a4a06-130">-MapRed</span></span>
<span data-ttu-id="a4a06-131">Anger MapRed för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="a4a06-132">-OozieEnv</span></span>
<span data-ttu-id="a4a06-133">Anger Oozie för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="a4a06-134">-OozieSite</span></span>
<span data-ttu-id="a4a06-135">Anger Oozie för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="a4a06-136">-RServer</span></span>
<span data-ttu-id="a4a06-137">Anger RServer-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="a4a06-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="a4a06-138">Giltigt endast för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="a4a06-138">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="a4a06-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="a4a06-139">-Spark2Defaults</span></span>
<span data-ttu-id="a4a06-140">Anger Spark2 standardinställningar för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4a06-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="a4a06-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="a4a06-142">Anger Spark2-Thrift SparkConf-konfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4a06-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="a4a06-143">-SparkDefaults</span></span>
<span data-ttu-id="a4a06-144">Anger standardkonfigurationer för Spark-standarden för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4a06-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="a4a06-145">-SparkThriftConf</span></span>
<span data-ttu-id="a4a06-146">Anger de Thrift SparkConf-konfigurationerna för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4a06-147">-Storm</span><span class="sxs-lookup"><span data-stu-id="a4a06-147">-Storm</span></span>
<span data-ttu-id="a4a06-148">Anger Storm-webbplatskonfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="a4a06-149">-Tez</span></span>
<span data-ttu-id="a4a06-150">Anger Tez för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="a4a06-151">-WebHCat</span></span>
<span data-ttu-id="a4a06-152">Anger WebHCat för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-153">-Garn</span><span class="sxs-lookup"><span data-stu-id="a4a06-153">-Yarn</span></span>
<span data-ttu-id="a4a06-154">Anger den avskärmade konfigurationen för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4a06-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="a4a06-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a06-155">CommonParameters</span></span>
<span data-ttu-id="a4a06-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a06-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a06-157">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4a06-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a06-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4a06-158">INPUTS</span></span>

### <span data-ttu-id="a4a06-159">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a4a06-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a4a06-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4a06-160">OUTPUTS</span></span>

### <span data-ttu-id="a4a06-161">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a4a06-161">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a4a06-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4a06-162">NOTES</span></span>

## <span data-ttu-id="a4a06-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4a06-163">RELATED LINKS</span></span>

[<span data-ttu-id="a4a06-164">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a4a06-164">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

