---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093294"
---
# Get-AzureSqlDatabaseServiceObjective

## Sammanfattning
Hämtar tjänste mål för en Azure SQL Database-Server.

## FRÅGESYNTAXEN

### ByConnectionContext (standard)
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureSqlDatabaseServiceObjective** hämtar tjänst mål för en Azure SQL Database-Server.
Tjänste mål kallas prestanda nivåer.
Om du inte anger något tjänst mål returnerar denna cmdlet alla giltiga tjänst mål för den angivna servern.

Denna cmdlet gäller för grundläggande, standard-och premie tjänst nivåer.

## BESKRIVS

### Exempel 1: få alla tjänst mål genom att använda en kontext för anslutning
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

Det här kommandot får alla tjänst mål för servern som kontexten för anslutning $Context anger.

### Exempel 2: få alla tjänst mål genom att använda ett server namn
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

Det här kommandot får alla tjänst mål för servern som heter Server01.

## MALLPARAMETRAR

### -Kontext
Anger en servers anslutning.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

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

### -ServiceObjective
Anger ett objekt som representerar det tjänst mål som denna cmdlet får.
Giltiga värden är: 

- Grundläggande: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c
- Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b
- Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928
- Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7
- * Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446

* Standard (S3) är en del av den senaste SQL-V12 (för hands version).
Mer information finns i [Nyheter i för hands versionen av V12 för Azure SQL Database](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) i Azure-biblioteket.

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceObjectiveName
Anger namnet på ett tjänst mål som ska visas.
Giltiga värden är: Basic, S0, S1, S2, S3, P1, P2 och P3.

```yaml
Type: String
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

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. ServiceObjective

## VÄRDEN

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\>

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Azure SQL-databas](https://msdn.microsoft.com/library/ee336279.aspx)

[Skaffa service nivå mål](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


