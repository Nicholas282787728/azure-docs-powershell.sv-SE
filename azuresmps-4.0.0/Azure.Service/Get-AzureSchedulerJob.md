---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099541"
---
# Get-AzureSchedulerJob

## Sammanfattning
Hämtar en lista över jobb i schemaläggare eller ett visst jobb i Schemaläggaren.

## FRÅGESYNTAXEN

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Cmdleten **Get-AzureSchedulerJobCollection** hämtar en lista över jobb i schemaläggare eller ett visst jobb i Schemaläggaren.

## BESKRIVS

### Exempel 1: Hämta alla jobb i en samling
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

Det här kommandot hämtar schema jobb som är en del av jobb samlingen med namnet JobCollection01.

### Exempel 2: Hämta ett namngivet jobb
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

Det här kommandot får jobbet med namnet Job01 från samlingen med namnet JobCollection01 på den angivna platsen.

### Exempel 3: komma igång med jobb i en samling
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

Det här kommandot får alla inaktiverade schemaläggnings jobb som ingår i JobCollection01 på den angivna platsen.

## MALLPARAMETRAR

### -JobCollectionName
Anger namnet på den mängd som innehåller Schemaläggaren-jobbet som ska visas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobName
Anger namnet på ett jobb i Schemaläggaren som ska visas.

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

### -JobState
Anger tillståndet för de jobb du vill få.
De acceptabla värdena för den här parametern är:

- Aktiverat
- Aktiv
- Fel
- Rätta

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
De acceptabla värdena för den här parametern är:

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

Required: True
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

[Remove-AzureSchedulerJob](./Remove-AzureSchedulerJob.md)


