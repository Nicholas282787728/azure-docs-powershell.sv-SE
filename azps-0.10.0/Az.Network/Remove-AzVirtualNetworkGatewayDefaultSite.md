---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: bfd90797ff60c42927b23424e3c100efd16a6d24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924337"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## Sammanfattning
Tar bort standard webbplatsen från en virtuell nätverksgateway.

## FRÅGESYNTAXEN

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzVirtualNetworkGatewayDefaultSite** tar bort den tvingande standard webbplatsen för tunnel trafik från en virtuell nätverksgateway.
Med tvingande tunnlar kan du omdirigera Internet-bundna trafik från virtuella Azure-datorer till det lokala nätverket. Detta gör att du kan kontrol lera och granska trafiken innan den släpps.
Framtvingad tunnel trafik utförs med en VPN-tunnel (Virtual Private Network). Denna tunnel kräver en standard webbplats, en lokal gateway där all Azure Internet-bunden trafik omdirigeras.

**Remove-AzVirtualNetworkGatewayDefaultSite** tar bort standard webbplatsen som är tilldelad en gateway.
Om du gör det måste du använda Set-AzVirtualNetworkGatewayDefaultSite för att tilldela en ny standard webbplats innan gatewayen kan användas för tvingande tunnel.

## BESKRIVS

### Exempel 1: ta bort standard webbplatsen som är kopplad till en virtuell nätverksgateway
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

I det här exemplet tas standard webbplatsen för närvarande till en virtuell nätverksgateway som heter ContosoVirtualGateway.

Det första kommandot använder **Get-AzVirtualNetworkGateway** för att skapa en objekt referens till gatewayen. Denna objekt referens lagras i en variabel som heter $Gateway.

Det andra kommandot använder **Remove-AzVirtualNetworkGatewayDefaultSite** för att ta bort standard webbplatsen som har tilldelats till den gatewayen.

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

### -VirtualNetworkGateway
Anger en objekt referens till den virtuella nätverksgateway som innehåller den standard webbplats som ska tas bort.
Du kan skapa en objekt referens till en virtuell nätverksgateway genom att använda Get-AzVirtualNetworkGateway och ange namnet på gatewayen.

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

## RELATERADE LÄNKAR

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


