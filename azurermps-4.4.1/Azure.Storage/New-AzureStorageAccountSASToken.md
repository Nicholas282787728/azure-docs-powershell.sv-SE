---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8b280a13e7eb7a2e6ea3f52b4a121f313504b2ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573803"
---
# New-AzureStorageAccountSASToken

## Sammanfattning
Skapar en SAS-token på konto nivå.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureStorageSASToken** skapar en SAS-token för ett Azure Storage-konto.

Du kan använda SAS-token för att delegera behörigheter för flera tjänster eller för att delegera behörigheter för tjänster som inte är tillgängliga med en SAS-token på objekt nivå.

## BESKRIVS

### Exempel 1: skapa en SAS-token på konto nivå med fullständig behörighet
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

Det här kommandot skapar en SAS-token på konto nivå med fullständig behörighet.

### Exempel 2: skapa en SAS-token på konto nivå för ett intervall med IP-adresser
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Det här kommandot skapar en SAS-token på konto nivå för HTTPS-Only-begäranden från det angivna IP-adressintervallet.

## MALLPARAMETRAR

### -Kontext
Anger Azure Storage-kontexten.
Du kan använda New-AzureStorageContext cmdlet för att hämta ett **AzureStorageContext** -objekt.

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
Anger behörigheterna för lagrings kontot.
Behörigheter är bara giltiga om de stämmer överens med den angivna resurs typen.
Mer information om acceptabla behörighets värden finns i skapa en konto-SÄKERHETSASSOCIATIONERhttps://go.microsoft.com/fwlink/?LinkId=799514

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

### -Protokoll
Anger det protokoll som tillåts för en begäran som gjorts med konto säkerhets associationen.
De acceptabla värdena för den här parametern är:

- HttpsOnly
- HttpsOrHttp

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

### -ResourceType
Anger vilka resurs typer som är tillgängliga med SAS-token.
De acceptabla värdena för den här parametern är:

- Ingen
- Serv
- Beh
- Serverobjektet

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Service
Anger tjänsten.
De acceptabla värdena för den här parametern är:

- Ingen
- Object
- Fil
- Svarskö
- Tabell

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Anger tiden, som ett **datetime** -objekt där säkerhets associationen blir giltig.
Använd Get-Date cmdlet för att få ett **datetime** -objekt.

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

## VÄRDEN

### System. String

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)

[New-AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)

[New-AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)

[New-AzureStorageQueueSASToken](./New-AzureStorageQueueSASToken.md)

[New-AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)

[New-AzureStorageTableSASToken](./New-AzureStorageTableSASToken.md)


