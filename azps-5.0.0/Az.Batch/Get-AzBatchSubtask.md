---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 4a1278734e6c9f40dc7495acb92f847d7b2cd32d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321799"
---
# Get-AzBatchSubtask

## Sammanfattning
Hämtar under aktivitetens information för den angivna aktiviteten.

## FRÅGESYNTAXEN

### ODataFilter (standard)
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzBatchSubtask** hämtar under aktivitetens information om den angivna uppgiften.
Under aktiviteter ger parallell bearbetning för enskilda uppgifter och möjliggör noggrann övervakning av aktivitets körning och förlopp.

## BESKRIVS

### Exempel 1: returnera alla under aktiviteter för en viss aktivitet
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

De här kommandona returnerar alla under aktiviteter för aktiviteten med aktivitets-ID: t.
För att göra detta skapar det första kommandot i exemplet en objekt referens till konto nycklarna för batch-contosobatchaccount.
Denna objekt referens lagras i en variabel som heter $context.
Med det andra kommandot används den objekt referensen och cmdleten **Get-AzBatchSubtask** för att returnera alla under aktiviteter för min aktivitet, en aktivitet som körs som en del av jobb jobbet – 01.

## MALLPARAMETRAR

### -BatchContext
Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.
Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten. Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda. När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard. Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.

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

### -JobId
Anger ID för det jobb som innehåller den aktivitet vars under aktiviteter den här cmdleten får.

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
Anger det maximala antalet under aktiviteter som ska returneras.
Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.
Standardvärdet är 1000.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aktivitets
Anger en objekt referens till aktiviteten som innehåller de under aktiviteter som denna cmdlet returnerar.
Denna objekt referens skapas med Get-AzBatchTask cmdlet och det returnerade objektet lagras i en variabel.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskId
Anger ID för den aktivitet vars under aktiviteter den här cmdleten returnerar.

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## VÄRDEN

### Microsoft.Azure.Commands.BatCH. Modeller. PSSubtaskInformation

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzBatchTask](./Get-AzBatchTask.md)


