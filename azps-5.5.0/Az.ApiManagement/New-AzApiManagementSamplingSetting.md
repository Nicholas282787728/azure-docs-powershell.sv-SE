---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 2658e1af1865668adfa865cfc0bc7f09c7340251
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100254164"
---
# New-AzApiManagementSamplingSetting

## SYNOPSIS
Skapa en ny samplingsinställning för Diagnostik

## SYNTAX

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzApiManagementSamplingSetting** skapar en ny samplingsinställning för Diagnostik

## EXEMPEL

### Exempel 1: Skapa en enkel samplingsinställning
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

Skapar en samplingsinställning `Fixed` av typ med loggning för 100 % av förfrågningar/svar

### Exempel 2

Skapa en ny samplingsinställning för Diagnostik. (autogenererat)

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementSamplingSetting -SamplingPercentage 100 -SamplingType fixed
```

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -SamplingPercentage
Samplingshastighet för sampling med fast hastighet. Den här parametern är valfri.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SamplingType
Typen av sampling.
Den här parametern är valfri.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementsamplingSetting

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzapiManagementDiagnostic](./Get-AzApiManagementDiagnostic.md)

[Remove-AzapiManagementDiagnostic](./Remove-AzApiManagementDiagnostic.md)

[Set-AzapiManagementDiagnostic](./Set-AzApiManagementDiagnostic.md)

[New-AzapiManagementSamplingSetting](./New-AzApiManagementHttpMessageDiagnostic.md)
