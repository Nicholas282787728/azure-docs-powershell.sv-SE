---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093309"
---
# Get-AzureSiteRecoveryRecoveryPlanFile

## Sammanfattning
Laddar ned en Azure Site Recovery-plan i XML-format.

## FRÅGESYNTAXEN

### ByRPObject (standard)
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureSiteRecoveryRecoveryPlanFile** laddar ned en Azure Site Recovery-plan i XML-format.
Du kan använda den här filen för att uppdatera återställnings planen och sedan överföra den till Site Recovery Server.

En återställnings plan samlar virtuella datorer i en grupp för användning av redundans och återställning.

## BESKRIVS

### Exempel 1: skaffa en återställnings plan fil
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

Det här kommandot använder cmdleten **Get-AzureSiteRecoveryRecoveryPlan** för att få återställnings planen och lagrar den sedan i $RecoveryPlan variabel.

Det andra kommandot använder cmdleten **GetAzureSiteRecoveryRecoveryPlanFile** för att hämta en XML-fil för återställnings plan i $RecoveryPlan.
Kommandot lagrar XML-filen på den angivna sökvägen.

## MALLPARAMETRAR

### -ID
Anger ID för den återställnings plan som ska erhållas.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Anger den fullständiga sökvägen för att lagra en återställnings plan XML-fil.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -RecoveryPlan
Anger ett **ASRRecoveryPlan** -objekt som du vill hämta återställnings planen från.
För att få ett **ASRRecoveryPlan** -objekt, Använd cmdleten **Get-AzureSiteRecoveryRecoveryPlan** .

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureSiteRecoveryRecoveryPlan](./Get-AzureSiteRecoveryRecoveryPlan.md)


