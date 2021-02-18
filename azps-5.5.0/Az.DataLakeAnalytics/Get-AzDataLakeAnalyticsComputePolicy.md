---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100253309"
---
# Get-AzDataLakeAnalyticsComputePolicy

## SYNOPSIS
Hämtar en beräkningsprincip eller lista över beräkningsprinciper för Data Lake Analytics.

## SYNTAX

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Get-AzDataLakeAnalyticsComputePolicy** får en angiven beräkningsprincip för Azure Data Lake Analytics eller en lista med principer.

## EXEMPEL

### Exempel 1: Hämta en specifik beräkningsprincip
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

Det här kommandot får den angivna beräkningsprincipen med namnet "myPolicy" i kontot contosoadla.

### Exempel 2: Visa en lista över alla beräkningsprinciper i kontot
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

Det här kommandot får en lista över alla beräkningsprinciper i kontot "contosoadla"

## PARAMETERS

### -Konto
Namnet på kontot som du vill beräkna policyn eller principerna från.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
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
Namnet på beräkningsprincipen som ska beräknas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Namn på resursgrupp som kontot finns i.
Valfritt och försöker identifiera om det inte anges.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy

## ANTECKNINGAR

## RELATERADE LÄNKAR
