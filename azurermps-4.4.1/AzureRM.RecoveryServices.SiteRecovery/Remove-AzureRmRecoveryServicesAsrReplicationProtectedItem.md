---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 17836b900e56fdfd5d90211c9bceb79fce87c66e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758019"
---
# Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem

## Sammanfattning
Stoppar/inaktiverar replikering för ett skyddat objekt i Azure Site Recovery-replikering.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** inaktiverar replikeringen av angivet skyddat objekt för Azure Site Recovery-objektet.
Den här åtgärden gör att replikering stoppas för det skyddade objektet.

## BESKRIVS

### Exempel 1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

Startar åtgärden inaktivera replikering för det angivna replikerade skyddade objektet och returnerar det ASR-jobb som används för att spåra åtgärden.

## MALLPARAMETRAR

### -Force
Tvinga kommandot att köras utan ytterligare en varning.

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

### -InputObject
Indatavärdet till cmdleten: objektet Protected ASR-objekt som är kopplat till det replikerade objektet för replikering ska inaktive ras.

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WaitForCompletion
Anger att cmdleten ska vänta på att åtgärden ska slutföras innan den returneras.

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

### -Bekräfta
Ange om du vill bekräfta. Ange värdet för parametern Confirm till $false för att hoppa över bekräftelsen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs utan att köra cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem

## VÄRDEN

### Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmRecoveryServicesAsrReplicationProtectedItem](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[New-AzureRmRecoveryServicesAsrReplicationProtectedItem](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[Set-AzureRmRecoveryServicesAsrReplicationProtectedItem](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
