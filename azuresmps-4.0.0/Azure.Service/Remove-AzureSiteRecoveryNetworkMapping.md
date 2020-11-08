---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099340"
---
# Remove-AzureSiteRecoveryNetworkMapping

## Sammanfattning
Tar bort en nätverks mappning från ett återställnings valv för webbplatser.

## FRÅGESYNTAXEN

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureSiteRecoveryNetworkMapping** tar bort en nätverks mappning från det aktuella Azure Site Recovery-valvet.

## BESKRIVS

### Exempel 1: ta bort mappningen mellan ett nätverk och ett återställnings nätverk
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Den första kommando cmdleten hämtar servrar för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryServer** .
Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.

Det andra kommandot får mappningen mellan det primära nätverket och återställnings nätverket och lagrar det i $NetworkMapping variabeln.
Kommandot anger den primära servern för nätverks mappningen som det första elementet i $Servers.
Kommandot anger Server för återställnings nätverket som det andra $Servers.

Kommandot tar bort nätverks mappningen i $NetworkMapping.

### Exempel 2: ta bort mappningen mellan ett nätverk och ett virtuellt Azure-nätverk
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Den första kommando cmdleten hämtar servrar för det aktuella Site Recovery-valvet.
Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.

Det andra kommandot får en mappning mellan det primära nätverket och ett nätverk med Azure Virtual Machine och lagrar det sedan i $NetworkMapping variabel.
Kommandot anger det primära servern för nätverket som det första elementet i $Servers.
Kommandot anger *Azure* -parametern.
Därför hämtas kommandot till en virtuell Azure-dator.

Kommandot tar bort nätverks mappningen i $NetworkMapping.

## MALLPARAMETRAR

### -NetworkMapping
Anger den nätverks mappning som ska tas bort.

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[New-AzureSiteRecoveryNetworkMapping](./New-AzureSiteRecoveryNetworkMapping.md)

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)


