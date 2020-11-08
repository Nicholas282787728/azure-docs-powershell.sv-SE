---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099782"
---
# Get-AzureStorSimpleAccessControlRecord

## Sammanfattning
Hämtar åtkomst kontroll poster i en tjänst konfiguration.

## FRÅGESYNTAXEN

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorSimpleAccessControlRecord** hämtar åtkomst kontroll poster i StorSimple Manager-tjänstens konfiguration.
Denna cmdlet hämtar alla poster eller en namngiven post.

Åtkomst kontroll poster är behållare för iSCSI Initiator-parametrar.
Dessa parametrar anger vilka initierare som kan komma åt en volym.
När en iSCSI-initieraren försöker ansluta till en volym kontrollerar din enhet vilka åtkomst kontroll poster som har tilldelats till volymen.
Om parametrarna för iSCSI-initieraren matchar en av posterna i en åtkomst kontroll post som mappats till den volymen kan iSCSI-initieraren ansluta.

## BESKRIVS

### Exempel 1: Hämta alla åtkomst kontroll poster
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

Det här kommandot får alla åtkomst kontroll poster.

### Exempel 2: Hämta en specifik åtkomst kontroll post
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

Det här kommandot får åtkomst kontroll posten med namnet Acr11.

## MALLPARAMETRAR

### -ACRName
Anger namnet på en åtkomst kontroll post som ska visas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger en Azure-profil.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### AccessControlRecord, IList\<AccessControlRecord\>
Denna cmdlet returnerar ett **AccessControlRecord** -objekt eller **ett \<AccessControlRecord\> ilist** -objekt.
Ett **AccessControlRecord** -objekt innehåller följande fält: 

- **GlobalId** ( **sträng** ) 
- **InitiatorName** ( **sträng** ) 
- **InstanceID** ( **sträng** ) 
- **Namn** ( **sträng** ) 
- **OperationInProgress** ( **OperationInProgress** ) 
- **VolumeCount** ( **int** )

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Remove-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)


