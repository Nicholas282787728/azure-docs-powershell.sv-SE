---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 338e54a602391f1c7234445fa9b27713859d0089
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754700"
---
# Get-AzBatchLocationQuota

## Sammanfattning
Hämtar värdet för batch-tjänsten för din prenumeration på den angivna platsen.

## FRÅGESYNTAXEN

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämtar värdet för batch-tjänsten för angiven prenumeration på den angivna platsen.

## BESKRIVS

### Exempel 1: Hämta värdet för batch-tjänsten för abonnemanget i västra USA-regionen
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

Det här kommandot får kvoterna för det aktuella abonnemanget i västra USA-regionen.
Returvärdet visar att denna prenumeration endast kan skapa ett batch-konto i den regionen.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger den region som denna cmdlet kontrollerar kvoterna för.
Mer information finns i Azure-regioner ( https://azure.microsoft.com/regions) .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft.Azure.Commands.BatCH. Modeller. PSBatchLocationQuotas

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
