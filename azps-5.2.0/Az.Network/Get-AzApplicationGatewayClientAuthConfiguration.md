---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: eee7040dab93a4f73bacdf440c6450a525fab9a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389463"
---
# Get-AzApplicationGatewayClientAuthConfiguration

## Sammanfattning
Hämtar konfigurationen för klientautentisering för ett SSL-profil objekt.

## FRÅGESYNTAXEN

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzApplicationGatewayClientAuthConfiguration** hämtar konfigurationen för klientautentisering för ett SSL-profil objekt.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln. Det andra kommandot får den SSL-profil som heter SslProfile01 för $AppGw och lagrar den $SslProfile variabel. Med det senaste kommandot får konfigurationen för klientautentisering från SSL-profilen $SslProfile och lagras i $ClientAuthConfig-variabeln.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -SslProfile
SSL-profil

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayClientAuthConfiguration

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzApplicationGatewayClientAuthConfiguration](./New-AzApplicationGatewayClientAuthConfiguration.md)

[Add-AzApplicationGatewayClientAuthConfiguration](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[Remove-AzApplicationGatewayClientAuthConfiguration](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[Set-AzApplicationGatewayClientAuthConfiguration](./Set-AzApplicationGatewayClientAuthConfiguration.md)