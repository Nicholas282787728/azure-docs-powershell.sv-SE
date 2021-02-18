---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100254136"
---
# Remove-AzApiManagementRegion

## SYNOPSIS
Tar bort ett befintligt distributionsområde från PsApiManagement-instansen.

## SYNTAX

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzApiManagementRegion** tar bort en instans av typen **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** från en samling **additionalregions** av angivna instansen av typen **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**
Den här cmdleten ändrar inte distributionen för sig men uppdaterar instansen av **PsApiManagement-minnet.**
Om du vill uppdatera en distribution av en API-hantering skickar du den modifierade **PsApiManagementInstance** **till Set-AzApiManagement.**

## EXEMPEL

### Exempel 1: Ta bort en region från en PsApiManagement-instans
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Med det här kommandot tas regionen Östra USA bort från **PsApiManagement-instansen.**

### Exempel 2: Ta bort en region från en PsApiManagement-instans med en serie kommandon
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

Det första kommandot hämtar en instans av **PsApiManagement** från resursgruppen Contoso med namnet ContosoApi.
Det slutliga kommandot tar sedan bort regionen Öst, USA från den instansen, och uppdaterar sedan distributionen.

## PARAMETERS

### -ApiManagement
Anger **PsApiManagement-instansen** som denna cmdlet tar bort den ytterligare distributionsregion från.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile

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

### -Plats
Anger platsen för den region som cmdleten tar bort.
Anger platsen för den nya distributionsområdet i den region som stöds för api-hanteringstjänsten.
För att få giltiga platser använder du cmdleten Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | där {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object platser

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

## UTDATA

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzapiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzapiManagementRegion](./Update-AzApiManagementRegion.md)


