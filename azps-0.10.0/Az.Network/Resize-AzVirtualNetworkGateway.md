---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: bd42d7cec30b7d42dcb1cdb3657f6681bf2cb6b0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924302"
---
# Resize-AzVirtualNetworkGateway

## Sammanfattning
Ändrar storlek på en befintlig virtuell nätverksgateway.

## FRÅGESYNTAXEN

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Med cmdleten **ändra storlek-AzVirtualNetworkGateway** kan du ändra lagerhållnings enheten (SKU) för en virtuell nätverksgateway.
SKU: er avgör vilka funktioner en gateway har, inklusive sådant som genomflöde och det högsta antalet IP-tunnlar som tillåts.
Azure har stöd för grundläggande, standard, högpresterande, VpnGw1, VpnGw2 och VpnGw3 SKU: er (kallas ibland för små, medel stora och stora SKU: er).
Detaljerad information om funktionerna för varje SKU-typ finns i https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .

Kom ihåg att SKU: er skiljer sig från både priser och möjligheter.
Mer information finns i https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## BESKRIVS

### Exempel 1: ändra storleken på en virtuell nätverksgateway
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

Det här exemplet ändrar storleken på en virtuell nätverksgateway som heter ContosoVirtualGateway.

Det första kommandot skapar en objekt referens till ContosoVirtualGateway. Denna objekt referens lagras i en variabel som heter $Gateway.

Det andra kommandot använder sedan cmdleten för att **ändra storlek-AzVirtualNetworkGateway** för att ange egenskapen *GatewaySku* till Basic.

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

### -GatewaySku
Anger den nya typen av Gateway SKU.
De acceptabla värdena för den här parametern är:

- Basisk
- Standar
- Hög prestanda
- VpnGw1
- VpnGw2
- VpnGw3

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Anger en objekt referens till den virtuella nätverksgateway för att ändra storlek.
Du kan skapa denna objekt referens genom att använda Get-AzVirtualNetworkGateway och ange namnet på gatewayen.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

###  
Denna cmdlet accepterar pipeline-instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.

## VÄRDEN

###  
Denna cmdlet ändrar befintliga instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.

## ANMÄRKNINGAR
Du kan inte ändra storlek från grundläggande/standard-HighPerformance SKU till nya VpnGw1/VpnGw2/VpnGw3 SKU: er. Läs https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways mer om detta.

## RELATERADE LÄNKAR

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


