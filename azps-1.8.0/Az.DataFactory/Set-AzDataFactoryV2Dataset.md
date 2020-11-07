---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c3b15f198002ff11c936ad9e45a4dc87557329ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754347"
---
# Set-AzDataFactoryV2Dataset

## Sammanfattning
Skapar en data uppsättning i data fabriken.

## FRÅGESYNTAXEN

### ByFactoryName (standard)
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByResourceId
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Set-AzDataFactoryV2Dataset-cmdleten skapar en data uppsättning i Azure Data Factory.
Om du anger ett namn för en data mängd som redan finns uppmanas du att bekräfta denna cmdlet innan den ersätter DataSet.
Om du anger parametern Force ersätter cmdleten det befintliga dataset utan bekräftelse.
Utför de här operationerna i följande ordning:--skapa en data fabrik.
--Skapa länkade tjänster.
--Skapa data uppsättningar.
--Skapa en rörledning.
Om det redan finns en data uppsättning med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga data uppsättningen med den nya data uppsättningen.
Om du bekräftar att den befintliga data mängden skrivs över ersätts även data uppsättnings definitionen.

## BESKRIVS

### Exempel 1: skapa en data mängd
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

Det här kommandot skapar en data mängd som heter DA_WikipediaClickEvents i data fabriken med namnet WikiADF.
Kommandot baserar data uppsättningen på informationen i filen DAWikipediaClickEvents.js.

## MALLPARAMETRAR

### -DataFactoryName
Anger namnet på en data fabrik.
Den här cmdleten skapar en data mängd i data fabriken som den här parametern anger.

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

### -DefinitionFile
Sökvägen till JSON-filen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Kör cmdleten utan att behöva bekräfta.

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

### -Namn
Anger namnet på den data uppsättning som ska skapas.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en Azure-adressresurs.
Denna cmdlet skapar en data mängd i gruppen som den här parametern anger.

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

### -ResourceId
ID för Azure-resursen.

```yaml
Type: System.String
Parameter Sets: ByResourceId
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs men inte kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset

## ANMÄRKNINGAR
Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer

## RELATERADE LÄNKAR

[Get-AzDataFactoryV2Dataset]()

[Remove-AzDataFactoryV2Dataset]()
