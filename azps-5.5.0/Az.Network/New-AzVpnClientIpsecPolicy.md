---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227614"
---
# New-AzVpnClientIpsecPolicy

## SYNOPSIS
Med det här kommandot kan användarna skapa principobjektet Vpn ipsec som anger ett eller alla värden, till exempel IpsecEncryption, IpsecIntegrity, IkeEncryption,IkeIntegrity,DhGroup,PfsGroup, att ange för VPN-gatewayen. Med det här kommandot kan utdataobjekt användas för att ange vpn ipsec-principen för både ny/befintlig gateway.

## SYNTAX

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Med det här kommandot kan användarna skapa principobjektet Vpn ipsec som anger ett eller alla värden, till exempel IpsecEncryption, IpsecIntegrity, IkeEncryption,IkeIntegrity,DhGroup,PfsGroup, att ange för VPN-gatewayen. Med det här kommandot kan utdataobjekt användas för att ange vpn ipsec-principen för både ny/befintlig gateway.

## EXEMPEL

### Exempel 1: Definiera principobjektet vpn ipsec:
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

Den här cmdleten används för att skapa principobjektet vpn ipsec med hjälp av de godkända ena eller alla parametrarnas värden som användaren kan överföra till param:VpnClientIpsecPolicy för PS-kommandot låta: New-AzVirtualNetworkGateway (Skapa ny VPN-gateway) / Set-AzVirtualNetworkGateway (befintlig VPN Gateway-uppdatering) i ResourceGroup:

### Exempel 2: Skapa ny virtuell nätverksgateway med inställning av vpn-anpassad ipsec-princip:
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Den här cmdleten returnerar det virtuella nätverksgatewayobjektet när det har skapats. 

### Exempel 3: Ange principen för vpn-anpassad ipsec på befintlig virtuell nätverksgateway:
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Den här cmdleten returnerar objektet för virtuell nätverksgateway när du har inställningen vpn-anpassad ipsec-princip.

### Exempel 4: Hämta virtuell nätverksgateway för att se om den anpassade VPN-principen är korrekt inställd:
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

Den här cmdleten returnerar virtuellt nätverksgatewayobjekt.

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

### -DhGroup
VpnClient DH-grupperna som används i IKE Fas 1 för inledande SA

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeEncryption
VpnClient IKE-krypteringsalgoritmen (IKE Fas 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeIntegrity
VpnClient IKE-integritetsalgoritmen (IKE Fas 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecEncryption
VpnClient IPSec-krypteringsalgoritmen (IKE Fas 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipsec-integritet
VpnClient IPSec-integritetsalgoritmen (IKE Fas 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfsGroup
VpnClient PFS-grupperna som används i IKE Fas 2 för nya barnet SA

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SADataSize
Payload-storleken för VpnClient IPSec (kallas även snabbläge eller fas 2 SA) i KB

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SALifeTime
VpnClient IPSec Security Association (kallas även snabbläge eller fas 2 SA) livslängd i sekunder

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy

## ANTECKNINGAR

## RELATERADE LÄNKAR
