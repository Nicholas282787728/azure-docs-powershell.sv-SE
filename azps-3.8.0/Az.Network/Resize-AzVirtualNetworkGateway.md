---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 31ec0453b0ce64c27d1bb37d4bf6c0f100a8c760
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411763"
---
# Resize-AzVirtualNetworkGateway

## SYNOPSIS
Ändrar storlek på en befintlig virtuell nätverksgateway.

## SYNTAX

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Med cmdleten **Resize-AzVirtualNetworkGateway** kan du ändra lagerenhet (SKU) för en virtuell nätverksgateway.
SKU:er avgör en gateways funktioner, till exempel dataflöde och maximalt antal IP-tunnlar som är tillåtna.
Azure stöder Grundläggande, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKU:er (kallas ibland för små, medelstora och stora SKU:er).
Detaljerad information om funktionerna för varje SKU-typ finns https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ i.
Kom ihåg att SKU:er skiljer sig vad gäller priser och funktioner.
Mer information finns i https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## EXEMPEL

### Exempel 1: Ändra storleken på en virtuell nätverksgateway
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

I det här exemplet ändras storleken på en virtuell nätverksgateway med namnet ContosoVirtualGateway.
Det första kommandot skapar en objektreferens till ContosoVirtualGateway. objektreferensen lagras i en variabel med namnet $Gateway.
Det andra kommandot använder sedan **cmdleten Resize-AzVirtualNetworkGateway** till att ange *egenskapen GatewaySku* till Basic.

## PARAMETERS

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

### -GatewaySku
Anger den nya typen av gateway-SKU.
De godtagbara värdena för den här parametern är:
- Grundläggande
- Standard
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
Anger en objektreferens till den virtuella nätverksgateway som ska ändras.
Du kan skapa den här objektreferensen genom Get-AzVirtualNetworkGateway namnet på gatewayen och ange namnet på den.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### System.String

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## ANTECKNINGAR
Du kan inte ändra storlek från Basic/Standard/HighPerformance SKU:er till nya VpnGw1/VpnGw2/VpnGw3 SKU:er. Vidare storlek tillåts inte från/till VpnGw1AZ/VpnGw2AZ/VpnGw3AZ eller ErGw1AZ/ErGw2AZ/ErGw3AZ. Storleksändring tillåts endast i SKU-serien, t.ex. VpnGw1AZ, kan ändras till/från VpnGw2AZ/VpnGw3AZ och ErGw1AZ kan storleksändras till/från ErGw2AZ/ErGw3AZ. Se https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways anvisningar.

## RELATERADE LÄNKAR

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

