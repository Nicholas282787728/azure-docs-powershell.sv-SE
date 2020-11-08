---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093338"
---
# Get-AzureSchedulerJobCollection

## Sammanfattning
Hämtar jobb samlingar för schemaläggare.

## FRÅGESYNTAXEN

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Cmdleten **Get-AzureSchedulerJobCollection** får en eller flera jobb samlingar för schemaläggare.

## BESKRIVS

### Exempel 1: Hämta alla samlingar
```
PS C:\> Get-AzureSchedulerJobCollection
```

Det här kommandot får alla jobb samlingar för schemaläggare på alla platser i det aktuella abonnemanget.

### Exempel 2: Hämta alla samlingar för en plats
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

Det här kommandot får alla jobb samlingar i Schemaläggaren på platsen norra Central oss.

### Exempel 3: Hämta en samling med hjälp av ett namn
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

Det här kommandot får jobb samlingen Schemaläggaren med namnet JobCollection01.

## MALLPARAMETRAR

### -JobCollectionName
Anger namnet på jobb samlingen i Schemaläggaren som ska visas.

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

### -Plats
Anger namnet på platsen där moln tjänsten är värd.
Giltiga värden är: 

- Världen över
- Överallt i Europa
- Var du än är
- Östasien
- Östra USA
- Norra Central USA
- Nord Europa
- Södra centrala USA
- Sydostasien
- Västeuropa
- Västra USA

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

[New-AzureSchedulerJobCollection](./New-AzureSchedulerJobCollection.md)

[Remove-AzureSchedulerJobCollection](./Remove-AzureSchedulerJobCollection.md)

[Set-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)


