---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
ms.openlocfilehash: 44080736635a5b4e8964340aeeee448798ffaefc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577299"
---
# New-AzureStorageShareSASToken

## Sammanfattning
Generera signatur för delad åtkomst för Azure Storage Share.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### SasPolicy
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureStorageShareSASToken** skapar en signatur för delad åtkomst för en Azure-lagringsenhet.

## BESKRIVS

### Exempel 1: generera ett signatur-token för delad åtkomst för en resurs
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

Det här kommandot skapar ett signatur-token för delad åtkomst för resursen som heter ContosoShare.

### Exempel 2: generera flera signaturer med delad åtkomst med hjälp av pipeline
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

Det här kommandot får alla lagrings resurser som matchar prefixet.
Kommandot skickar dem till den aktuella cmdleten med hjälp av pipeline-operatorn.
Den aktuella cmdleten skapar en delad åtkomsttoken för varje lagrings resurs som har de angivna behörigheterna.

### Exempel 3: generera en signatur för signaturer som använder en delad åtkomst policy
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

Det här kommandot skapar ett signatur-token för delad åtkomst för lagrings resursen som heter ContosoShare och som har principen med namnet ContosoPolicy03.

## MALLPARAMETRAR

### -Kontext
Anger en Azure Storage-kontext.
Använd New-AzureStorageContext cmdlet för att få en kontext.

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
Anger den tid då den delade åtkomst-signaturen blir ogiltig.

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

### -FullUri
Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.

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

### -IPAddressOrRange
Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.
Intervallet är inkluderat.

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

### -Tillstånd
Anger behörigheterna i token för att komma åt resursen och filerna under resursen.

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Princip
Anger den lagrade åtkomst principen för en resurs.

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protokoll
Anger det protokoll som tillåts för en begäran.
De acceptabla värdena för den här parametern är:
* HttpsOnly
* HttpsOrHttp

Standardvärdet är HttpsOrHttp.

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShareName
Anger namnet på lagrings resursen.

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

### -StartTime
Anger den tid då den delade Access-signaturen blir giltig.

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

### IStorageContext

Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline

### Strängvärdet

Parametern ' ShareName ' godkänner värdet för typen ' String ' från pipeline

## VÄRDEN

### System. String

## ANMÄRKNINGAR
* Nyckelord: Allmänt, Azure, tjänster, data, lagring, BLOB, kö, tabell

## RELATERADE LÄNKAR

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[New-AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)
