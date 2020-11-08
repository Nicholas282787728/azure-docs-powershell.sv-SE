---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099779"
---
# Get-AzureStorSimpleResourceContext

## Sammanfattning
Hämtar den aktuella resurs kontexten.

## FRÅGESYNTAXEN

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorSimpleResourceContext** hämtar den aktuella resurs kontexten.

## BESKRIVS

### Exempel 1: hämta den aktuella kontexten
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

Det första kommandot ställer in den aktuella kontexten så att den blir resursen som heter Contoso63-Tsqa genom att använda cmdleten **Select-AzureStorSimpleResource** .

Det andra kommandot får den aktuella resurs kontexten.

### Exempel 2: försök att hämta den aktuella kontexten
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

Det här kommandot får den aktuella kontexten.
I det här exemplet har ingen kontext ställts in.
Kommandot returnerar ett meddelande som förklarar problemet.

## MALLPARAMETRAR

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

### StorSimpleResourceContext
Denna cmdlet returnerar ett **ResourceContext** -objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Select-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


