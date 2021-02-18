---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228071"
---
# Add-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Lägger till en IP-konfiguration på framsidan till en programgateway.

## SYNTAX

### SetByResourceId
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Add-AzApplicationGatewayFrontendIPConfig** lägger till en frontend IP-konfiguration i en programgateway.
En programgateway har stöd för två typer av IP-konfigurationer av typen frontend: 
- Offentliga IP-adresser
- Privata IP-adresser som använder intern belastningsutjämning (ILB) En programgateway kan ha minst en offentlig IP och en privat IP.
Lägg till den offentliga IP-adressen och den privata IP-adressen som separata IP-adresser på framsidan.

## EXEMPEL

### Exempel 1: Lägga till en offentlig IP som IP-adress på framsidan
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

Det första kommandot skapar ett offentligt IP-adressobjekt och lagrar det i $PublicIp variabeln.
Det andra kommandot hämtar programgatewayen med namnet ApplicationGateway01 som tillhör resursgruppen ResourceGroup01 och lagrar den i $AppGw variabeln.
Det tredje kommandot lägger till frontend IP-konfigurationen med namnet FrontEndIp01 för gatewayen i $AppGw, med den adress som lagras i $PublicIp.

### Exempel 2: Lägg till en statisk privat IP som IP-adress på framsidan
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Det första kommandot får ett virtuellt nätverk med namnet VNet01 som tillhör resursgruppen ResourceGroup01 och lagrar det i $VNet variabeln.
Det andra kommandot hämtar en undernätskonfiguration med namnet Subnet01 $VNet från det första kommandot och lagrar den i $Subnet variabeln.
Det tredje kommandot hämtar programgatewayen med namnet ApplicationGateway01 som tillhör resursgruppen ResourceGroup01 och lagrar den i $AppGw variabeln.
Det fjärde kommandot lägger till en frontend IP-konfiguration med namnet FrontendIP02 med $Subnet från det andra kommandot och den privata IP-adressen 10.0.1.1.

### Exempel 3: Lägga till en dynamisk privat IP som IP-adress på framsidan
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

Det första kommandot får ett virtuellt nätverk med namnet VNet01 som tillhör resursgruppen ResourceGroup01 och lagrar det i $VNet variabeln.
Det andra kommandot hämtar en undernätskonfiguration med namnet Subnet01 $VNet från det första kommandot och lagrar den i $Subnet variabeln.
Det tredje kommandot hämtar programgatewayen med namnet ApplicationGateway01 som tillhör resursgruppen ResourceGroup01 och lagrar den i $AppGw variabeln.
Det fjärde kommandot lägger till en frontend IP-konfiguration med namnet FrontendIP02 med $Subnet från det andra kommandot.

## PARAMETERS

### -ApplicationGateway
Anger programgatewayen där den här cmdleten lägger till en IP-konfiguration på framsidan.

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
Anger namnet på den frontend-IP-konfiguration som ska läggas till.

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
Anger den privata IP-adress som ska läggas till som en frontend-IP för programgatewayen.
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
Anger den offentliga IP-adressen som denna cmdlet lägger till som en FRONTEND IP-adress för programmets gateway.

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
Anger ID för den offentliga IP-adressen som denna cmdlet lägger till som en frontend IP-adress för programgatewayen.

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
Anger undernätet som denna cmdlet lägger till som frontend IP-konfiguration.
Om du anger den här parametern antyder det att programmets gateway har stöd för en privat IP-baserad konfiguration.
Om *parametern PrivateIPAddress* anges, bör den tillhöra det här undernätet.
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
Anger undernätets ID som denna cmdlet lägger till som frontend IP-konfiguration.
Att skicka undernät antyder privat IP.
Om *parametern PrivateIPAddress* anges, bör den tillhöra det här undernätet.
Annars hämtas en IP från det här undernätet dynamiskt som frontend-IP för programgatewayen.

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

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[New-AzApplicationGatewayFrontendIPConfig](./New-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


