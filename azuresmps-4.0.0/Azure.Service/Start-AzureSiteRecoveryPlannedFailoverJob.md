---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093477"
---
# Start-AzureSiteRecoveryPlannedFailoverJob

## Sammanfattning
Startar en planerad redundansväxling för en webbplats återställning.

## FRÅGESYNTAXEN

### ByRPId (standard)
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPEId
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPEObject
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Start-AzureSiteRecoveryPlannedFailoverJob** startar en planerad redundans för en entitet eller återställnings plan för Azure Site Recovery-skydd.
Du kan kontrol lera om jobbet följer med cmdleten **Get-AzureSiteRecoveryJob** .

## BESKRIVS

### Exempel 1: starta ett planerat redundans jobb
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

Det första kommandot får alla skyddade behållare i det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryProtectionContainer** och lagrar sedan resultatet i variabeln $container.
I det här exemplet finns det en enda behållare.

Det andra kommandot hämtar de skyddade virtuella datorerna som tillhör behållaren som lagras i $Container genom att använda cmdleten **Get-AzureSiteRecoveryProtectionEntity** .
Kommandot lagrar resultaten i variabeln $Protected.

Med kommandot sista startas jobbet redundans i riktningen PrimaryToRecovery för de skyddade virtuella datorerna i $Protected.

## MALLPARAMETRAR

### -Riktning
Anger riktningen för redundansväxlingen.
De acceptabla värdena för den här parametern är:

- PrimaryToRecovery
- RecoveryToPrimary

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

### -Optimera
Ange vad du vill optimera för.
Den här parametern gäller för redundans från en Azure-webbplats till en lokal plats som kräver en omfattande datasynkronisering.
De acceptabla värdena för den här parametern är:

- ForDowntime
- ForSynchronization

När **ForDowntime** anges visar detta att data är synkroniserade innan redundans för att minimera nertid.
Synkroniseringen utförs utan att stänga av den virtuella datorn.
När synkroniseringen är klar är jobbet inaktiverat.
Återuppta jobbet för att utföra ytterligare en synkronisering som stänger av den virtuella datorn.

När **ForSynchronization** anges visar detta att data synkroniseras endast under redundans så att datasynkroniseringen är minimerad.
Eftersom den här inställningen är aktive rad avslutas den virtuella datorn omedelbart.
Synkroniseringen startar efter avstängning för att slutföra redundansväxlingen.

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

### -ProtectionContainerId
Anger ID: t för den skyddade behållare som jobbet ska startas för.

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionEntity
Anger objektet för webbplats återställnings skydd.

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionEntityId
Anger ett **ASRProtectionEntity** -objekt som jobbet ska startas med.
För att få ett **ASRProtectionEntity** -objekt, Använd cmdleten **Get-AzureSiteRecoveryProtectionEntity** .

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
Anger ett återställnings plan objekt.

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

### -RPId
Anger ID för en återhämtnings plan som jobbet ska startas med.

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForCompletion
Anger att cmdleten väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.

```yaml
Type: SwitchParameter
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

[Get-AzureSiteRecoveryProtectionContainer](./Get-AzureSiteRecoveryProtectionContainer.md)

[Get-AzureSiteRecoveryProtectionEntity](./Get-AzureSiteRecoveryProtectionEntity.md)


