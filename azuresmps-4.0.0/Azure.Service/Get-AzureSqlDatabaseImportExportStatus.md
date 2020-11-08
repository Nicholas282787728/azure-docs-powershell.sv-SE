---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099524"
---
# Get-AzureSqlDatabaseImportExportStatus

## Sammanfattning
Hämtar statusen för en import-eller export förfrågan.

## FRÅGESYNTAXEN

### ByConnectionInfo
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRequestObject
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureSqlDatabaseImportExportStatus** får statusen för en import-eller export förfrågan.
Start-AzureSqlDatabaseImport eller Start-AzureSqlDatabaseExport cmdlet initierar begär Anden.
Du kan ange ett Request-objekt med hjälp av parametern *Request* , eller så kan du identifiera begäran genom att använda parametern *RequestId* och parametrarna *username* , *Password* och *servername* .

## BESKRIVS

### Exempel 1: få statusen för en export förfrågan
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

Det första kommandot skapar en export förfrågan och lagrar den sedan i $ExportRequest variabel.

Det andra kommandot får statusen för den exportfiler som är lagrad i $ExportRequest.

## MALLPARAMETRAR

### -Lösen ord
Anger det lösen ord som krävs för att ansluta till Azure SQL Database-servern.
Du måste ange den här parametern om du har angett parametern *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

### -Begäran
Anger ett **ImportExportRequest** -objekt.
Om du vill hämta ett objekt för import eller export, Använd cmdleten Start-AzureSqlDatabaseImport eller Start-AzureSqlDatabaseExport.

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Begärande-RequestId
Anger GUID för den import-eller export åtgärd som denna cmdlet får status för.
Om du anger den här parametern måste du ange *användar namn* , *lösen ord* och *servername* -parametrar.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Anger namnet på Azure SQL Database-servern.
Du måste ange den här parametern om du har angett parametern *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Username
Anger det användar namn som krävs för att ansluta till Azure SQL Database-servern.
Du måste ange den här parametern om du har angett parametern *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. ImportExport. StatusInfo

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Azure SQL-databas](https://azure.microsoft.com/en-us/services/sql-database/)

[Hämta status för importera export databas](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start-AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)

[Start-AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


