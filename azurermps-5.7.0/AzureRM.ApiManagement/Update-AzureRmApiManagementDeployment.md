---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: 62400acbb9fb70f05772bd9749e39e3d7d62cc62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577275"
---
# Update-AzureRmApiManagementDeployment

## Sammanfattning
Uppdaterar distribution av en API-hanterings tjänst.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### UpdateSpecificService (standard)
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### UpdateFromPsApiManagementInstance
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Update-AzureRmApiManagementDeployment** uppdaterar nuvarande distributioner av en API-hanterings tjänst.

## BESKRIVS

### Exempel 1: uppdatera en distribution av en ApiManagement-instans
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

Det här kommandot uppdaterar distributionen av en API-hanterings instans till en tre enhets kapacitets standard.

### Exempel 2: skaffa en ApiManagement-förekomst och skala den
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

Det här exemplet får en API-hanterings instans, ändrar den till fem premie enheter och lägger sedan till ytterligare tre enheter till Premium-området.

### Exempel 3: uppdaterings distribution (externt virtuellt nätverk)
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

Det här kommandot uppdaterar en befintlig API-distribution och ansluter till en extern *VpnType*.

### Exempel 4: uppdaterings distribution (internt virtuellt nätverk)
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

Det här kommandot uppdaterar en befintlig API-distribution och ansluter till en intern *VpnType*.

## MALLPARAMETRAR

### -AdditionalRegions
Anger ytterligare distributions områden för Azure API Management.

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApiManagement
Anger den **PsApiManagement** -instans som du vill hämta distributions konfigurationen från.
Använd den här parametern om instansen redan har alla nödvändiga ändringar.

```yaml
Type: PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Kapacitet
Anger SKU-kapaciteten för huvud området för distribution av Azure API-hantering.

```yaml
Type: Int32
Parameter Sets: UpdateSpecificService
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger platsen för distributions området Master API Management.

För att få giltiga platser, Använd cmdleten Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på API-hanteringen som uppdateras med den här cmdleten.

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Returnerar ett objekt som representerar det objekt som du arbetar med.
Denna cmdlet genererar som standard inga utdata.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som API-hantering finns under.

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Anger nivån för distributions området för Master API-hantering för Azure.

De acceptabla värdena för den här parametern är:

- Utvecklar
- Standar
- Beta

```yaml
Type: PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Anger virtuell nätverks konfiguration för distributions regionen Master API Management.

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnType
Anger den virtuella nätverks typen för API-hanterings distributionen.
De acceptabla värdena för den här parametern är:

- Ingen.
API-hanterings distributionen är inte en del av något virtuellt nätverk.
Det här är standardvärdet. 
- 5,25.
Distributionen av API-hanteringen har en extern vänd virtuell adress. 
- Intern.
Distributionen av API-hanteringen har en vänd intranäts adress.

```yaml
Type: PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### PsApiManagement
Parametern ' ApiManagement ' godkänner värdet av typen ' PsApiManagement ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmApiManagement](./Get-AzureRmApiManagement.md)


