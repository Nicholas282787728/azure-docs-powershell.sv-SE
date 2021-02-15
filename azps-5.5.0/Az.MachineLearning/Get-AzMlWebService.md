---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: be34a81e28f2a11ed604afe922694872fedb5f0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221606"
---
# Get-AzMlWebService

## SYNOPSIS
Hämtar sammanfattningsinformationen för en eller flera webbtjänster.

## SYNTAX

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Hämtar information om webbtjänstdefinitioner.
Beroende på vilka parametrar som överförs returnerar cmdleten definitionen för en viss webbtjänst, en samling definitioner för webbtjänsterna för en viss resursgrupp i den aktuella prenumerationen eller en samling definitioner för webbtjänsterna i den aktuella prenumerationen.

## EXEMPEL

### Exempel 1: Få information om specifik webbtjänst
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### Exempel 2: Hämta alla webbtjänstresurser i den aktuella prenumerationen
```
Get-AzMlWebService
```

### Exempel 3: Hämta alla webbtjänster i den aktuella prenumerationen och den givna resursgruppen
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

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

### -Name
Namnet på webbtjänsten som informationen hämtas för.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region
Namnet på regionen

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resursgruppen som informationen för webbtjänsten hämtas från.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## ANTECKNINGAR
Nyckelord: azure, azurerm, arm, resurs, hantering, chef, dator, maskininlärning, azureml

## RELATERADE LÄNKAR
