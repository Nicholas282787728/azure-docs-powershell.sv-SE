---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 8b84028bc9da854b5aa749867a8759b71d9f7b63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233583"
---
# Stop-AzBatchTask

## SYNOPSIS
Stoppar en batchaktivitet.

## SYNTAX

### Id
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Stop-AzBatchTask** stoppar en Azure Batch-uppgift.

## EXEMPEL

### Exempel 1: Ta bort en batchaktivitet med ID
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

Det här kommandot avbryter en aktivitet som har ID-aktiviteten23 under jobbet som har ID-jobbet-0000001.
Kommandot uppmanar dig att bekräfta.
Använd cmdlet Get-AzBatchAccountKey-cmdleten för att tilldela en kontext till $Context variabeln.

### Exempel 2: Stoppa en batchaktivitet med hjälp av förloppsförloppet
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

Det här kommandot hämtar den batchaktivitet som har ID-aktiviteten26 i jobbet som har ID-jobbet-0000001 med hjälp av cmdleten Get-AzBatchTask-id:t.
Kommandot skickar aktiviteten till den aktuella cmdleten med hjälp av rörledningsoperatorn.
Kommandot stoppar aktiviteten.

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

### -Id
Anger ID för aktiviteten som cmdleten stoppar.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
Anger ID för jobbet som innehåller aktiviteten.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Uppgift
Anger aktiviteten som cmdleten stoppar.
Om du vill hämta **ett PSCloudTask-objekt** använder du Get-AzBatchTask-cmdleten.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
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

### System.String

### Microsoft.Azure.Commands.Batkap. Models.PSCloudTask

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## UTDATA

### System.Void

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzBatchTask](./Get-AzBatchTask.md)

[New-AzBatchTask](./New-AzBatchTask.md)

[Remove-AzBatchTask](./Remove-AzBatchTask.md)

[Azure-batch-cmdlets](/powershell/module/Az.Batch/)
