---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 575c2e8a7e510f3c8b3808b4ed6ce9169cd4f21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233598"
---
# Remove-AzBatchPool

## SYNOPSIS
Tar bort den angivna batchpoolen.

## SYNTAX

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzBatchPool** tar bort den angivna Azure Batch-poolen.
Du uppmanas att bekräfta detta såvida du inte använder *force-parametern.*

## EXEMPEL

### Exempel 1: Ta bort en batchpool med pool-ID
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

Det här kommandot tar bort poolen med ID MyPool.
Användaren uppmanas att bekräfta åtgärden innan borttagningen utförs.

### Exempel 2: Ta bort alla batchpooler genom tvingad
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

Det här kommandot tar bort alla batchpooler.
Eftersom *force-parametern* finns utelämnas bekräftelsemeddelandet.

## PARAMETERS

### -BatchContext
Anger **batchaccountContext-instansen** som denna cmdlet använder för att interagera med batchtjänsten.
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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
Anger ID för poolen som ska tas bort.
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

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchPool](./Get-AzBatchPool.md)

[New-AzBatchPool](./New-AzBatchPool.md)

[Azure-batch-cmdlets](/powershell/module/Az.Batch/)
