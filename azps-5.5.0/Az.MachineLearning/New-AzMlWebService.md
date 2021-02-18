---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224366"
---
# New-AzMlWebService

## SYNOPSIS
Skapar en ny webbtjänst.

## SYNTAX

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

## BESKRIVNING
Skapar en Azure Machine Learning-webbtjänst i en befintlig resursgrupp.
Om det finns en webbtjänst med samma namn i resursgruppen fungerar samtalet som en uppdateringsåtgärd och den befintliga webbtjänsten skrivs över.

## EXEMPEL

### Exempel 1: Skapa en ny tjänst från en Json-filbaserad definition
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Skapar en ny Azure Machine Learning-webbtjänst med namnet "mywebservicename" i gruppen "myresourcegroup" och regionen Syd central i USA, baserat på definitionen som finns i den refererade json-filen.

### Exempel 2: Skapa en ny tjänst från en objektinstans
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Du kan hämta en webbtjänstobjektsinstans som du kan anpassa innan du publicerar som en resurs med hjälp Import-AzMlWebService-cmdleten.

## PARAMETERS

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

### -DefinitionFile
Anger sökvägen till filen som innehåller JSON-formatdefinitionen för webbtjänsten.
Du hittar den senaste specifikationen för webbtjänstdefinitionen i swaggerspecifikationen https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning under.

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
Be inte om bekräftelse.

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
Webbtjänstens region.
Ange en Azure-datacenterregion, till exempel "Västra USA" eller "Sydostasien".
Du kan placera en webbtjänst i alla regioner som har stöd för resurser av den typen.
Webbtjänsten måste inte finnas i samma region som din Azure-prenumeration eller samma region som resursgruppen.
Resursgrupper kan innehålla webbtjänster från olika regioner.
Om du vill avgöra vilka regioner som stöder varje resurstyp använder du Get-AzResourceProvider med providernamespace-parameter cmdleten.

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

### -Name
Namnet på webbtjänsten.
Namnet måste vara unikt i resursgruppen.

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
Definitionen för den nya webbtjänsten, som innehåller alla egenskaper som utgör tjänsten.
Den här parametern är obligatorisk och representerar en instans av klassen Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.
Du hittar den senaste specifikationen för webbtjänstdefinitionen i swaggerspecifikationen https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json under.

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
Resursgruppen där webbtjänsten ska placeras.
Ange en Azure-datacenterregion, till exempel "Västra USA" eller "Sydostasien".
Du kan placera en webbtjänst i alla regioner som har stöd för resurser av den typen.
Webbtjänsten måste inte finnas i samma region som din Azure-prenumeration eller samma region som resursgruppen.
Resursgrupper kan innehålla webbtjänster från olika regioner.
Om du vill avgöra vilka regioner som stöder varje resurstyp använder du Get-AzResourceProvider med providernamespace-parameter cmdleten.

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
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs.
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## UTDATA

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## ANTECKNINGAR
Nyckelord: azure, azurerm, arm, resurs, hantering, chef, dator, maskininlärning, azureml

## RELATERADE LÄNKAR
