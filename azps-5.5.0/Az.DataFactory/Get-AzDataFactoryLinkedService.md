---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5f59dfeeb024b4a81554a700bdcebc9d7f39e80a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230662"
---
# Get-AzDataFactoryLinkedService

## SYNOPSIS
Hämtar information om länkade tjänster i Azure Data Factory.

## SYNTAX

### ByFactoryName (standard)
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzDataFactoryLinkedService** hämtar information om länkade tjänster i Azure Data Factory.
Om du anger namnet på en länkad tjänst hämtar den här cmdleten information om den länkade tjänsten.
Om du inte anger ett namn hämtar den här cmdleten information om alla länkade tjänster i data factory.

## EXEMPEL

### Exempel 1: Få information om alla länkade tjänster
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

Det här kommandot hämtar information om alla länkade tjänster i data factory med namnet WikiADF och skickar sedan de länkade tjänsterna till cmdleten Format-List med hjälp av pipelineoperatorn.
Den cmdleten formaterar resultatet.
Om du vill ha mer information skriver du `Get-Help Format-List` .

### Exempel 2: Hämta information om en specifik länkad tjänst
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

Det här kommandot hämtar information om den länkade tjänsten HDILinkedService i data factory med namnet WikiADF.

### Exempel 3: Få information om en specifik länkad tjänst genom att ange parametern DataFactory
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

Det första kommandot använder cmdleten Get-AzDataFactory hämta data factory med namnet ContosoFactory och lagrar den sedan i $DataFactory variabeln.
Det andra kommandot hämtar information om den länkade tjänsten för data factoryen som lagras i $DataFactory och skickar sedan informationen till cmdleten Format-Table med hjälp av rörledningsoperatorn.
**Formatera tabell formaterar** resultatet som en datauppsättning med angivna egenskaper som kolumner i datauppsättningen.

## PARAMETERS

### -DataFactory
Anger ett **PSDataFactory-objekt.**
Den här cmdleten får länkade tjänster som tillhör data factoryn som parametern anger.

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
Den här cmdleten får länkade tjänster som tillhör data factoryn som parametern anger.

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

### -Name
Anger namnet på den länkade tjänsten som du vill hämta information om.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en Azure-resursgrupp.
Den här cmdleten får länkade tjänster som tillhör den grupp som parametern anger.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## UTDATA

### Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService

## ANTECKNINGAR
* Nyckelord: azure, azurerm, arm, resource, management, manager, data, factories

## RELATERADE LÄNKAR

[New-AzDataFactoryLinkedService](./New-AzDataFactoryLinkedService.md)

[Remove-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


