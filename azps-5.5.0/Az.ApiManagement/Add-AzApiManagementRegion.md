---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221847"
---
# Add-AzApiManagementRegion

## SYNOPSIS
Lägger till nya distributionsområden i en PsApiManagement-instans.

## SYNTAX

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Add-AzApiManagementRegion** lägger till en ny instans av typen **PsApiManagementRegion** i samlingen **AdditionalRegions** för den angivna instansen av typen **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**
Den här cmdleten distribuerar ingenting för sig själv, men uppdaterar instansen av **PsApiManagement** i minnet.
Om du vill uppdatera en distribution av ett API Management-pass den modifierade **PsApiManagement-instansen** till Set-AzApiManagement.

## EXEMPEL

### Exempel 1: Lägga till nya distributionsområden i en PsApiManagement-instans
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

Det här kommandot lägger till två premium-SKU-enheter och regionen Öst-USA till **PsApiManagement-instansen.**

### Exempel 2: Lägga till nya distributionsområden i en PsApiManagement-instans och sedan uppdatera distributionen
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

Det här kommandot får **ett PsApiManagement-objekt,** lägger till två premium-SKU-enheter för regionen Östra USA och uppdaterar sedan distributionen.

## PARAMETERS

### -ApiManagement
Anger **PsApiManagement-instansen** som denna cmdlet lägger till ytterligare distributionsområden i.

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

### -Kapacitet
Anger SKU-kapaciteten för distributionsområdet.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Plats
Anger platsen för den nya distributionsområdet mellan den region som stöds för api-hanteringstjänsten.
För att få giltiga platser använder du cmdleten Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | där {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object platser

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

### -SKU
Anger nivån för distributionsområdet.
Giltiga värden är: 
- Utvecklare
- Standard
- Premium

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
Anger en konfiguration av virtuellt nätverk.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
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

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## UTDATA

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## ANTECKNINGAR
* Cmdleten skriver den uppdaterade **PsApiManagement-instansen** till pipeline.

## RELATERADE LÄNKAR

[Remove-AzapiManagementRegion](./Remove-AzApiManagementRegion.md)

[Update-AzapiManagementRegion](./Update-AzApiManagementRegion.md)

[Set-AzapiManagement](./Set-AzApiManagement.md)


