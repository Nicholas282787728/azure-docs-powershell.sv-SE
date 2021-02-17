---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225663"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Anger standardwebbplatsen för en virtuell nätverksgateway.

## SYNTAX

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzVirtualNetworkGatewayDefaultSite** tilldelar en standardwebbplats för tvingad tunnel till en virtuell nätverksgateway.
Tvingade tunnlar är ett sätt för dig att omdirigera Internetbunden trafik från Azure-virtuella datorer till ditt lokala nätverk. det här gör att du kan kontrollera och granska trafiken innan du släpper den.
Tvingad tunnel utförs med hjälp av en virtuell privat nätverks tunnel (VPN). Den här tunneln kräver en standardplats, en lokal gateway där all Azure Internetbunden trafik omdirigeras.
**Set-AzVirtualNetworkGatewayDefaultSite** är ett sätt att ändra standardwebbplatsen som tilldelats till en gateway.

## EXEMPEL

### Exempel 1: Tilldela en standardwebbplats till en virtuell nätverksgateway
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

I det här exemplet tilldelas en standardwebbplats till en virtuell nätverksgateway med namnet ContosoVirtualGateway.
Med det första kommandot skapas en objektreferens till en lokal gateway med namnet ContosoLocalGateway.
Den här objektreferensen som lagras i den $LocalGateway representerar den gateway som ska konfigureras som standardwebbplats.
Det andra kommandot skapar sedan en objektreferens till den virtuella nätverksgatewayen och lagrar resultatet i variabeln $VirtualGateway.
Det tredje kommandot använder cmdleten **Set-AzVirtualNetworkGatewayDefaultSite** till att tilldela standardwebbplatsen till ContosoVirtualGateway.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -GatewayDefaultSite
Anger en objektreferens till den lokala nätverksgateway som ska tilldelas som standardwebbplats för det angivna virtuella nätverket.
Du kan använda cmdlet Get-AzLocalNetworkGateway för att skapa en objektreferens till en lokal gateway.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Anger en objektreferens till den virtuella nätverksgateway där standardwebbplatsen ska tilldelas.
Du kan skapa en objektreferens till en virtuell nätverksgateway genom att använda **Get-AzVirtualNetworkGateway** och ange namnet på gatewayen.
Variabeln $VirtualGateway sedan användas som parametervärde för *VirtualNetworkGateway-parametern:*

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

### Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


