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
# Add-AzureHDInsightConfigValues

## Sammanfattning
Lägger till en anpassning av Hadoop-konfigurationsinställningar eller en struktur för anpassning av ett delat bibliotek i HDInsight-klustret.

## FRÅGESYNTAXEN

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Den här versionen av Azure PowerShell HDInsight är inaktuell.
Dessa cmdletar tas bort den 1 januari 2017.
Använd den nyare versionen av Azure PowerShell HDInsight.

Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).
Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).
Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight-cmdletar](https://msdn.microsoft.com/en-us/library/mt438705.aspx).

Cmdleten **Add-AzureHDInsightConfigValues** lägger till en konfiguration för Hadoop-konfigurationsinställningar, till exempel Core-site.xml eller Hive-site.xml, eller en anpassning av ett delat bibliotek för en Azure HDInsight-kluster.

Med cmdlet läggs anpassade konfigurations värden till i ett angivet konfigurations objekt.
Anpassade inställningar läggs till i konfigurationsfilerna för de relevanta Hadoop-tjänsterna när klustret distribueras.

## BESKRIVS

### Exempel 1: Konfigurera ett kluster
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

Det första kommandot skapar ett nytt **AzureHDInsightHiveConfiguration** -objekt och lagrar det sedan i $HiveConfigValues variabel.

Nästa fem kommandon skapar konfigurations värden för struktur och lagrar dessa värden som medlemmar i $HiveConfigValues.

Det sjunde kommandot skapar ett **AzureHDInsightOozieConfiguration** -objekt och lagrar det sedan i $OozieConfigValues variabel.
Med kommandot åtto skapas ett konfigurations värde för Oozie och sedan lagras värdena som en medlem i $OozieConfigValues.

Det nionde kommandot skapar ett **AzureHDInsightMapReduceConfiguration** -objekt och lagrar det sedan i $MapredConfigValues variabel.
Nästa två kommandon skapar konfigurations värden för MapReduce och lagrar dessa värden som medlemmar i $MapredConfigValues.

Det tolfte kommandot använder cmdleten **New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration och lagrar den sedan i $config variabel.
Kommandot använder pipeline-operatorn för att överföra $Config till cmdleten **set-AzureHDInsightDefaultStorage** för att uppdatera standardinställningarna för lagring och till cmdleten **Add-AzureHDInsightConfigValues** för att lägga till nya konfigurations värden i kluster konfigurationen.

I det sista kommandot används pipeline-operatorn för att överföra $Config till cmdleten **New-AzureHDInsightCluster** för att skapa ett nytt HDInsight-kluster med de anpassade inställningarna.

## MALLPARAMETRAR

### -Config
Anger det konfigurations objekt som du vill lägga till en Hadoop-konfiguration för.

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

### -Core
Anger en uppsättning Hadoop-konfigurationsdata för Core-site.xml.

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

### -HBase
Anger en uppsättning HBase-konfigurations värden för Hbase-site.xml.

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

### -HDFS
Anger en uppsättning Hadoop-konfigurationsdata för Hdfs-site.xml.

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

### -Struktur
Anger ett anpassat objekt för Hadoop-datatjänst, inklusive en uppsättning Hadoop-konfigurationsinställningar för Hive-site.xml-och registreringsdatafiler-delade bibliotek.

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

### -MapReduce
Anger ett anpassat objekt för MapReduce och kapacitets Schemaläggaren.

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

### -Oozie
Anger ett Customization-objekt för Hadoop Oozie-tjänsten, inklusive en uppsättning Hadoop-konfigurationsinställningar för Oozie-site.xml.

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

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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

### -Spark
Anger ett Customization-objekt för Apache Spark.

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

### -Storm
Anger ett Customization-objekt för Apache storm.

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

### -Garn
Anger ett Customization-objekt för Hadoop-garn, med en uppsättning anpassade konfigurations värden för garn för Yarn-site.xml.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)
