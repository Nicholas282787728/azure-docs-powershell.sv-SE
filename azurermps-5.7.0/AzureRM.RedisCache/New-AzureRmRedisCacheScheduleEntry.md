---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 2f43cfa1e10fe115f8bf5fc94404f532f04f6573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755242"
---
# New-AzureRmRedisCacheScheduleEntry

## Sammanfattning
Skapar en schema post.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmRedisCacheScheduleEntry** skapar ett **PSScheduleEntry** -objekt.
Azure Redis cache-korrigering Schemalägg cmdlets, till exempel New-AzureRmRedisCachePatchSchedule cmdlet, kräver schemaläggning av objekt.

## BESKRIVS

### Exempel 1: skapa en schema post för helger
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

Det här kommandot skapar ett **PSScheduleEntry** -objekt som representerar ett helg schema med angiven start tid och det angivna fönstret.

## MALLPARAMETRAR

### -DayOfWeek
Anger vecko dagen för schema posten.
De acceptabla värdena för den här parametern är:

- Vardaglig 
- Migration 
- Dagarna 
- Torsdag 
- Onsdagen 
- Torsdag 
- Fredag 
- Afton 
- Lördag

```yaml
Type: String
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
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindow
Anger hur länge fönster tillåts för uppdateringar.

```yaml
Type: TimeSpan
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
Type: Int32
Parameter Sets: (All)
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

### Ingen
Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.

## VÄRDEN

### Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry
Denna cmdlet returnerar ett objekt för schemaläggning.

## ANMÄRKNINGAR
* Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats

## RELATERADE LÄNKAR

[Get-AzureRmRedisCachePatchSchedule](./Get-AzureRmRedisCachePatchSchedule.md)

[New-AzureRmRedisCachePatchSchedule](./New-AzureRmRedisCachePatchSchedule.md)

[Remove-AzureRmRedisCachePatchSchedule](./Remove-AzureRmRedisCachePatchSchedule.md)


