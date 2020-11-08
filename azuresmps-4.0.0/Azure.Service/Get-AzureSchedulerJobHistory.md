---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099540"
---
# Get-AzureSchedulerJobHistory

## Sammanfattning
Hämtar historik för ett jobb i schemaläggare.

## FRÅGESYNTAXEN

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Cmdleten **Get-AzureSchedulerJobHistory** hämtar historiken för ett jobb i Schemaläggaren.

## BESKRIVS

### Exempel 1: Hämta historik för ett jobb med dess namn
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

Det här kommandot får historiken för jobbet som heter Job01.
Jobbet tillhör jobbet JobCollection01 på den angivna platsen.

### Exempel 2: Hämta historik för ett misslyckat jobb med dess namn
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

Det här kommandot får historiken för jobbet med namnet Job12 som har statusen Misslyckad.
Jobbet tillhör jobbet JobCollection01 på den angivna platsen.

## MALLPARAMETRAR

### -Först
Hämtar bara angivet antal objekt.
Ange antalet objekt som ska visas.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Rapporterar totalt antal objekt i data uppsättningen (ett heltal) följt av de markerade objekten.
Om cmdleten inte kan bestämma det totala antalet visar den "okänt antal". Heltalet har en egenskap för exakthet som anger tillförlitligheten hos det totala värdet.
Värdet för precisions intervall från 0,0 till 1,0 där 0,0 innebär att cmdleten inte kan räkna antalet objekt, ger 1,0 att antalet är exakt och ett värde mellan 0,0 och 1,0 tyder på en allt tillförlitlig uppskattning.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
Anger namnet på en jobb samling i Schemaläggaren.
Denna cmdlet hämtar historiken för ett jobb som tillhör samlingen som den här parametern anger.

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
Anger namnet på ett jobb i Schemaläggaren där historiken ska visas.

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

### -JobStatus
Anger statusen för Schemaläggaren-jobbet som du vill hämta historik för.
De acceptabla värdena för den här parametern är:

- Rätta
- Startade

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

### -Hoppa över
Ignorerar angivet antal objekt och hämtar sedan återstående objekt.
Ange antalet objekt som ska hoppas över.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureSchedulerJob](./Get-AzureSchedulerJob.md)

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)


