---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 0c05800bc72af7b6158b2adeaccc92255d7ae4af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575603"
---
# Set-AzureRmVirtualNetworkGatewayDefaultSite

## Sammanfattning
Anger standard platsen för en virtuell nätverksgateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmVirtualNetworkGatewayDefaultSite** tilldelar en standard plats för tvingande tunnel till en virtuell nätverksgateway.
Med tvingande tunnlar kan du omdirigera Internet-bundna trafik från virtuella Azure-datorer till det lokala nätverket. Detta gör att du kan kontrol lera och granska trafiken innan den släpps.
Framtvingad tunnel trafik utförs med en VPN-tunnel (Virtual Private Network). Denna tunnel kräver en standard webbplats, en lokal gateway där all Azure Internet-bunden trafik omdirigeras.
**Set-AzureRmVirtualNetworkGatewayDefaultSite** ger dig ett sätt att ändra standard webbplatsen som är tilldelad en gateway.

## BESKRIVS

### Exempel 1: tilldela en standard webbplats till en virtuell nätverksgateway
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

I det här exemplet tilldelas en standard webbplats till en virtuell nätverksgateway med namnet ContosoVirtualGateway.

Det första kommandot skapar en objekt referens till en lokal gateway som heter ContosoLocalGateway.
Den här objekt referensen som lagras i variabeln som heter $LocalGateway representerar den gateway som ska konfigureras som standard webbplats

.
Det andra kommandot skapar sedan en objekt referens till den virtuella Nätverksgatewayen och lagrar resultatet i variabeln som heter $VirtualGateway.

I det tredje kommandot används cmdleten **set-AzureRmVirtualNetworkGatewayDefaultSite** för att koppla standard platsen till ContosoVirtualGateway.

## MALLPARAMETRAR

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

### -GatewayDefaultSite
Anger en objekt referens till den lokala Nätverksgatewayen som ska tilldelas som standard webbplats för det angivna virtuella nätverket.
Du kan använda Get-AzureRmLocalNetworkGateway cmdlet för att skapa en objekt referens till en lokal gateway.

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Anger en objekt referens till den virtuella Nätverksgatewayen där standard webbplatsen tilldelas.
Du kan skapa en objekt referens till en virtuell nätverksgateway genom att använda **Get-AzureRmVirtualNetworkGateway** och ange namnet på gatewayen.

Variabeln $VirtualGateway kan sedan användas som parameter värde för parametern *VirtualNetworkGateway* :

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

###  
Denna cmdlet accepterar pipeline-instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.

## VÄRDEN

###  
Denna cmdlet ändrar befintliga instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmLocalNetworkGateway](./Get-AzureRmLocalNetworkGateway.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Remove-AzureRmVirtualNetworkGatewayDefaultSite](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


