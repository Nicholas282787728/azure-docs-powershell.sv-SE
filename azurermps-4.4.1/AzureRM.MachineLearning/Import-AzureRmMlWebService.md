---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: d85767623d88c9fd7d0a00ea98e575953132d3f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758050"
---
# Import-AzureRmMlWebService

## Sammanfattning
Importerar ett JSON-objekt till en webb tjänst definition.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Importera från JSON-fil.
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Importera från JSON-sträng.
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Import-AzureRmMlWebService cmdlet importeras, anges antingen direkt eller i en refererad fil, och skapar ett webb tjänst definitions objekt som kan skickas till New-AzureRmMlWebService cmdlet.

## BESKRIVS

### --------------------------Exempel 1: importera från sträng--------------------------
@ {paragraf = PS C: \\ \> }





```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### --------------------------Exempel 2: importera från sökväg--------------------------
@ {paragraf = PS C: \\ \> }





```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## MALLPARAMETRAR

### -InputFile
Sökvägen till filen som innehåller webb tjänst definitionen som ska importeras.

```yaml
Type: System.String
Parameter Sets: Import from JSON file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JsonString
Den JSON-formaterade sträng som innehåller webb tjänst definitionen som ska importeras.

```yaml
Type: System.String
Parameter Sets: Import from JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService

## ANMÄRKNINGAR
Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml

## RELATERADE LÄNKAR

