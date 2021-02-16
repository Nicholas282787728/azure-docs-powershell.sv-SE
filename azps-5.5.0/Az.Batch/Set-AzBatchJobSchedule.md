---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233590"
---
# Set-AzBatchJobSchedule

## SYNOPSIS
Anger ett jobbschema.

## SYNTAX

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzBatch Och schemalagda** scheman anger ett jobbschema i Azure Batch-tjänsten.

## EXEMPEL

### Exempel 1: Uppdatera ett jobbschema
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

Det första kommandot får ett jobb med hjälp av **Get-AzBatchKommandoSchedule** och lagrar det sedan i $JobSchedule variabeln.
Det andra kommandot ändrar upprepningsintervallet för `$JobSchedule.Schedule` objektet.
Det slutliga kommandot uppdaterar batchtjänsten så att den matchar det lokala objektet i $JobSchedule.

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

### -JobSchedule
Anger ett **PSCloudCloudSchedule-objekt** som representerar ett jobbschema.
Om du vill hämta **ett PSCloudCloudSchedule-objekt** använder du Get-AzBatchJobSchedule-cmdleten.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Batkap. Models.PSCloudCloudSchedule

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## UTDATA

### System.Void

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Disable-AzBatch Det här är AzBatch Ochchedule](./Disable-AzBatchJobSchedule.md)

[Enable-AzBatch Utsläckt](./Enable-AzBatchJobSchedule.md)

[Get-AzBatch Utsläckt](./Get-AzBatchJobSchedule.md)

[New-AzBatch Utsläckt](./New-AzBatchJobSchedule.md)

[Remove-AzBatch Utsläckt](./Remove-AzBatchJobSchedule.md)

[Stop-AzBatch Det här är](./Stop-AzBatchJobSchedule.md)


