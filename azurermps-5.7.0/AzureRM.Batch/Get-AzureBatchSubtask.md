---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 8e3633e88bc3c0972df0d667ed1002571d5ec142
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574425"
---
# Get-AzureBatchSubtask

## Sammanfattning
Hämtar under aktivitetens information för den angivna aktiviteten.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ODataFilter (standard)
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureBatchSubtask** hämtar under aktivitetens information om den angivna uppgiften.
Under aktiviteter ger parallell bearbetning för enskilda uppgifter och möjliggör noggrann övervakning av aktivitets körning och förlopp.

## BESKRIVS

### Exempel 1: returnera alla under aktiviteter för en viss aktivitet
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

De här kommandona returnerar alla under aktiviteter för aktiviteten med aktivitets-ID: t.
För att göra detta skapar det första kommandot i exemplet en objekt referens till konto nycklarna för batch-contosobatchaccount.
Denna objekt referens lagras i en variabel som heter $context.

Med det andra kommandot används den objekt referensen och cmdleten **Get-AzureBatchSubtask** för att returnera alla under aktiviteter för min aktivitet, en aktivitet som körs som en del av jobb jobbet – 01.

## MALLPARAMETRAR

### -BatchContext
Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.
Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten. Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda. När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard. Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.

```yaml
Type: BatchAccountContext
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Anger ID för det jobb som innehåller den aktivitet vars under aktiviteter den här cmdleten får.

```yaml
Type: String
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
Type: Int32
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
Denna objekt referens skapas med Get-AzureBatchTask cmdlet och det returnerade objektet lagras i en variabel.

```yaml
Type: PSCloudTask
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
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### BatchAccountContext
Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline

### PSCloudTask
Parametern ' Task ' godkänner värdet av typen ' PSCloudTask ' från pipeline

## VÄRDEN

###  
Denna cmdlet returnerar instanser av **PSSubtaskInformation** -objektet.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureBatchTask](./Get-AzureBatchTask.md)


