---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213542"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Tar bort standardwebbplatsen från en virtuell nätverksgateway.

## SYNTAX

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Remove-AzVirtualNetworkGatewayDefaultSite** tar bort standardplatsen för tvingad tunnel från en virtuell nätverksgateway.
Tvingade tunnlar är ett sätt för dig att omdirigera Internetbunden trafik från Azure-virtuella datorer till ditt lokala nätverk. det här gör att du kan kontrollera och granska trafiken innan du släpper den.
Tvingad tunnel utförs med hjälp av en virtuell privat nätverks tunnel (VPN). Den här tunneln kräver en standardplats, en lokal gateway där all Azure Internetbunden trafik omdirigeras.
**Remove-AzVirtualNetworkGatewayDefaultSite** tar bort standardwebbplatsen som tilldelats till en gateway.
Om du gör det måste du använda Set-AzVirtualNetworkGatewayDefaultSite tilldela en ny standardwebbplats innan gatewayen kan användas för tvingad tunnel.

## EXEMPEL

### Exempel 1: Ta bort standardwebbplatsen som tilldelats en virtuell nätverksgateway
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

Det här exemplet tar bort den standardwebbplats som för närvarande är tilldelad en virtuell nätverksgateway med namnet ContosoVirtualGateway.
Det första kommandot använder **Get-AzVirtualNetworkGateway** för att skapa en objektreferens till gatewayen. objektreferensen lagras i en variabel med namnet $Gateway.
Det andra kommandot använder sedan **Remove-AzVirtualNetworkGatewayDefaultSite** för att ta bort standardwebbplatsen som tilldelats den gatewayen.

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

### -VirtualNetworkGateway
Anger en objektreferens till den virtuella nätverksgateway som innehåller standardwebbplatsen som ska tas bort.
Du kan skapa en objektreferens till en virtuell nätverksgateway genom att Get-AzVirtualNetworkGateway och ange namnet på gatewayen.

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

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


