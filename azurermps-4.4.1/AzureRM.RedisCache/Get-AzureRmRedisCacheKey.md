---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: e7e50488f69adb2b168453fd18264bf25a69942d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758018"
---
# Get-AzureRmRedisCacheKey

## Sammanfattning
Hämtar snabb tangenterna för en Redis cache.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmRedisCacheKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmRedisCacheKey** hämtar snabb tangenterna för Azure Redis-cachen.

## BESKRIVS

### Exempel 1: Hämta snabb tangenterna för en Redis cache
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

Det här kommandot får åtkomst nycklar som heter MyCacheKey.

## MALLPARAMETRAR

### -Namn
Anger namnet på en Redis-cache.

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
Anger namnet på den resurs grupp som innehåller Redis-cachen.

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

### Microsoft. Azure. Management. Redis. Models. RedisAccessKeys
Denna cmdlet returnerar primära och sekundära åtkomst nycklar för en Redis cache.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmRedisCacheKey](./New-AzureRmRedisCacheKey.md)


