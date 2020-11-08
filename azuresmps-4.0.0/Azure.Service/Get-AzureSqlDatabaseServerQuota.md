---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093296"
---
# Get-AzureSqlDatabaseServerQuota

## Sammanfattning
Hämtar kvot information för en Azure SQL Database-Server.

## FRÅGESYNTAXEN

### ByConnectionContext
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureSqlDatabaseServerQuota** hämtar kvot informationen för en viss instans av Azure SQL Database Server.
Ange en anslutnings kontext eller Server namnet.
Om du inte anger ett kvot namn får denna cmdlet all kvot information för servern.

## BESKRIVS

### Exempel 1: Hämta information för en specifik kvot
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

Med det här kommandot får du den kvot som heter Premium_Databases från den Azure SQL-databasserver som anges av anslutningen som lagras i $Context variabel.

### Exempel 2: Hämta information för alla kvoter
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

Det här kommandot får alla kvot värden från den server som anges av anslutnings $Context.

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

### -QuotaName
Anger namnet på det kvot värde som denna cmdlet får.

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

## VÄRDEN

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. ServerQuota []

## ANMÄRKNINGAR
* Verifiera: denna cmdlet kan använda SQL Server-serverautentisering eller certifikatbaserad identifiering. Exempel på hur du konfigurerar en konfiguration finns i New-AzureSqlDatabaseServerContext cmdlet.

## RELATERADE LÄNKAR

[Azure SQL-databas](https://azure.microsoft.com/en-us/services/sql-database/)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


