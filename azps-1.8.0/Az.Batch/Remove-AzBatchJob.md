---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 4d15680902cb324561983877fef317d20ed94704
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755068"
---
# Remove-AzBatchJob

## Sammanfattning
Tar bort ett batchjobb.

## FRÅGESYNTAXEN

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzBatchJob** tar bort ett Azure-batchjobb.
Denna cmdlet ber dig bekräfta att du vill ta bort ett jobb, såvida du inte anger parametern *Force* .

## BESKRIVS

### Exempel 1: ta bort ett batchjobb
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

Det här kommandot tar bort jobbet med ID-000001.
Med kommandot uppmanas du att bekräfta innan jobbet tas bort.
Använd Get-AzBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.

### Exempel 2: ta bort ett batchjobb utan bekräftelse genom att använda pipeline
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

Det här kommandot får jobbet som har ID-000002 med hjälp av Get-AzBatchJob cmdlet.
Kommandot skickar jobbet till den aktuella cmdleten med hjälp av pipeline-operatorn.
Kommandot tar bort jobbet.
Eftersom kommandot @ innehåller parametern *Force* uppmanas du inte att bekräfta.

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

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Anger ID för det jobb som den här cmdleten tar bort.
Du kan inte ange jokertecken.

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

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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

[Disable-AzBatchJob](./Disable-AzBatchJob.md)

[Enable-AzBatchJob](./Enable-AzBatchJob.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Get-AzBatchAccountKeys](./Get-AzBatchAccountKey.md)

[New-AzBatchJob](./New-AzBatchJob.md)

[Stopp-AzBatchJob](./Stop-AzBatchJob.md)

[Cmdlets för Azure Batch](/powershell/module/az.batch)


