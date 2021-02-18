---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: f769eb91d524bc9115199127833471246f6fdd1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224071"
---
# Add-AzApplicationGatewayHttpListener

## SYNOPSIS
Lägger till en HTTP-lyssnare i en programgateway.

## SYNTAX

### SetByResourceId
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResource
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Add-AzApplicationGatewayHttpListener** lägger till en HTTP-lyssnare i en programgateway.

## EXEMPEL

### Exempel 1: Lägga till en HTTP-lyssnare
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

Det första kommandot hämtar programmets gateway och lagrar den i variabeln $AppGw variabeln. Det andra kommandot lägger till HTTP-lyssnaren i programmets gateway.

### Exempel 2: Lägga till en HTTPS-lyssnare med SSL
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

Det första kommandot hämtar programmets gateway och lagrar den i variabeln $AppGw variabeln.
Det andra kommandot lägger till lyssnaren, som använder HTTPS-protokollet, i programmets gateway.

### Exempel 3: Lägga till en HTTPS-lyssnare med SSL och HostNames
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com","www.microsoft.com"
```

Det första kommandot hämtar programmets gateway och lagrar den i variabeln $AppGw variabeln.
Det andra kommandot lägger till lyssnaren, som använder HTTPS-protokollet, med SSL-certifikat och HostNames, i programmets gateway.

## PARAMETERS

### -ApplicationGateway
Anger programgatewayen där denna cmdlet lägger till en HTTP-lyssnare.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CustomErrorConfiguration
Kundfel av en programgateway

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -FirewallPolicy
FirewallPolicy

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyId
FirewallPolicyId

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendIPConfiguration
Anger programmets gatewayens IP-resursobjekt.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendIPConfigurationId
Anger programmets gateway-IP-ID.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPort
Anger programmets gatewayens frontend-portobjekt.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPortId
Anger programmets gatewayens frontend-port-ID.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostName
Anger värdnamnet som denna cmdlet lägger till en HTTP-lyssnare till.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostNames
Värdnamn

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Anger namnet på frontend-porten som det här kommandot lägger till.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Anger protokollet för HTTP-lyssnaren.
Både HTTP och HTTPS stöds.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireServerNameIndication
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCertificate
Anger SSL-certifikatet för HTTP-lyssnaren.
Måste anges om HTTPS har valts som lyssnarprotokoll.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCertificateId
Anger HTTP-lyssnarens SSL-certifikat-ID.
Måste anges om HTTPS har valts som lyssnarprotokoll.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslProfile
SslProfile

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslProfileId
SslProfileId

```yaml
Type: System.String
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

[Get-AzApplicationGatewayHttpListener](./Get-AzApplicationGatewayHttpListener.md)

[New-AzApplicationGatewayHttpListener](./New-AzApplicationGatewayHttpListener.md)

[Remove-AzApplicationGatewayHttpListener](./Remove-AzApplicationGatewayHttpListener.md)

[Set-AzApplicationGatewayHttpListener](./Set-AzApplicationGatewayHttpListener.md)


