---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100253356"
---
# Get-AzDataFactorySlice

## SYNOPSIS
Hämtar datasegment för en datauppsättning i Azure Data Factory.

## SYNTAX

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

## BESKRIVNING
Cmdleten **Get-AzDataFactorySlice** hämtar datasegment för en datauppsättning i Azure Data Factory.
Ange en starttid och en sluttid för att definiera ett dataområde som ska visas.
Statusen för en datasegment är något av följande värden: 
- PendingExecution.
Databearbetningen har inte påbörjats. 
- InProgress.
Databearbetning pågår. 
- Klar.
Databearbetningen har slutförts.
Datasegmentet är klart för att använda beroende sektorer. 
- Misslyckades.
Det gick inte att köra den sektor som produceras. 
- Hoppa över.
Data Factory hoppar över bearbetningen av utsnittet. 
- Försök igen.
Data Factory försöker göra om körningen som ger sektorerna. 
- Timed Out. Databearbetningen har time out. 
- PendingValidation.
Datautsnittet väntar på verifiering innan den bearbetas. 
- Försök validera igen.
Data Factory försöker bekräfta utsnittet. 
- Verifieringen misslyckades.
Verifieringen av utsnittet misslyckades.
För var och en av sektorerna kan du se mer information om körningen som ger sektorerna med hjälp av cmdleten Get-AzDataFactoryRun.

## EXEMPEL

### Exempel 1: Hämta datasegment för en datauppsättning
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

Det här kommandot hämtar alla datasegment för datauppsättningen WikiAggregatedData i data factory med namnet WikiADF.
Kommandot får sektorer som skapas efter den tidpunkt som parametern StartDateTime anger.
I följande exempelkod anges tillgängligheten för den här datauppsättningen varje timme i JavaScript Object Notation-filen (JSON).
tillgänglighet: { period: "Hour", periodMultiplier: 1 } Vissa av resultaten är Redo och andra ärPendingExecution.
Färdiga sektorer har redan körts.
De väntande sektorerna väntar på att köras i slutet av varje timme i intervallet som cmdleten Set-AzDataFactoryPipelineActivePeriod anger.
I det här exemplet har både start- och slutperioder för rörledning och sektorer värdet en dag (24 timmar).

### Exempel 2

Hämtar datasegment för en datauppsättning i Azure Data Factory. (autogenererat)

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## PARAMETERS

### -DataFactory
Anger ett **PSDataFactory-objekt.**
Den här cmdleten hämtar sektorer som tillhör data factoryn som den här parametern anger.

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
Anger namnet på en data factory.
Den här cmdleten hämtar sektorer som tillhör data factoryn som den här parametern anger.

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
Anger namnet på den datauppsättning som den här cmdleten hämtar sektorer för.

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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
Anger slutet på en tidsperiod som ett **DateTime-objekt.**
Den här cmdleten produceras innan den tid den här parametern anges.
Om du vill ha mer information **om DateTime-objekt** skriver du `Get-Help Get-Date` .
*EndDateTime* måste anges i ISO8601-format som i följande exempel: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) Standarddesigner för tidszon är UTC.

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
Anger namnet på en Azure-resursgrupp.
Den här cmdleten hämtar sektorer som tillhör gruppen som parametern anger.

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
Anger början av en tidsperiod som ett **DateTime-objekt.**
Den här cmdleten får sektorer som produceras efter den tid som parametern anges.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## UTDATA

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## ANTECKNINGAR
* Nyckelord: azure, azurerm, arm, resource, management, manager, data, factories

## RELATERADE LÄNKAR

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


