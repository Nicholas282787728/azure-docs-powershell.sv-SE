---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236511"
---
# Set-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Ändrar en ip-adresskonfiguration på frontend.

## SYNTAX

### SetByResourceId
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Set-AzApplicationGatewayFrontendIPConfig** uppdaterar en IP-konfiguration på framsidan.
En programgateway har stöd för två typer av IP-adresser på frontend: 
- Offentliga IP-adresser
- Privata IP-adresser där konfigurationen använder intern belastningsutjämning (ILB) En programgateway kan ha minst en offentlig IP-adress och en privat IP-adress.
En offentlig IP-adress och en privat IP-adress bör läggas till separat som IP-adresser på framsidan.

## EXEMPEL

### Exempel 1: Ange en offentlig IP som frontend-IP för en programgateway
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

Det första kommandot skapar ett offentligt IP-adressobjekt och lagrar det i $PublicIp variabeln.
Det andra kommandot hämtar programgatewayen med namnet ApplicationGateway01 som tillhör resursgruppen ResourceGroup01 och lagrar den i $AppGw variabeln.
Det tredje kommandot uppdaterar frontend-IP-konfigurationen med namnet FrontEndIp01 för gatewayen i $AppGw, med den adress som lagras i $PublicIp.

### Exempel 2: Ange en statisk privat IP som frontend-IP för en programgateway
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Det första kommandot får ett virtuellt nätverk med namnet VNet01 som tillhör resursgruppen ResourceGroup01 och lagrar det i $VNet variabeln.
Det andra kommandot hämtar en undernätskonfiguration med namnet Subnet01 $VNet från det första kommandot och lagrar den i $Subnet variabeln.
Det tredje kommandot hämtar programgatewayen med namnet ApplicationGateway01 som tillhör resursgruppen ResourceGroup01 och lagrar den i $AppGw variabeln.
Det fjärde kommandot lägger till en frontend IP-konfiguration med namnet FrontendIP02 med $Subnet från det andra kommandot och den privata IP-adressen 10.0.1.1.

### Exempel 3: Ange en dynamisk privat IP som frontend-IP för en programgateway
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

Det första kommandot får ett virtuellt nätverk med namnet VNet01 som tillhör resursgruppen ResourceGroup01 och lagrar det i $VNet variabeln.
Det andra kommandot hämtar en undernätskonfiguration med namnet Subnet01 $VNet från det första kommandot och lagrar den i $Subnet variabeln.
Det tredje kommandot hämtar programgatewayen med namnet ApplicationGateway01 som tillhör resursgruppen ResourceGroup01 och lagrar den i $AppGw variabeln.
Det fjärde kommandot lägger till en frontend IP-konfiguration med namnet FrontendIP02 med $Subnet från det andra kommandot.

## PARAMETERS

### -ApplicationGateway
Anger ett programgatewayobjekt där IP-konfigurationen ska ändras.

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Anger namnet på frontend-IP-konfigurationen som denna cmdlet ändrar.

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

### -PrivateIPAddress
Anger den privata IP-adressen.
Om den anges tilldelas den här IP-adressen statiskt från undernätet.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfiguration
PrivateLinkConfiguration

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfigurationId
PrivateLinkConfigurationId

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

### -PublicIPAddress
Anger den offentliga IP-adressen.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
Anger ID för den offentliga IP-adressen.

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

### -Subnet
Anger det undernät som används i programmets gateway.
Ange den här parametern om gatewayen använder en privat IP-adress.
Om adress *till PrivateIPAddress* har angetts, bör den tillhöra det här undernätet.
Om *PrivateIPAddress* inte har angetts hämtas en av IP-adresserna från det här undernätet dynamiskt som frontend IP-adress för programmets gateway.

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
Anger undernätets ID.
Ange den här parametern om gatewayen använder en privat IP-adress.
Om *parametern PrivateIPAddress* anges, bör den tillhöra det här undernätet.
Om *PrivateIPAddress* inte har angetts hämtas en av IP-adresserna från det här undernätet dynamiskt som frontend IP-adress för programmets gateway.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[New-AzApplicationGatewayFrontendIPConfig](./New-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)


