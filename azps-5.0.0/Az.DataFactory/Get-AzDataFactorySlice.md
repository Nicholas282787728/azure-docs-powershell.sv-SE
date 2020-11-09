---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321043"
---
# Get-AzDataFactorySlice

## Sammanfattning
Hämtar data sektorer för en data uppsättning i Azure Data Factory.

## FRÅGESYNTAXEN

### ByFactoryName (standard)
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzDataFactorySlice** hämtar data segment för en data uppsättning i Azure Data Factory.
Ange en start tid och en slut tid för att definiera ett data område som ska visas.
Statusen för en data sektor är något av följande värden: 
- PendingExecution.
Data behandling har inte påbörjats. 
- Inaktive.
Data bearbetning pågår. 
- Förbereder.
Data bearbetning är klar.
Data sektorn är redo för att du ska kunna använda det. 
- Startade.
Det gick inte att köra sektorn. 
- Vidare.
Data fabriken hoppar över bearbetning av sektorn. 
- Försök igen.
Data fabriken försöker igen med den körning som tillverkar segmentet. 
- Tids gränsen uppnåddes. Tids gränsen för data bearbetning har uppnåtts. 
- PendingValidation.
Data sektorn väntar på verifiering innan den behandlas. 
- Gör om verifieringen.
Data fabriken försöker att verifiera segmentet igen. 
- Valideringen misslyckades.
Det gick inte att verifiera sektorn.
För var och en av sektorerna kan du Visa mer information om den körning som producerar segmentet med hjälp av Get-AzDataFactoryRun cmdlet.

## BESKRIVS

### Exempel 1: Hämta data sektorer för en data mängd
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

Det här kommandot får alla data sektorer för den data uppsättning som heter WikiAggregatedData i data fabriken med namnet WikiADF.
Kommandot får de sektorer som uppstår efter den tid som StartDateTime-parametern anger.
I följande exempel kod anges tillgänglighet för denna dataset varje timme i JSON-filen (JavaScript Object Notation).
tillgänglighet: {period: "timme", periodMultiplier: 1} vissa av resultaten är klara och andra är PendingExecution.
Klara sektorer har redan körts.
De väntande sektorerna väntar på att de ska köras vid slutet av varje timme i det intervall som Set-AzDataFactoryPipelineActivePeriod-cmdleten anger.
I det här exemplet har både start-och slut perioderna för pipeline och segmentet ett värde om 1 dag (24 timmar).

### Exempel 2

Hämtar data sektorer för en data uppsättning i Azure Data Factory. (automatiskt genererat)

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## MALLPARAMETRAR

### -DataFactory
Anger ett **PSDataFactory** -objekt.
Denna cmdlet hämtar sektorer som tillhör data fabriken som den här parametern anger.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
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
Denna cmdlet hämtar sektorer som tillhör data fabriken som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatasetName
Anger namnet på den dataset för vilken denna cmdlet hämtar sektorer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -EndDateTime
Anger slutet på en tids period som ett **datetime** -objekt.
Denna cmdlet tar fram sektorer som produceras före den tid som parametern anger.
Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .
*EndDateTime* måste anges i formatet iso8601 som i följande exempel: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time).

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en Azure-adressresurs.
Denna cmdlet hämtar sektorer som tillhör den grupp som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDateTime
Anger början av en tids period som ett **datetime** -objekt.
Denna cmdlet tar emot sektorer efter den tid som den här parametern anger.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## VÄRDEN

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## ANMÄRKNINGAR
* Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer

## RELATERADE LÄNKAR

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


