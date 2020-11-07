---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 196608c24e31daad500fbf9b8aae1945550bb3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758269"
---
# Set-AzureRmSqlServerDisasterRecoveryConfiguration

## Sammanfattning
Ändrar en konfiguration för återställning av databas server.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmSqlServerDisasterRecoveryConfiguration** ändrar en återställnings konfiguration för SQL-serverdatabasen.

## BESKRIVS

## MALLPARAMETRAR

### -AllowDataLoss
Visar att Redundansåtgärden tillåter data förlust.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Failover
Anger att den här åtgärden är en redundansväxling.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en resurs grupp.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Anger namnet på en SQL-databasserver.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualEndpointName
Anger namnet på en virtuell slut punkt.

```yaml
Type: System.String
Parameter Sets: (All)
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmSqlServerDisasterRecoveryConfiguration](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[New-AzureRmSqlServerDisasterRecoveryConfiguration](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[Remove-AzureRmSqlServerDisasterRecoveryConfiguration](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[Dokumentation för SQL-databaser](https://docs.microsoft.com/azure/sql-database/)
