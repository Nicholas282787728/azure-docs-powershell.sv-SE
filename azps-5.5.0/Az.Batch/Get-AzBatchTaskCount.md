---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239271"
---
# Get-AzBatchTaskCount

## SYNOPSIS
Hämtar antalet aktiviteter för det angivna jobbet.

## SYNTAX

### Id
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzBatchTaskCount** hämtar antalet Azure Batch-uppgifter för ett Batch-jobb.
Ange ett jobb med *parametern JobId* eller *jobparametern.*
Med antal aktiviteter räknas antalet aktiviteter efter aktiv, pågående eller slutförd aktivitet och antalet aktiviteter som har lyckats eller misslyckats. Aktiviteter i förberedelsetillståndet räknas som igång. Om verifieringsstatus är ej validerad har tjänsten Batch inte kunnat kontrollera statusräkning mot aktivitetstillstånd som rapporterats i API:t för listaktiviteter. Verifieringsstatus kan vara ej validerad om jobbet innehåller fler än 200 000 aktiviteter.

## EXEMPEL

### Exempel 1: Få antalet aktiviteter efter ID
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Med det här kommandot räknas antalet aktiviteter för jobbet01.
Använd cmdlet Get-AzBatchAccountKey för att tilldela en kontext till den $Context variabeln.

## PARAMETERS

### -BatchContext
BatchAccountContext-instansen som ska användas när du interagerar med batchtjänsten.
Om du använder Get-AzBatchAccount-cmdleten för att hämta BatchAccountContext används Azure Active Directory-autentisering när du interagerar med batchtjänsten.
Om du vill använda autentisering med delad nyckel i Get-AzBatchAccountKey använder du cmdleten för att få ett BatchAccountContext-objekt med dess snabbtangenter ifyllda.
När du använder autentisering med delad nyckel används primärnyckeln som standard.
Om du vill ändra nyckeln som ska användas anger du egenskapen BatchAccountContext.KeyInUse.

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

### -Job
Anger jobbet som innehåller aktiviteter som den här cmdleten hämtar.
Om du vill hämta **ett PSCloudCloudCloud-objekt** använder du Get-AzBatchJob-cmdleten.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
ID för det jobb som du vill räkna antalet aktiviteter för.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### Microsoft.Azure.Commands.Batkap. Models.PSCloudCloud

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## UTDATA

### Microsoft.Azure.Commands.Batkap. Models.PSTaskCounts

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatch Ent](./Get-AzBatchJob.md)

[Azure-batch-cmdlets](/powershell/module/Az.Batch/)
