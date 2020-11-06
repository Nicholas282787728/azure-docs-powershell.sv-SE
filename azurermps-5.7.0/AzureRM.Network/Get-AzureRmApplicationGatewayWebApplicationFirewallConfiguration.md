---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 44411d8f763e217d5513440a90f713c92c6d6398
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580356"
---
# Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration

## Sammanfattning
Hämtar WAF konfiguration för en Programgateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** hämtar webb program brand väggen (WAF) för en Programgateway.

## BESKRIVS

### Exempel 1: Hämta en brand Väggs konfiguration för Application Gateway
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

Det första kommandot hämtar programgatewayen med namnet ApplicationGateway01 och lagrar den sedan i $AppGW variabel.

Det andra kommandot får brand Väggs konfigurationen för programgatewayen i $AppGW och lagrar den sedan i $FirewallConfig.

## MALLPARAMETRAR

### -ApplicationGateway
Anger ett Application Gateway-objekt.
Du kan använda Get-AzureRmApplicationGateway cmdlet för att hämta ett objekt för Application Gateway.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### PSApplicationGateway
Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallConfiguration

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


