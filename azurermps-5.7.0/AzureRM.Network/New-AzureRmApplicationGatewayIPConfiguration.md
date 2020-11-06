---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 8b550d0ba38036b527a1082f4ce48f40913a54e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581088"
---
# New-AzureRmApplicationGatewayIPConfiguration

## Sammanfattning
Skapar en IP-konfiguration för en Programgateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### SetByResourceId
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmApplicationGatewayIPConfiguration** skapar en IP-konfiguration för en Programgateway.
IP-konfigurationen innehåller det undernät då Programgateway distribueras.

## BESKRIVS

### Exempel 1: skapa en IP-konfiguration för en Programgateway.
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen "ResourceGroup01".

Det andra kommandot får under nätets konfiguration för det undernät som det virtuella nätverket i föregående kommando tillhör och lagrar det i $Subnet variabeln.

Det tredje kommandot skapar IP-konfigurationen med $Subnet.

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
Anger namnet på den IP-konfiguration som ska skapas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Undernät
Anger ett under näts objekt.
Det här är det undernät där Application Gateway distribueras.

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Anger nät-ID.
Det här är det undernät där programgatewayen distribueras.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayIPConfiguration

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmApplicationGatewayIPConfiguration](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[Get-AzureRmApplicationGatewayIPConfiguration](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[Remove-AzureRmApplicationGatewayIPConfiguration](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[Set-AzureRmApplicationGatewayIPConfiguration](./Set-AzureRmApplicationGatewayIPConfiguration.md)


