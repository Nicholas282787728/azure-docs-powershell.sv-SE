---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 0a809f9ef3d3c89edc7571b9bb7b7cc2f03e043b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758021"
---
# Get-AzureRmRecoveryServicesAsrVaultContext

## Sammanfattning
Hämtar information om inställningar för ASR-valv för Recovery Services-valvet.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmRecoveryServicesAsrVaultContext [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmRecoveryServicesAsrVaultContext** hämtar information om inställningar för ASR-valv relaterade till Recovery Services-valvet.

## BESKRIVS

### Exempel 1
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

Hämtar inställningar för ASR-valv för det aktiva (i PowerShell-sessionen) Recovery Services-valvet.

## MALLPARAMETRAR

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRVaultSettings

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

