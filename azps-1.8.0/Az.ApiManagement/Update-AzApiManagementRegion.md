---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 3f9c88177d3f791acdd0be5c81eec2fb5bc6911c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400713"
---
# Update-AzApiManagementRegion

## SYNOPSIS
Uppdaterar befintlig distributionsregion i PsApiManagement-instansen.

## SYNTAX

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Update-AzApiManagementRegion** uppdaterar en befintlig instans av typen **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** i en samling **AdditionalRegions-objekt** för en a provided-instans av typen **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**
Den här cmdleten distribuerar ingenting men uppdaterar en instans av **PsApiManagement** i minnet.
Om du vill uppdatera en distribution av en API-hantering använder du den modifierade **PsApiManagementInstance** till cmdleten Set-AzApiManagement.

## EXEMPEL

### Exempel 1: Ökar kapaciteten för ytterligare region i en PsApiManagement-instans
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium

# Set the ApiManagement service and Enable Msi idenity on the service
PS C:\>$updatedService = Set-AzApiManagement -InputObject $apimService -PassThru
```

Det här kommandot får API Management Premium-SKU-tjänsten, med regioner i södra centrala USA och centrala USA. Därefter ökar kapaciteten i området i centrala USA till 2 med hjälp av **Update-AzApiManagementRegion.** Nästa cmdlet Set-AzApiManagement konfigurationsändringen för tjänsten Api Management.

## PARAMETERS

### -ApiManagement
Anger **PsApiManagement-instansen** som en befintlig distributionsregion ska uppdateras i.

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

### -Capacity
Anger det nya SKU-kapacitetsvärdet för distributionsområdet.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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
Anger platsen för distributionsområdet som ska uppdateras.
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

### -SKU
Anger det nya nivåvärdet för distributionsområdet.
Giltiga värden är:
- Utvecklare
- Standard
- Premium

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Anger en konfiguration av ett virtuellt nätverk för distributionsområdet.
Passerar $null tar bort virtuell nätverkskonfiguration för regionen.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

### Microsoft.Azure.Commands.ApiManagement.Models.PsapiManagementSku

### System.Int32

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork

## UTDATA

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzapiManagementRegion](./Add-AzApiManagementRegion.md)

[Remove-AzapiManagementRegion](./Remove-AzApiManagementRegion.md)

[Set-AzapiManagement](./Set-AzApiManagement.md)
