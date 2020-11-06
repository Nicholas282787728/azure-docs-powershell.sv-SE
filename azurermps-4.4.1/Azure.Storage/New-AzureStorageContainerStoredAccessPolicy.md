---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3429c142ce31f8cd08786e180b6725130501ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575076"
---
# New-AzureStorageContainerStoredAccessPolicy

## Sammanfattning
Skapar en lagrad åtkomst princip för en Azure Storage-behållare.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureStorageContainerStoredAccessPolicy** skapar en lagrad åtkomst princip för en Azure Storage-behållare.

## BESKRIVS

### Exempel 1: skapa en lagrad åtkomst princip i en lagrings behållare
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

Det här kommandot skapar en åtkomst princip med namnet Policy01 i lagrings behållaren som heter $.

## MALLPARAMETRAR

### -ClientTimeoutPerRequest
Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.
Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.
Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Anger maximalt antal samtidiga nätverks samtal.
Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.
Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.
Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.
Standardvärdet är 10.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Container
Anger namnet på Azure-lagringsplatsen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Kontext
Anger en Azure Storage-kontext.
Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
Anger den tid då den lagrade åtkomst policyn blir ogiltig.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tillstånd
Anger behörigheter i den lagrade åtkomst principen för att komma åt behållaren.

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

### -Princip
Anger en lagrad åtkomst princip som innehåller behörigheter för denna SAS-token.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.
Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.
Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Anger den tid då den lagrade åtkomst policyn blir giltig.

```yaml
Type: DateTime
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

### Strängvärdet

Parametern "container" accepterar värdet för typen String från pipeline

### IStorageContext

Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline

## VÄRDEN

### System. String

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorageContainerStoredAccessPolicy](./Get-AzureStorageContainerStoredAccessPolicy.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)

[Remove-AzureStorageContainerStoredAccessPolicy](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[Set-AzureStorageContainerStoredAccessPolicy](./Set-AzureStorageContainerStoredAccessPolicy.md)


