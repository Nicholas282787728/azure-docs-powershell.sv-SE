---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
ms.openlocfilehash: 0e287922c692a8271a82a62f20539bb97518b9f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757291"
---
# <span data-ttu-id="9770a-101">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="9770a-101">Add-AzureRmHDInsightConfigValues</span></span>

## <span data-ttu-id="9770a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9770a-102">SYNOPSIS</span></span>
<span data-ttu-id="9770a-103">Lägger till ett konfigurations värde för Hadoop-konfigurering och/eller en struktur för ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="9770a-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9770a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9770a-104">SYNTAX</span></span>

### <span data-ttu-id="9770a-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="9770a-105">Spark1</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9770a-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="9770a-106">Spark2</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9770a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9770a-107">DESCRIPTION</span></span>
<span data-ttu-id="9770a-108">Cmdleten **Add-AzureRmHDInsightConfigValues** lägger till en konfiguration för Hadoop-konfigurationsinställningar, till exempel core-site.xml eller hive-site.xml, och/eller en struktur för att skapa ett delat bibliotek för HDInsight-konfigurationsobjekt som skapas av New-AzureRmHDInsightClusterConfig cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9770a-108">The **Add-AzureRmHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="9770a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9770a-109">EXAMPLES</span></span>

### <span data-ttu-id="9770a-110">Exempel 1: lägga till ett anpassat konfigurations värde i klustrets konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="9770a-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightConfigValues `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="9770a-111">Det här kommandot lägger till ett Hadoop-konfigurationsdata i det kluster som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="9770a-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="9770a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9770a-112">PARAMETERS</span></span>

### <span data-ttu-id="9770a-113">-Config</span><span class="sxs-lookup"><span data-stu-id="9770a-113">-Config</span></span>
<span data-ttu-id="9770a-114">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="9770a-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="9770a-115">Det här objektet skapas av New-AzureRmHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9770a-115">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="9770a-116">-Core</span><span class="sxs-lookup"><span data-stu-id="9770a-116">-Core</span></span>
<span data-ttu-id="9770a-117">Anger de grundläggande webbplatskonfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="9770a-118">-HBaseEnv</span></span>
<span data-ttu-id="9770a-119">Anger HBase för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="9770a-120">-HBaseSite</span></span>
<span data-ttu-id="9770a-121">Anger HBase för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-122">-HDFS</span><span class="sxs-lookup"><span data-stu-id="9770a-122">-Hdfs</span></span>
<span data-ttu-id="9770a-123">Anger HDFS-konfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="9770a-124">-HiveEnv</span></span>
<span data-ttu-id="9770a-125">Anger registrerings data filens stack-konfigurationer för detta HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="9770a-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="9770a-126">-HiveSite</span></span>
<span data-ttu-id="9770a-127">Anger registrerings data filen för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="9770a-128">-MapRed</span></span>
<span data-ttu-id="9770a-129">Anger MapRed för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="9770a-130">-OozieEnv</span></span>
<span data-ttu-id="9770a-131">Anger Oozie för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="9770a-132">-OozieSite</span></span>
<span data-ttu-id="9770a-133">Anger Oozie för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="9770a-134">-RServer</span></span>
<span data-ttu-id="9770a-135">Anger RServer-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="9770a-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="9770a-136">Giltigt endast för RServer-kluster.</span><span class="sxs-lookup"><span data-stu-id="9770a-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="9770a-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="9770a-137">-Spark2Defaults</span></span>
<span data-ttu-id="9770a-138">Anger Spark2 standardinställningar för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="9770a-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="9770a-140">Anger Spark2-Thrift SparkConf-konfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="9770a-141">-SparkDefaults</span></span>
<span data-ttu-id="9770a-142">Anger standardkonfigurationer för Spark-standarden för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="9770a-143">-SparkThriftConf</span></span>
<span data-ttu-id="9770a-144">Anger de Thrift SparkConf-konfigurationerna för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="9770a-145">-Storm</span></span>
<span data-ttu-id="9770a-146">Anger Storm-webbplatskonfigurationer för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="9770a-147">-Tez</span></span>
<span data-ttu-id="9770a-148">Anger Tez för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="9770a-149">-WebHCat</span></span>
<span data-ttu-id="9770a-150">Anger WebHCat för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-151">-Garn</span><span class="sxs-lookup"><span data-stu-id="9770a-151">-Yarn</span></span>
<span data-ttu-id="9770a-152">Anger den avskärmade konfigurationen för det här HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9770a-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9770a-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9770a-153">-DefaultProfile</span></span>
<span data-ttu-id="9770a-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9770a-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9770a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9770a-155">CommonParameters</span></span>
<span data-ttu-id="9770a-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9770a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9770a-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9770a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9770a-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9770a-158">INPUTS</span></span>

### <span data-ttu-id="9770a-159">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="9770a-159">AzureHDInsightConfig</span></span>
<span data-ttu-id="9770a-160">Parametern ' config ' godkänner värdet av typen ' AzureHDInsightConfig ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9770a-160">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="9770a-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9770a-161">OUTPUTS</span></span>

### <span data-ttu-id="9770a-162">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="9770a-162">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="9770a-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9770a-163">NOTES</span></span>

## <span data-ttu-id="9770a-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9770a-164">RELATED LINKS</span></span>

[<span data-ttu-id="9770a-165">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="9770a-165">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


