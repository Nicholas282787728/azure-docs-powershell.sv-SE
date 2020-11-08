---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099809"
---
# Get-AzureRemoteAppTemplateImage

## Sammanfattning
Hämtar information om Azure RemoteApp-mallfiler.

## FRÅGESYNTAXEN

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRemoteAppTemplateImage** hämtar information om Azure RemoteApp-mallfiler i Microsoft Azure.
Denna cmdlet returnerar ett objekt som innehåller information om en viss Malltyp.
Om ingen Malltyp anges hämtar den information om alla mallfiler i det aktuella abonnemanget.

## BESKRIVS

### Exempel 1: få en lista över alla listmallar
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

Det här kommandot returnerar listan över alla listmallar.

### Exempel 2: Hämta information om en viss Malltyp
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

Det här kommandot hämtar information om den mallfiler som heter ContosoApps.

## MALLPARAMETRAR

### -ImageName
Anger namnet på en Azure RemoteApp-mallfil.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppStartMenuProgram](./Get-AzureRemoteAppStartMenuProgram.md)


