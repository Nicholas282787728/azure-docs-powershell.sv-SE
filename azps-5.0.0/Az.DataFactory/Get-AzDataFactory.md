---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 11aaaa3bb17a35583655f231123b7f6e9dea9ab4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321080"
---
# Get-AzDataFactory

## Sammanfattning
Hämtar information om data fabriker.

## FRÅGESYNTAXEN

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzDataFactory** hämtar information om data fabrikerna i en Azure-resurs grupp.
Om du anger namnet på en data fabrik får denna cmdlet information om den data fabriken.
Om du inte anger ett namn hämtas den här cmdleten information om alla data fabrikerna i en Azure-resurs grupp.

## BESKRIVS

### Exempel 1: Hämta alla data fabriker
```
PS C:\>Get-AzDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

Det här kommandot visar information om alla data faktorer i Azure-abonnemanget.

### Exempel 2: skaffa en specifik data fabrik
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

Det här kommandot visar information om data fabriken med namnet WikiADF i prenumerationen för resurs gruppen med namnet ADF och sedan lagras den i $DataFactory variabel.
Ange parametern *DataFactory* i efterföljande cmdlets för att använda data fabriken som lagras i $DataFactory.

## MALLPARAMETRAR

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

### -Namn
Anger namnet på data fabriken för att få information.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en Azure-adressresurs.
Denna cmdlet hämtar information om data fabriker som tillhör gruppen som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## ANMÄRKNINGAR
* Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer

## RELATERADE LÄNKAR

[New-AzDataFactory](./New-AzDataFactory.md)

[Remove-AzDataFactory](./Remove-AzDataFactory.md)


