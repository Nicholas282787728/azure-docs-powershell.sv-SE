---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099565"
---
# Get-AzureMediaServicesAccount

## Sammanfattning
Får tillgängliga Azure Media Services-konton.

**Obs!** Den här versionen är föråldrad, se den [senaste versionen](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).

## FRÅGESYNTAXEN

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Om du vill visa alla konton använder du `Get-AzureMediaServicesAccount` cmdleten.
Om du vill ha mer detaljerad information om ett visst konto använder du `Get-AzureMediaServicesAccount -Name YourAccountName` cmdleten.

## BESKRIVS

### Exempel 1: lista alla medie tjänst konton
```
PS C:\> Get-AzureMediaServicesAccount
```

Det här kommandot visar alla tillgängliga medie tjänst konton.

### Exempel 2: få detaljerad information om ett media tjänst konto
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

Det här kommandot visar egenskaper för ett Media Services-konto.

## MALLPARAMETRAR

### -Namn
Medie tjänstens konto namn.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
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

[Använda Azure PowerShell för medie tjänster](https://go.microsoft.com/fwlink/?LinkId=324179)


