---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099523"
---
# Get-AzureSqlDatabaseOperation

## Sammanfattning
Hämtar statusen för databas åtgärder på en Azure-Server.

## FRÅGESYNTAXEN

### ByConnectionContext (standard)
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureSqlDatabaseOperation** får statusen för databas åtgärder på den angivna Azure-servern.
Om du bara anger parametern *Server namn* eller *ConnectionContext* , får cmdleten alla databas operationer för servern.
Om du också anger en databas med parametern *databas* eller *databasename* får denna cmdlet alla åtgärder för den angivna databasen.
Om du anger ett åtgärds-GUID och *Server namn* eller *ConnectionContext* , får cmdleten en enda databas operation.

## BESKRIVS

### Exempel 1: få status för alla databas åtgärder för en databas
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

Det här kommandot får statusen för alla databas åtgärder på databasen som heter Database17 på den server som kontexten för anslutning $Context anger.

### Exempel 2: få status för alla databas åtgärder för en server
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

Det här kommandot får statusen för alla databas åtgärder på den server som kontexten $Context anger.

## MALLPARAMETRAR

### -ConnectionContext
Anger en servers anslutning.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Databas
Anger ett objekt som representerar en Azure SQL-databas.
Om du anger den här parametern måste du ange parametern *Server namn* eller parametern *ConnectionContext* .

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Anger namnet på en databas.
Om du anger den här parametern måste du ange parametern *Server namn* eller parametern *ConnectionContext* .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OperationGuid
Anger det åtgärds-ID som representerar en specifik databas åtgärd för vilken denna cmdlet får status.
Du kan skaffa åtgärds-ID genom att begära alla databas åtgärder för en Azure SQL-databas eller-server.
Om du anger den här parametern måste du ange parametern *Server namn* eller parametern *ConnectionContext* .

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -ServerName
Anger namnet på en server.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerContext

### System. GUID

## VÄRDEN

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database. DatabaseOperationResponseList []
Denna cmdlet returnerar en matris med **DatabaseOperationResponseList** -objekt om du får flera operationer.

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database. DatabaseOperationResponse

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Azure SQL-databas](https://msdn.microsoft.com/library/ee336279.aspx)

[Databas åtgärds status](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


