---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233606"
---
# Remove-AzBatchJob

## SYNOPSIS
Tar bort ett batchjobb.

## SYNTAX

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzBatch Det** här cmdleten tar bort ett Azure Batch-jobb.
Den här cmdleten uppmanar dig att bekräfta detta innan ett jobb tas bort, såvida du inte anger *force-parametern.*

## EXEMPEL

### Exempel 1: Ta bort ett batchjobb
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

Det här kommandot tar bort jobbet som har ID-jobbet-000001.
Du uppmanas att bekräfta kommandot innan jobbet tas bort.
Använd cmdlet Get-AzBatchAccountKey för att tilldela en kontext till den $Context variabeln.

### Exempel 2: Ta bort ett batchjobb utan bekräftelse med hjälp av pipelinen
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

Det här kommandot hämtar jobbet som har ID-jobbet-000002 med hjälp av cmdleten Get-AzBatchJob-cmdleten.
Kommandot skickar det jobbet till den aktuella cmdleten med hjälp av rörledningsoperatorn.
Kommandot tar bort det jobbet.
Eftersom kommandot innehåller *force-parametern* uppmanas du inte att bekräfta.

## PARAMETERS

### -BatchContext
Anger den **BatchAccountContext-instans** som denna cmdlet använder för att interagera med batchtjänsten.
Om du använder Get-AzBatchAccount-cmdleten för att hämta BatchAccountContext används Azure Active Directory-autentisering när du interagerar med batchtjänsten. Om du vill använda autentisering med delad nyckel i Get-AzBatchAccountKey använder du cmdleten för att få ett BatchAccountContext-objekt med dess snabbtangenter ifyllda. När du använder autentisering med delad nyckel används primärnyckeln som standard. Om du vill ändra nyckeln som ska användas anger du egenskapen BatchAccountContext.KeyInUse.

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
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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
Tvingar kommandot att köras utan att användaren uppmanas att bekräfta.

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

### -Id
Anger ID för det jobb som cmdleten tar bort.
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
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs.
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## UTDATA

### System.Void

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Disable-AzBatch Ent](./Disable-AzBatchJob.md)

[Enable-AzBatch Ent](./Enable-AzBatchJob.md)

[Get-AzBatch Ent](./Get-AzBatchJob.md)

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[New-AzBatch Ent](./New-AzBatchJob.md)

[Stop-AzBatch Ent](./Stop-AzBatchJob.md)

[Azure-batch-cmdlets](/powershell/module/Az.Batch/)
