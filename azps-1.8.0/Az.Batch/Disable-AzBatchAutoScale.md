---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: d20a52c3e907bd981bc0a692ebb4aa44495d0960
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755146"
---
# Disable-AzBatchAutoScale

## Sammanfattning
Inaktiverar automatisk skalning av en pool.

## FRÅGESYNTAXEN

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **disable-AzBatchAutoScale** inaktiverar automatisk skalning för den angivna poolen.

## BESKRIVS

### Exempel 1: inaktivera automatisk skalning av en pool
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

Det här kommandot inaktiverar automatisk skalning för poolen med namnet min pool.

## MALLPARAMETRAR

### -BatchContext
Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.
Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten. Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda. När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard. Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -ID
Anger poolens objekt-ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## VÄRDEN

### System. Void

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Enable-AzBatchAutoScale](./Enable-AzBatchAutoScale.md)

[Test-AzBatchAutoScale](./Test-AzBatchAutoScale.md)

[Cmdlets för Azure Batch](/powershell/module/az.batch)


