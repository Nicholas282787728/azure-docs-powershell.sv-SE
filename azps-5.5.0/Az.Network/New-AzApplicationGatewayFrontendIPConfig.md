---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252404"
---
# New-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Skapar en IP-konfiguration på en frontend för en programgateway.

## SYNTAX

### SetByResourceId
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten New-AzApplicationGatewayFrontendIPConfig** skapar en frontend IP-konfiguration för en Azure-programgateway.
En programgateway har stöd för två typer av IP-konfiguration på frontend: 
- Offentliga IP-adresser – privata IP-adresser med intern belastningsutjämning (ILB).
 En programgateway kan ha minst en offentlig IP-adress och en privat IP-adress.
Den offentliga IP-adressen och den privata IP-adressen bör läggas till separat som frontend IP-adresser.

## EXEMPEL

### Exempel 1: Skapa en IP-konfiguration på framsidan med ett offentligt IP-resursobjekt
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

Det första kommandot skapar ett offentligt IP-resursobjekt och lagrar det i $PublicIP variabeln.
Det andra kommandot använder $PublicIP för att skapa en ny IP-konfiguration med namnet FrontEndIP01 och lagrar den i $FrontEnd variabeln.

### Exempel 2: Skapa en statisk privat IP som IP-adress på framsidan
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Det första kommandot får ett virtuellt nätverk med namnet VNet01 som tillhör resursgruppen ResourceGroup01 och lagrar det i $VNet variabeln.
Det andra kommandot hämtar en undernätskonfiguration med namnet Subnet01 $VNet från det första kommandot och lagrar den i $Subnet variabeln.
Det tredje kommandot skapar en frontend IP-konfiguration med namnet FrontEndIP02 med $Subnet från det andra kommandot och den privata IP-adressen 10.0.1.1, och lagrar sedan den i variabeln $FrontEnd.

### Exempel 3: Skapa en dynamisk privat IP som IP-adress på framsidan
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

Det första kommandot får ett virtuellt nätverk med namnet VNet01 som tillhör resursgruppen ResourceGroup01 och lagrar det i $VNet variabeln.
Det andra kommandot hämtar en undernätskonfiguration med namnet Subnet01 $VNet från det första kommandot och lagrar den i $Subnet variabeln.
Det tredje kommandot skapar en frontend IP-konfiguration med namnet FrontEndIP03 $Subnet från det andra kommandot och lagrar den i $FrontEnd variabeln.

## PARAMETERS

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
Anger namnet på den frontend-IP-konfiguration som cmdleten skapar.

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
Anger den privata IP-adressen som denna cmdlet associerar med frontend-IP-adressen för programgatewayen.
Det här kan bara anges om ett undernät har angetts.
Denna IP tilldelas statiskt från undernätet.

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
Anger det offentliga IP-adressobjektet som denna cmdlet associerar med frontend-IP-adressen för programgatewayen.

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
Anger det offentliga IP-adress-ID som denna cmdlet associerar med frontend-IP för programgatewayen.

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
Anger det undernätsobjekt som denna cmdlet associerar med ip-adressen på frontend för programgatewayen.
Om du anger den här parametern antyder det att gatewayen använder en privat IP-adress.
Om *parametern PrivateIPAddress* anges, bör den tillhöra undernätet som anges av den här parametern.
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
Anger undernätets ID som denna cmdlet associerar med frontend IP-konfigurationen av programgatewayen.
Om du anger *parametern Undernät* antyder det att gatewayen använder en privat IP-adress.
Om *parametern PrivateIPAddress* anges, bör den tillhöra det undernät som anges av *undernätet.*
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

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


