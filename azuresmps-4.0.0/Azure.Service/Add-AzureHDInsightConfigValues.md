---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093454"
---
# <span data-ttu-id="9b78d-101">Add-AzureHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="9b78d-101">Add-AzureHDInsightConfigValues</span></span>

## <span data-ttu-id="9b78d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b78d-102">SYNOPSIS</span></span>
<span data-ttu-id="9b78d-103">Lägger till en anpassning av Hadoop-konfigurationsinställningar eller en struktur för anpassning av ett delat bibliotek i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9b78d-103">Adds a Hadoop configuration value customization or a Hive shared library customization to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="9b78d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b78d-104">SYNTAX</span></span>

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9b78d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b78d-105">DESCRIPTION</span></span>
<span data-ttu-id="9b78d-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="9b78d-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="9b78d-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="9b78d-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="9b78d-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9b78d-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="9b78d-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="9b78d-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="9b78d-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="9b78d-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="9b78d-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight-cmdletar](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="9b78d-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="9b78d-112">Cmdleten **Add-AzureHDInsightConfigValues** lägger till en konfiguration för Hadoop-konfigurationsinställningar, till exempel Core-site.xml eller Hive-site.xml, eller en anpassning av ett delat bibliotek för en Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="9b78d-112">The **Add-AzureHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as Core-site.xml or Hive-site.xml, or a Hive shared library customization to an Azure HDInsight cluster configuration.</span></span>

<span data-ttu-id="9b78d-113">Med cmdlet läggs anpassade konfigurations värden till i ett angivet konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="9b78d-113">The cmdlet adds custom configuration values to a specified configuration object.</span></span>
<span data-ttu-id="9b78d-114">Anpassade inställningar läggs till i konfigurationsfilerna för de relevanta Hadoop-tjänsterna när klustret distribueras.</span><span class="sxs-lookup"><span data-stu-id="9b78d-114">The custom settings are added to the configuration files of the relevant Hadoop services when the cluster is deployed.</span></span>

## <span data-ttu-id="9b78d-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b78d-115">EXAMPLES</span></span>

### <span data-ttu-id="9b78d-116">Exempel 1: Konfigurera ett kluster</span><span class="sxs-lookup"><span data-stu-id="9b78d-116">Example 1: Configure a cluster</span></span>
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

<span data-ttu-id="9b78d-117">Det första kommandot skapar ett nytt **AzureHDInsightHiveConfiguration** -objekt och lagrar det sedan i $HiveConfigValues variabel.</span><span class="sxs-lookup"><span data-stu-id="9b78d-117">The first command creates a new **AzureHDInsightHiveConfiguration** object, and then stores it in the $HiveConfigValues variable.</span></span>

<span data-ttu-id="9b78d-118">Nästa fem kommandon skapar konfigurations värden för struktur och lagrar dessa värden som medlemmar i $HiveConfigValues.</span><span class="sxs-lookup"><span data-stu-id="9b78d-118">The next five commands create configuration values for Hive and store those values as members of $HiveConfigValues.</span></span>

<span data-ttu-id="9b78d-119">Det sjunde kommandot skapar ett **AzureHDInsightOozieConfiguration** -objekt och lagrar det sedan i $OozieConfigValues variabel.</span><span class="sxs-lookup"><span data-stu-id="9b78d-119">The seventh command creates an **AzureHDInsightOozieConfiguration** object, and then stores it in the $OozieConfigValues variable.</span></span>
<span data-ttu-id="9b78d-120">Med kommandot åtto skapas ett konfigurations värde för Oozie och sedan lagras värdena som en medlem i $OozieConfigValues.</span><span class="sxs-lookup"><span data-stu-id="9b78d-120">The eighth command creates a configuration value for Oozie, and then stores that values as a member of $OozieConfigValues.</span></span>

<span data-ttu-id="9b78d-121">Det nionde kommandot skapar ett **AzureHDInsightMapReduceConfiguration** -objekt och lagrar det sedan i $MapredConfigValues variabel.</span><span class="sxs-lookup"><span data-stu-id="9b78d-121">The ninth command creates an **AzureHDInsightMapReduceConfiguration** object, and then stores it in the $MapredConfigValues variable.</span></span>
<span data-ttu-id="9b78d-122">Nästa två kommandon skapar konfigurations värden för MapReduce och lagrar dessa värden som medlemmar i $MapredConfigValues.</span><span class="sxs-lookup"><span data-stu-id="9b78d-122">The next two commands create configuration values for MapReduce and store those values as members of $MapredConfigValues.</span></span>

<span data-ttu-id="9b78d-123">Det tolfte kommandot använder cmdleten **New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration och lagrar den sedan i $config variabel.</span><span class="sxs-lookup"><span data-stu-id="9b78d-123">The twelfth command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>
<span data-ttu-id="9b78d-124">Kommandot använder pipeline-operatorn för att överföra $Config till cmdleten **set-AzureHDInsightDefaultStorage** för att uppdatera standardinställningarna för lagring och till cmdleten **Add-AzureHDInsightConfigValues** för att lägga till nya konfigurations värden i kluster konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="9b78d-124">The command uses the pipeline operator to pass $Config to the **Set-AzureHDInsightDefaultStorage** cmdlet to update the default storage setting and to the **Add-AzureHDInsightConfigValues** cmdlet to add the new configuration values to the cluster configuration.</span></span>

<span data-ttu-id="9b78d-125">I det sista kommandot används pipeline-operatorn för att överföra $Config till cmdleten **New-AzureHDInsightCluster** för att skapa ett nytt HDInsight-kluster med de anpassade inställningarna.</span><span class="sxs-lookup"><span data-stu-id="9b78d-125">The final command uses the pipeline operator to pass $Config to the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster with the customized settings.</span></span>

## <span data-ttu-id="9b78d-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b78d-126">PARAMETERS</span></span>

### <span data-ttu-id="9b78d-127">-Config</span><span class="sxs-lookup"><span data-stu-id="9b78d-127">-Config</span></span>
<span data-ttu-id="9b78d-128">Anger det konfigurations objekt som du vill lägga till en Hadoop-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="9b78d-128">Specifies the configuration object to which to add a Hadoop configuration.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b78d-129">-Core</span><span class="sxs-lookup"><span data-stu-id="9b78d-129">-Core</span></span>
<span data-ttu-id="9b78d-130">Anger en uppsättning Hadoop-konfigurationsdata för Core-site.xml.</span><span class="sxs-lookup"><span data-stu-id="9b78d-130">Specifies a set of Hadoop configuration values for Core-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b78d-131">-HBase</span><span class="sxs-lookup"><span data-stu-id="9b78d-131">-HBase</span></span>
<span data-ttu-id="9b78d-132">Anger en uppsättning HBase-konfigurations värden för Hbase-site.xml.</span><span class="sxs-lookup"><span data-stu-id="9b78d-132">Specifies a set of HBase configuration values for Hbase-site.xml.</span></span>

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b78d-133">-HDFS</span><span class="sxs-lookup"><span data-stu-id="9b78d-133">-Hdfs</span></span>
<span data-ttu-id="9b78d-134">Anger en uppsättning Hadoop-konfigurationsdata för Hdfs-site.xml.</span><span class="sxs-lookup"><span data-stu-id="9b78d-134">Specifies a set of Hadoop configuration values for Hdfs-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b78d-135">-Struktur</span><span class="sxs-lookup"><span data-stu-id="9b78d-135">-Hive</span></span>
<span data-ttu-id="9b78d-136">Anger ett anpassat objekt för Hadoop-datatjänst, inklusive en uppsättning Hadoop-konfigurationsinställningar för Hive-site.xml-och registreringsdatafiler-delade bibliotek.</span><span class="sxs-lookup"><span data-stu-id="9b78d-136">Specifies a customization object for Hadoop Hive service, including a set of Hadoop configuration values for Hive-site.xml and Hive shared libraries.</span></span>

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b78d-137">-MapReduce</span><span class="sxs-lookup"><span data-stu-id="9b78d-137">-MapReduce</span></span>
<span data-ttu-id="9b78d-138">Anger ett anpassat objekt för MapReduce och kapacitets Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="9b78d-138">Specifies a customization object for MapReduce and the capacity scheduler.</span></span>

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b78d-139">-Oozie</span><span class="sxs-lookup"><span data-stu-id="9b78d-139">-Oozie</span></span>
<span data-ttu-id="9b78d-140">Anger ett Customization-objekt för Hadoop Oozie-tjänsten, inklusive en uppsättning Hadoop-konfigurationsinställningar för Oozie-site.xml.</span><span class="sxs-lookup"><span data-stu-id="9b78d-140">Specifies a customization object for Hadoop Oozie service, including a set of Hadoop configuration values for Oozie-site.xml.</span></span>

```yaml
Type: AzureHDInsightOozieConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b78d-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="9b78d-141">-Profile</span></span>
<span data-ttu-id="9b78d-142">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9b78d-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b78d-143">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9b78d-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b78d-144">-Spark</span><span class="sxs-lookup"><span data-stu-id="9b78d-144">-Spark</span></span>
<span data-ttu-id="9b78d-145">Anger ett Customization-objekt för Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="9b78d-145">Specifies a customization object for Apache Spark.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b78d-146">-Storm</span><span class="sxs-lookup"><span data-stu-id="9b78d-146">-Storm</span></span>
<span data-ttu-id="9b78d-147">Anger ett Customization-objekt för Apache storm.</span><span class="sxs-lookup"><span data-stu-id="9b78d-147">Specifies a customization object for Apache Storm.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b78d-148">-Garn</span><span class="sxs-lookup"><span data-stu-id="9b78d-148">-Yarn</span></span>
<span data-ttu-id="9b78d-149">Anger ett Customization-objekt för Hadoop-garn, med en uppsättning anpassade konfigurations värden för garn för Yarn-site.xml.</span><span class="sxs-lookup"><span data-stu-id="9b78d-149">Specifies a customization object for Hadoop YARN, specifying a set of customized YARN configuration values for Yarn-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b78d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b78d-150">CommonParameters</span></span>
<span data-ttu-id="9b78d-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b78d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b78d-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b78d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b78d-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b78d-153">INPUTS</span></span>

## <span data-ttu-id="9b78d-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b78d-154">OUTPUTS</span></span>

## <span data-ttu-id="9b78d-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b78d-155">NOTES</span></span>

## <span data-ttu-id="9b78d-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b78d-156">RELATED LINKS</span></span>

[<span data-ttu-id="9b78d-157">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9b78d-157">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="9b78d-158">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="9b78d-158">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="9b78d-159">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="9b78d-159">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
