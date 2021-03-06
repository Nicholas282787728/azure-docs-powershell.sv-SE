---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 7503d775b7241bbb1be6196db153e41587c0e736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758113"
---
# Get-AzureRmDataFactoryLinkedService

## Sammanfattning
Hämtar information om de länkade tjänsterna i Azure Data Factory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByFactoryName (standard)
```
Get-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmDataFactoryLinkedService** hämtar information om länkade tjänster i Azure Data Factory.
Om du anger namnet på en länkad tjänst får denna cmdlet information om den länkade tjänsten.
Om du inte anger ett namn hämtas den här cmdleten information om alla länkade tjänster i data fabriken.

## BESKRIVS

### Exempel 1: få information om alla länkade tjänster
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

Det här kommandot får information om alla länkade tjänster i data fabriken med namnet WikiADF och skickar sedan de länkade tjänsterna till Format-List cmdlet med hjälp av pipeline-operatorn.
Denna cmdlet formaterar resultaten.
Om du vill ha mer information skriver du `Get-Help Format-List` .

### Exempel 2: Hämta information om en specifik länkad tjänst
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

Med det här kommandot får du information om den länkade tjänsten som heter HDILinkedService i data fabriken med namnet WikiADF.

### Exempel 3: Hämta information om en specifik länkad tjänst genom att ange parametern DataFactory
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzureRmDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

Det första kommandot använder cmdleten Get-AzureRmDataFactory för att hämta data fabriken med namnet ContosoFactory och lagrar den sedan i $DataFactory variabel.

Det andra kommandot får information om den länkade tjänsten för data fabriken som lagras i $DataFactory och skickar sedan informationen till Format-Table-cmdleten med hjälp av pipeline-operatorn.
**Format-tabell** formaterar utdata som en data uppsättning med de angivna egenskaperna som data mängds kolumner.

## MALLPARAMETRAR

### -DataFactory
Anger ett **PSDataFactory** -objekt.
Denna cmdlet tar emot länkade tjänster som tillhör data fabriken som den här parametern anger.

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
Denna cmdlet tar emot länkade tjänster som tillhör data fabriken som den här parametern anger.

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

### -Namn
Anger namnet på den länkade tjänsten som ska få information om.

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
Anger namnet på en Azure-adressresurs.
Denna cmdlet tar emot länkade tjänster som tillhör gruppen som den här parametern anger.

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

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### System. Collections. Generic. list ' 1 [[Microsoft. WindowsAzure. commands. Utilities. PSLinkedService, Microsoft. WindowsAzure. commands. Utilities, version = 0.8.2.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]] Microsoft. WindowsAzure. kommandon. Utilities. PSLinkedService

## ANMÄRKNINGAR
* Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer

## RELATERADE LÄNKAR

[New-AzureRmDataFactoryLinkedService](./New-AzureRmDataFactoryLinkedService.md)

[Remove-AzureRmDataFactoryLinkedService](./Remove-AzureRmDataFactoryLinkedService.md)


