---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 0a8a5c4084813bac74ea907575d2bd26c3d8c5f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584060"
---
# Resize-AzureRmVirtualNetworkGateway

## Sammanfattning
Ändrar storlek på en befintlig virtuell nätverksgateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Med cmdleten **ändra storlek-AzureRmVirtualNetworkGateway** kan du ändra lagerhållnings enheten (SKU) för en virtuell nätverksgateway.
SKU: er avgör vilka funktioner en gateway har, inklusive sådant som genomflöde och det högsta antalet IP-tunnlar som tillåts.
Azure har stöd för grundläggande, standard, högpresterande, VpnGw1, VpnGw2, VpnGw3, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ,-SKU: er (kallas ibland för små, medel stora och stora SKU: er).
Detaljerad information om funktionerna för varje SKU-typ finns i https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .
Kom ihåg att SKU: er skiljer sig från både priser och möjligheter.
Mer information finns i https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## BESKRIVS

### Exempel 1: ändra storleken på en virtuell nätverksgateway
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

Det här exemplet ändrar storleken på en virtuell nätverksgateway som heter ContosoVirtualGateway.
Det första kommandot skapar en objekt referens till ContosoVirtualGateway. Denna objekt referens lagras i en variabel som heter $Gateway.
Det andra kommandot använder sedan cmdleten för att **ändra storlek-AzureRmVirtualNetworkGateway** för att ange egenskapen *GatewaySku* till Basic.

## MALLPARAMETRAR

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

### -GatewaySku
Anger den nya typen av Gateway SKU.
De acceptabla värdena för den här parametern är:
- Basisk
- Standar
- Hög prestanda
- VpnGw1
- VpnGw2
- VpnGw3
- VpnGw1AZ 
- VpnGw2AZ 
- VpnGw3AZ 
- ErGw1AZ 
- ErGw2AZ 
- ErGw3AZ 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Anger en objekt referens till den virtuella nätverksgateway för att ändra storlek.
Du kan skapa denna objekt referens genom att använda Get-AzureRmVirtualNetworkGateway och ange namnet på gatewayen.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
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

### Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway
Parametrar: VirtualNetworkGateway (ByValue)

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway

## ANMÄRKNINGAR
Du kan inte ändra storlek från grundläggande/standard-HighPerformance SKU till nya VpnGw1/VpnGw2/VpnGw3 SKU: er. Det går ännu inte att ändra storlek från/till VpnGw1AZ/VpnGw2AZ/VpnGw3AZ eller ErGw1AZ/ErGw2AZ/ErGw3AZ. Storleks ändring tillåts bara inom SKU ' Series ' VpnGw1AZ kan ändras till/från VpnGw2AZ/VpnGw3AZ och ErGw1AZ kan anpassas till/från ErGw2AZ/ErGw3AZ. Läs https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways mer om detta.

## RELATERADE LÄNKAR

[Get-AzureRmVpnClientPackage](./Get-AzureRmVpnClientPackage.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


