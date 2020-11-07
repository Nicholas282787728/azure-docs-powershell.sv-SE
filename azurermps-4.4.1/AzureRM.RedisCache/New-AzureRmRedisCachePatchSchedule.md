---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: b04977869364f43644556b9ef6bf16ac68d01f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755648"
---
# New-AzureRmRedisCachePatchSchedule

## Sammanfattning
Lägger till ett uppdaterings schema.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmRedisCachePatchSchedule** lägger till ett uppdaterings schema i ett cache i Azure Redis-cachen.

## BESKRIVS

### Exempel 1: skapa och lägga till ett uppdaterings schema i cachen
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

Det här kommandot lägger till ett uppdaterings schema i cachen med namnet RedisCache06.
Parametern värden tar ett kommando som använder **nya-AzureRmRedisCacheScheduleEntry** för att skapa ett schema.

## MALLPARAMETRAR

### -Poster
Anger en matris med scheman som denna cmdlet ställer in i cacheminnet. För att hämta ett **PSScheduleEntry** -objekt, Använd cmdleten New-AzureRmRedisCacheScheduleEntry.

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på cachen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som innehåller cacheminnet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Ingen
Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.

## VÄRDEN

### Microsoft. Azure. commands. RedisCache. Models. PSScheduleEntry
Den här cmdleten returnerar de ändrings schema poster som är inställda i cacheminnet.

## ANMÄRKNINGAR
* Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, Redis, cache, Web, webapp, webbplats

## RELATERADE LÄNKAR

[Get-AzureRmRedisCachePatchSchedule](./Get-AzureRmRedisCachePatchSchedule.md)

[New-AzureRmRedisCacheScheduleEntry](./New-AzureRmRedisCacheScheduleEntry.md)

[Remove-AzureRmRedisCachePatchSchedule](./Remove-AzureRmRedisCachePatchSchedule.md)


