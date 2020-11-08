---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099199"
---
# New-AzureSqlDatabaseServerFirewallRule

## Sammanfattning
Skapar en brand Väggs regel i Azure SQL Database Server.

## FRÅGESYNTAXEN

### IpRange (standard)
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AllowAllAzureServices
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureSqlDatabaseServerFirewallRule** skapar en brand Väggs regel i den angivna instansen av Azure SQL Database Server i den aktuella prenumerationen.

Använd parametrarna *StartIpAddress* och *EndIpAddress* för att ange ett intervall med IP-adresser som den här regeln tillåter att ansluta till Azure SQL Database-servern.

Ange parametern *AllowAllAzureServices* om du vill skapa en regel som tillåter Azure-anslutningar till servern.
Regeln har start-och slut värden för IP-adresserna 0.0.0.0.
Om du inte anger något namn för en brand Väggs regel tilldelar denna cmdlet standard namnet AllowAllAzureServices.

## BESKRIVS

### Exempel 1: skapa en brand Väggs regel
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

Det här kommandot skapar en brand Väggs regel FirewallRule24 på en Azure SQL-databasserver med namnet lpqd0zbr8y.
Kommandot anger ett IP-adressintervall.

### Exempel 2: skapa en regel som tillåter alla Azure-tjänster
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

Det här kommandot skapar en brand Väggs regel med namnet AzureConnections på servern med namnet lpqd0zbr8y som tillåter Azure-anslutningar.

### Exempel 3: skapa en regel som gör att alla Azure-tjänster som använder standard namnet skapar en regel som tillåter alla Azure-tjänster som använder standard namnet
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

Det här kommandot skapar en brand Väggs regel på den angivna servern med namnet lpqd0zbr8y som tillåter Azure-anslutningar.
Kommandot tilldelar standard regel namnet AllowAllAzureServices.

## MALLPARAMETRAR

### -AllowAllAzureServices
Visar att den här brand Väggs regeln gör att alla Azure IP-adresser kan komma åt servern.

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndIpAddress
Anger slutvärdet för IP-adressintervallet för den här regeln.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.

```yaml
Type: SwitchParameter
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

### -RuleName
Anger namnet på den nya brand Väggs regeln.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Anger namnet på en server.
Denna cmdlet skapar en brand Väggs regel på den server som denna cmdlet anger.
Ange Server namnet, inte det fullständigt kvalificerade DNS-namnet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartIpAddress
Anger startvärdet för IP-adressintervallet för brand Väggs regeln.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Azure SQL-databas](https://azure.microsoft.com/en-us/services/sql-database/)

[Skapa brand Väggs regel](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseServerFirewallRule](./Get-AzureSqlDatabaseServerFirewallRule.md)

[Remove-AzureSqlDatabaseServerFirewallRule](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[Set-AzureSqlDatabaseServerFirewallRule](./Set-AzureSqlDatabaseServerFirewallRule.md)


