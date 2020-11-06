---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dd17eef73ab07d662a10177ffb68776aa4ec6016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582248"
---
# Update-AzureRmRecoveryServicesAsrNetworkMapping

## Sammanfattning
Uppdaterar den angivna nätverks mappningen för automatisk system återställning.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByNetworkObject (standard)
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Update-AzureRmRecoveryServicesAsrNetworkMapping** uppdaterar den angivna nätverks mappningen för Azure Site Recovery.

## BESKRIVS

### Exempel 1
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

Startar uppdateringen av nätverks mappningen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.

## MALLPARAMETRAR

### -InputObject
Input-objekt: anger det nätverks mappnings objekt för ASR som motsvarar nätverks mappningen för automatisk system återställning 

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryAzureNetworkId
Anger återställnings-nätverks-ID för nätverks mappningen.

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

### -RecoveryNetwork
Anger återställnings nätverks objekt för nätverks mappningen.

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

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
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

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

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

