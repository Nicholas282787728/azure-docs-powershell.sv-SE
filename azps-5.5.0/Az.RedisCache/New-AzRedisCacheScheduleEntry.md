---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252041"
---
# New-AzRedisCacheScheduleEntry

## SYNOPSIS
Skapar en schemapost.

## SYNTAX

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzRedisCacheScheduleEntry** skapar ett **PSScheduleEntry-objekt.**
Azure Redis Cache-cmdlets för korrigeringsschema, till exempel New-AzRedisCachePatchSchedule cmdlet, kräver schemaläggningsinmatningsobjekt.

## EXEMPEL

### Exempel 1: Skapa en schemapost för helger
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

Det här kommandot skapar **ett PSScheduleEntry-objekt** som representerar ett helgschema som har den angivna starttiden och startfönstret.

## PARAMETERS

### -DayOfWeek
Anger veckodagen för schemaposten.
De godtagbara värdena för den här parametern är:
- Varje dag 
- Helg 
- Måndag 
- Tisdag 
- Onsdag 
- Torsdag 
- Fredag 
- Lördag 
- söndag

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindow
Anger hur lång tid som tillåts för uppdateringar.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartHourUtc
Anger en timme på dagen då schemat startar.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

### System.Int32

### System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## UTDATA

### Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry

## ANTECKNINGAR
* Nyckelord: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, webbplats

## RELATERADE LÄNKAR

[Get-AzRediscachePatchSchedule](./Get-AzRedisCachePatchSchedule.md)

[New-AzRediscachePatchSchedule](./New-AzRedisCachePatchSchedule.md)

[Remove-AzRediscachePatchSchedule](./Remove-AzRedisCachePatchSchedule.md)


