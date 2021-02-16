---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 94fbc1e9a4ae8b7befe6961a9648174770458583
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400220"
---
# New-AzApplicationGatewayPathRuleConfig

## SYNOPSIS
Skapar en regel för sökväg till programgateway.

## SYNTAX

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten New-AzApplicationGatewayPathRuleConfig** skapar en sökvägsregel för programgateway.
Regler som skapas av den här cmdleten kan läggas till i en samling konfigurationsinställningar för URL-sökvägskarta och sedan tilldelas till en gateway.
Konfigurationsinställningar för sökvägar används vid belastningsutjämning för programgateway.

## EXEMPEL

### Exempel 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Dessa kommandon skapar en ny sökvägsregel för programgateway och använder sedan cmdleten **Add-AzApplicationGatewayUrlPathMapConfig** för att tilldela regeln till en programgateway.
Det gör du genom att det första kommandot skapar en objektreferens till gatewayen ContosoApplicationGateway.
Den här objektreferensen lagras i en variabel med namnet $Gateway.
Följande två kommandon skapar en adresspool för backend och ett HTTP-inställningsobjekt för backend. Dessa objekt (lagrade i variablerna $AddressPool och $HttpSettings) behövs för att skapa ett sökvägsregelobjekt.
Det fjärde kommandot skapar sökvägsregelobjektet och lagras i en variabel med namnet $PathRuleConfig.
Det femte kommandot använder **Add-AzApplicationGatewayUrlPathMapConfig** för att lägga till konfigurationsinställningarna och den nya sökvägsregeln som finns i inställningarna i ContosoApplicationGateway.

## PARAMETERS

### -BackendAddressPool
Anger en objektreferens till en samling konfigurationsinställningar för backend-adresspool som ska läggas till i konfigurationsinställningarna för gatewaysökvägsregler.
Du kan skapa den här objektreferensen med hjälp New-AzApplicationGatewayBackendAddressPool cmdlet och syntax ungefär så här: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`
Med föregående kommando läggs två IP-adresser (192.16.1.1 och 192.168.1.2) till adresspoolen.
Observera att IP-adressen omges av citattecken och avgränsas med kommatecken.
Den resulterande variabeln $AddressPool sedan användas som parametervärde för parametervärdet för parametern *DefaultBackendAddressPool.*
Backend-adresspoolen representerar IP-adresserna på backend-servrarna.
Dessa IP-adresser bör antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.
Om du använder den här parametern kan du inte använda *parametern DefaultBackendAddressPoolId* i samma kommando.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
Anger ID för en befintlig serverlägesadresspool som kan läggas till i konfigurationsinställningarna för gatewaysökvägsregeln.
Adresspool-IP:n kan returneras med hjälp Get-AzApplicationGatewayBackendAddressPool cmdlet.
När du har ID:t kan du sedan använda parametern *DefaultBackendAddressPoolId* i stället för *parametern DefaultBackendAddressPool.*
Till exempel: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateway/appgwtest/backendAddressPools/ContosoAddressPool" Backend-adresspoolen representerar IP-adresserna på backend-servrarna.
Dessa IP-adresser bör antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.

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

### -BackendHttpSettings
Anger en objektreferens till en samling http-inställningar för server serveruppsättning som ska läggas till i konfigurationsinställningarna för gatewaysökvägsregeln.
Du kan skapa den här objektreferensen med hjälp av cmdleten New-AzApplicationGatewayBackendHttpSettings och syntaxen ungefär så här: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings kan sedan användas som parametervärde för parametervärdet för *parametern DefaultBackendAddressPool:* -DefaultBackendHttpSettings $HttpSettings HTTP-inställningarna för backend konfigurerar egenskaper som port, protokoll och cookie-baserad tillhörighet för en backend-pool.
Om du använder den här parametern kan du inte använda *parametern DefaultBackendHttpSettingsId* i samma kommando.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
Anger ID för en befintlig HTTP-inställningssamling för server serveruppsättning som kan läggas till i konfigurationsinställningarna för gatewaysökvägsregeln.
HTTP-inställnings-IDs kan returneras med hjälp Get-AzApplicationGatewayBackendHttpSettings cmdlet.
När du har ett ID kan du sedan använda parametern *DefaultBackendHttpSettingsId* i stället för *parametern DefaultBackendHttpSettings.*
Till exempel: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateway/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" HTTP-inställningarna för backend konfigurerar egenskaper som port, protocol, och cookiebaserad tillhörighet till en backendpool.
Om du använder den här parametern kan du inte använda *parametern DefaultBackendHttpSettings* i samma kommando.

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

### -Name
Anger namnet på konfigurationen av sökvägsregeln som cmdleten skapar.

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

### -Paths
Anger en eller flera regler för sökvägar till programgateway.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
RedirectConfiguration för programgateway

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
ID för RedirectConfiguration för programgateway

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

### -RewriteRuleSet
Application gateway RewriteRuleSet

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSetId
ID för programmets gateway RewriteRuleSet

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathrule

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[Get-AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[New-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)


[New-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[New-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


