---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269655"
---
# Get-AzBatchTaskCount

## Sammanfattning
Hämtar antalet aktiviteter för det angivna jobbet.

## FRÅGESYNTAXEN

### Et
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzBatchTaskCount** hämtar antalet Azure Batch-uppgifter för ett batchjobb.
Ange ett jobb genom parametern *jobId* eller *jobb* parameter.
Med aktivitets antal får du ett antal aktiviteter som är aktiva, kör eller slutförda aktivitets tillstånd och antalet uppgifter som lyckades eller misslyckades. Uppgifter i tillståndet för att förbereda räknas som körs. Om validationStatus är avverifierat har batch-tjänsten inte kunnat kontrol lera status för de uppgifter som rapporter ATS i API för List aktiviteter. ValidationStatus kan vara avverifierad om jobbet innehåller fler än 200 000 uppgifter.

## BESKRIVS

### Exempel 1: Hämta antal aktiviteter efter ID
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Det här kommandot får antalet aktiviteter för jobbet Job01.
Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.

## MALLPARAMETRAR

### -BatchContext
Den BatchAccountContext-instans som ska användas vid interaktion med kommando tjänsten.
Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.
Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.
När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.
Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.

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

### -Jobb
Anger det jobb som innehåller uppgifter som denna cmdlet får.
För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzBatchJob.

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
ID för det jobb som du vill hämta aktiviteter för.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## VÄRDEN

### Microsoft.Azure.Commands.BatCH. Modeller. PSTaskCounts

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Cmdlets för Azure Batch](/powershell/module/Az.Batch/)
