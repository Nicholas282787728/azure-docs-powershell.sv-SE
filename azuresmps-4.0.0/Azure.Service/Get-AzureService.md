---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099539"
---
# Get-AzureService

## Sammanfattning
Returnerar ett objekt med information om moln tjänsterna för det aktuella abonnemanget.

## FRÅGESYNTAXEN

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureService** returnerar ett List objekt med alla Azure Cloud-tjänster som är kopplade till det aktuella abonnemanget.
Om du anger *ServiceName* -parametern returnerar **Get-AzureService** information om den matchande tjänsten.

## BESKRIVS

### Exempel 1: få information om alla tjänster
```
PS C:\> Get-AzureService
```

Det här kommandot returnerar ett objekt som innehåller information om alla Azure-tjänster som är kopplade till det aktuella abonnemanget.

### Exempel 2: Hämta information om en viss tjänst
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

Det här kommandot returnerar information om $MySvc tjänsten.

### Exempel 3: Visa tillgängliga metoder och egenskaper
```
PS C:\> Get-AzureService | Get-Member
```

Det här kommandot visar de egenskaper och metoder som är tillgängliga i cmdleten **Get-AzureService** .

## MALLPARAMETRAR

### -InformationAction
Anger hur den här cmdleten svarar på en informations händelse.

De acceptabla värdena för den här parametern är:

- Vidare
- Över
- Inquire
- SilentlyContinue
- Stanna
- Avbryt

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Anger en informations variabel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ServiceName
Anger namnet på den tjänst där informationen ska returneras.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### HostedServiceContext

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureService](./New-AzureService.md)

[Set-AzureService](./Set-AzureService.md)


