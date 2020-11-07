---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryDataset.md
ms.openlocfilehash: d5cbaaa371918f12a8c29babc8cf81d3cdae07b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755254"
---
# New-AzureRmDataFactoryDataset

## Sammanfattning
Skapar en data uppsättning i data fabriken.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByFactoryName (standard)
```
New-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmDataFactoryDataset** skapar en data uppsättning i Azure Data Factory.
Om du anger ett namn för en data mängd som redan finns uppmanas du att bekräfta denna cmdlet innan den ersätter DataSet.
Om du anger parametern *Force* ersätter cmdleten det befintliga dataset utan bekräftelse.

Utför dessa operationer i följande ordning: 

- Skapa en data fabrik. 
- Skapa länkade tjänster. 
- Skapa data mängder. 
- Skapa en rörledning.

Om det redan finns en data uppsättning med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga data uppsättningen med den nya data uppsättningen.
Om du bekräftar att den befintliga data mängden skrivs över ersätts även data uppsättnings definitionen.

## BESKRIVS

### Exempel 1: skapa en data mängd
```
PS C:\>New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

Det här kommandot skapar en data mängd som heter DA_WikipediaClickEvents i data fabriken med namnet WikiADF.
Kommandot baserar data uppsättningen på informationen i filen DAWikipediaClickEvents.js.

### Exempel 2: Visa tillgänglighet för en ny data uppsättning
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

Det första kommandot skapar en data mängd som heter DA_WikipediaClickEvents, som i ett föregående exempel, och tilldelar sedan denna dataset till $Dataset variabel.

I det andra kommandot används standard punkt notation för att visa information om egenskapen Availability för data uppsättningen.

### Exempel 3: Visa plats för en ny data uppsättning
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

Det första kommandot skapar en data mängd som heter DA_WikipediaClickEvents, som i ett föregående exempel, och tilldelar sedan denna dataset till $Dataset variabel.

Det andra kommandot visar information om egenskapen location för data uppsättningen.

### Exempel 4: Visa verifierings uttryck för en ny data uppsättning
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

Det första kommandot skapar en data mängd som heter DA_WikipediaClickEvents, som i ett föregående exempel, och tilldelar sedan denna dataset till $Dataset variabel.

Det andra kommandot hämtar information om verifierings reglerna för data uppsättningen och skickar sedan vidare dem till Format-List cmdlet genom att använda pipeline-operatorn.
Som Windows PowerShell-cmdlet formaterar resultatet.
Om du vill ha mer information skriver du `Get-Help Format-List` .

## MALLPARAMETRAR

### -DataFactory
Anger ett **PSDataFactory** -objekt.
Den här cmdleten skapar en data mängd i data fabriken som den här parametern anger.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Anger namnet på en data fabrik.
Den här cmdleten skapar en data mängd i data fabriken som den här parametern anger.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -Fil
Anger den fullständiga sökvägen till den JavaScript-fil som innehåller en beskrivning av data mängden.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Anger att denna cmdlet ersätter en befintlig data uppsättning utan att du behöver bekräfta.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på den data uppsättning som ska skapas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en Azure-adressresurs.
Denna cmdlet skapar en data mängd i gruppen som den här parametern anger.

```yaml
Type: String
Parameter Sets: ByFactoryName
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
Type: SwitchParameter
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
Type: SwitchParameter
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

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft.WindowsAzure.Commands.Utilities.PSDataset

## ANMÄRKNINGAR
* Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer

## RELATERADE LÄNKAR

[Get-AzureRmDataFactoryDataset](./Get-AzureRmDataFactoryDataset.md)

[Remove-AzureRmDataFactoryDataset](./Remove-AzureRmDataFactoryDataset.md)


