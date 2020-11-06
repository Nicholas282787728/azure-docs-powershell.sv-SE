---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: ed26538e54cef189837bd36bf9e6f561df3541f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574056"
---
# Update-AzureRmApiManagementRegion

## Sammanfattning
Uppdaterar det befintliga distributions området i PsApiManagement-instansen.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Update-AzureRmApiManagementRegion** uppdaterar en befintlig instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementRegion** i en samling **AdditionalRegions** -objekt av en angiven instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.
Denna cmdlet distribuerar inte något men uppdaterar inte en instans av **PsApiManagement** i minnet.
Om du vill uppdatera en distribution av en API-hantering använder du den ändrade **PsApiManagementInstance** till cmdleten Update-AzureRmApiManagementDeployment.

## BESKRIVS

## MALLPARAMETRAR

### -ApiManagement
Anger den **PsApiManagement** -instans som du vill uppdatera ett befintligt distributions område i.

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
Anger det nya värdet för SKU-kapacitet för distributions området.

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

### -Plats
Anger platsen för det distributions område som ska uppdateras.
Anger platsen för det nya distributions området bland de regioner som stöds för API-hanterings tjänsten.
För att få giltiga platser, Använd cmdleten Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser

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
Anger det nya nivå svärdet för distributions området.
Giltiga värden är:
- Utvecklar
- Standar
- Beta

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
Anger en virtuell nätverks konfiguration för distributions området.
Om du överför $null tas nätverkets konfiguration för området bort.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement
Parametrar: ApiManagement (ByValue)

### System. String

### Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSku

### System. Int32

### Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVirtualNetwork

## VÄRDEN

### Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[Remove-AzureRmApiManagementRegion](./Remove-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementDeployment](./Update-AzureRmApiManagementDeployment.md)
