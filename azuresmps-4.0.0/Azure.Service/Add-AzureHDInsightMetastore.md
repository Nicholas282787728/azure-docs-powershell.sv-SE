---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093449"
---
# Add-AzureHDInsightMetastore

## Sammanfattning
Lägger till ett SQL Server-databasnamn i en HDInsight-kluster konfiguration.

## FRÅGESYNTAXEN

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Den här versionen av Azure PowerShell HDInsight är inaktuell.
Dessa cmdletar tas bort den 1 januari 2017.
Använd den nyare versionen av Azure PowerShell HDInsight.

Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Cmdleten **Add-AzureHDInsightMetastore** lägger till en Microsoft SQL Server-databas till en Azure HDInsight-konfiguration som skapas av den **nya-AzureHDInsightClusterConfig-** cmdleten.
Databasen används för att lagra metadata för registrerings data eller Oozie, eller både och.

## BESKRIVS

### Exempel 1: lägga till en metastore
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

Det här kommandot lägger till en SQL Server-databas med namnet ContosoSQLServer som fungerar som en struktur metastore för ett HDInsight-kluster.

### Exempel 2: Konfigurera lagring och Lägg till metastores
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer"
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

I det första kommandot används cmdleten **Get-AzureSubscription** för att hämta aktuellt ABONNEMANGS-ID och det sparas sedan i $SubId variabel.

I det andra och tredje kommandot används cmdleten **Get-AzureStorageKey** för att hämta primär lagrings nycklar för MyBlobStorage och MySecondBlobStorage, och sedan sparas nycklarna i $Key 1-och $Key 2-variabler.

De fjärde, femte och sjätte kommandona använder cmdleten **Get-Credential** för att få autentiseringsuppgifter för det aktuella abonnemanget och för Oozie och Hive och sedan lagra autentiseringsuppgifterna i variabler.

Det slutliga kommandot utför en sekvens med operationer genom att använda dessa cmdletar:

- **New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration.
- **Set-AzureHDInsightDefaultStorage** för att ange standard lagrings kontot för konfigurationen till MyBlobStorage.blob.Core.Windows.net.
- **Add-AzureHDInsightStorage** om du vill lägga till ett andra lagrings konto med namnet MySecondBlobStorage.blob.Core.Windows.net i konfigurationen.
- **Add-AzureHDInsightMetastore** om du vill lägga till en metastore för Oozie och en metastore för struktur till konfigurationen.
- **New-AzureHDInsightCluster** för att skapa ett HDInsight-kluster med den nya konfigurationen.

## MALLPARAMETRAR

### -Config
Anger ett konfigurations objekt.
Denna cmdlet lägger till metastore information i det konfigurations objekt som den här parametern anger.

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

### -Autentiseringsuppgift
Anger de autentiseringsuppgifter som används för att komma åt en SQL Server-databas.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Anger namnet på databasen där registrerings data ska lagras eller Oozie.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetastoreType
Anger typen av metastore.
De acceptabla värdena för den här parametern är: HiveMetaStore eller OozieMetaStore.

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
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

### -SqlAzureServerName
Anger det fullständigt kvalificerade domän namnet (FQDN) för SQL Server som innehåller databasen där metadata lagras.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[Add-AzureHDInsightStorage](./Add-AzureHDInsightStorage.md)

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)
