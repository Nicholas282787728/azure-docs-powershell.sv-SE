---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091958"
---
# New-AzMlWebService

## Sammanfattning
Skapar en ny webb tjänst.

## FRÅGESYNTAXEN

### CreateFromFile
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromInstance
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Skapar en Azure Machine Learning-webbtjänst i en befintlig resurs grupp.
Om en webb tjänst med samma namn finns i resurs gruppen fungerar samtalet som en uppdaterings åtgärd och den befintliga webb tjänsten skrivs över.

## BESKRIVS

### Exempel 1: skapa en ny tjänst från en JSON-filbaserad definition
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Skapar en ny Azure Machine Learning-webbtjänst med namnet "mywebservicename" i gruppen "myresourcegroup" och det centrala amerikanska området, baserat på definitionen i den refererade JSON-filen.

### Exempel 2: skapa en ny tjänst från en objekt instans
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Du kan få en instans av en webb tjänst objekt att anpassa innan du publicerar den som en resurs genom att använda Import-AzMlWebService cmdlet.

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

### -DefinitionFile
Anger sökvägen till filen som innehåller JSON-formatet för webb tjänsten.
Du hittar den senaste specifikationen för webb tjänst definitionen i Swagger-specifikationen under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Fråga inte efter bekräftelse.

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

### -Plats
Regionen för webb tjänsten.
Ange ett Azure Data Center-område, till exempel "västra USA" eller "Sydostasien".
Du kan använda en webb tjänst i vilken region som helst som stöder resurser av den typen.
Webb tjänsten måste inte vara i samma region som din Azure-prenumeration eller samma region som resurs gruppen.
Resurs grupper kan innehålla webb tjänster från olika regioner.
För att avgöra vilka regioner som stöder varje resurs typ använder du Get-AzResourceProvider med ProviderNamespace parameter-cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namnet på webb tjänsten.
Namnet måste vara unikt i resurs gruppen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewWebServiceDefinition
Definitionen för den nya webb tjänsten som innehåller alla egenskaper som utgör tjänsten.
Den här parametern är obligatorisk och representerar en instans av klassen Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.
Du hittar den senaste specifikationen för webb tjänst definitionen i Swagger-specifikationen under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs gruppen där webb tjänsten ska placeras.
Ange ett Azure Data Center-område, till exempel "västra USA" eller "Sydostasien".
Du kan använda en webb tjänst i vilken region som helst som stöder resurser av den typen.
Webb tjänsten måste inte vara i samma region som din Azure-prenumeration eller samma region som resurs gruppen.
Resurs grupper kan innehålla webb tjänster från olika regioner.
För att avgöra vilka regioner som stöder varje resurs typ använder du Get-AzResourceProvider med ProviderNamespace parameter-cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService

## VÄRDEN

### Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService

## ANMÄRKNINGAR
Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml

## RELATERADE LÄNKAR
