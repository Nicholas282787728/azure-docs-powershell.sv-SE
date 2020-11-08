---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099205"
---
# New-AzureSiteRecoveryStorageMapping

## Sammanfattning
Skapar en mappning mellan ett Azure-lagringssystem och ett återställnings objekt.

## FRÅGESYNTAXEN

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureSiteRecoveryStorageMapping** skapar en mappning mellan ett Azure Site Recovery-hanterat primärt Azure-lagringssystem och ett återställnings objekt.

## BESKRIVS

### Exempel 1: skapa en mappning mellan ett lagrings objekt och ett återställnings objekt
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

Den första kommando cmdleten hämtar servrar för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryServer** .
Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.

Det andra kommandot får webbplatsen för webbplats återställning för den första servern i $Servers matris och lagrar den sedan i $Storages.

Med kommandot slut skapas en mappning mellan det primära nätverket och återställnings nätverket.
Kommandot anger det primära lagrings objekt som det första elementet i $Storages.
Kommandot anger återställnings objekt som det andra elementet i $Storages.

## MALLPARAMETRAR

### -PrimaryStorage
Anger primär lagrings utrymmet som ska mappas till återställnings lagringen.
Använd Get-AzureSiteRecoveryStorage cmdlet för att få ett **ASRStorage** -objekt.

```yaml
Type: ASRStorage
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

### -RecoveryStorage
Anger återställnings objekt.
Denna cmdlet mappar det primära lagrings objekt till det lagrings objekt som den här parametern anger.
För att få ett **ASRStorage** -objekt, Använd **Get-AzureSiteRecoveryStorage**.

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
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

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)

[Get-AzureSiteRecoveryStorageMapping](./Get-AzureSiteRecoveryStorageMapping.md)

[Remove-AzureSiteRecoveryStorageMapping](./Remove-AzureSiteRecoveryStorageMapping.md)


