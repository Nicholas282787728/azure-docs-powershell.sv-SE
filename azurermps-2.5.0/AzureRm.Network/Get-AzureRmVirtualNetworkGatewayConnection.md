---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: c0599f599770467c3528cff902d2d60434c335e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929782"
---
# Get-AzureRmVirtualNetworkGatewayConnection

## Sammanfattning
Ansluter till en virtuell nätverksgateway

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Anslutningen för virtuell nätverksgateway är det objekt som representerar IPsec-tunneln (plats-till-plats eller VNet som är ansluten till din virtuella nätverksgateway i Azure.

Cmdleten **Get-AzureRmVirtualNetworkGatewayConnection** returnerar anslutningen baserat på namn-och resurs grupp namn.

## BESKRIVS

### 1: skaffa en virtuell nätverksgateway
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

Returnerar objektet för den virtuella Nätverksgatewayen med namnet "tunnel" i resurs gruppen "myRG"

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

### -Namn
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

