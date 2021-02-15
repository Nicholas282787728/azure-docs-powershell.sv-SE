---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252397"
---
# New-AzApplicationGatewayPathRuleConfig

## SYNOPSIS
Skapar en regel för sökväg till programgateway.

## SYNTAX

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
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
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Dessa kommandon skapar en ny sökvägsregel för programgateway och använder sedan cmdleten **Add-AzApplicationGatewayUrlPathMapConfig** för att tilldela regeln till en programgateway.
Det gör du genom att det första kommandot skapar en objektreferens till gatewayen ContosoApplicationGateway.
Den här objektreferensen lagras i en variabel med namnet $Gateway.
Följande två kommandon skapar en adresspool för backend och ett HTTP-inställningsobjekt för backend. Dessa objekt (lagrade i variablerna $AddressPool och $HttpSettings) behövs för att skapa ett sökvägsregelobjekt.
Det fjärde kommandot skapar sökvägsregelobjektet och lagras i en variabel med namnet $PathRuleConfig.
Det femte kommandot använder **Add-AzApplicationGatewayUrlPathMapConfig** för att lägga till konfigurationsinställningarna och den nya sökvägsregeln som finns i inställningarna i ContosoApplicationGateway.

### Exempel 2
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

Det här kommandot skapar en sökvägsregel med namnet som "bas", sökvägar som "/bas", BackendAddressPool som $AddressPool, BackendHttpSettings som $HttpSettings och FirewallPolicy som $firewallPolicy.ngs och den nya sökvägsregeln som finns i inställningarna för ContosoApplicationGateway.

## PARAMETERS

### -BackendAddressPool
Anger en objektreferens till en samling konfigurationsinställningar för backend-adresspool som ska läggas till i konfigurationsinställningarna för gatewaysökvägsregler.
Du kan skapa den här objektreferensen med hjälp New-AzApplicationGatewayBackendAddressPool cmdleten och syntaxen ungefär så här: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`
Med föregående kommando läggs två IP-adresser (192.16.1.1 och 192.168.1.2) till adresspoolen.
Observera att IP-adressen omges av citattecken och avgränsas med kommatecken.
Den resulterande variabeln $AddressPool sedan användas som parametervärde för parametervärdet för parametern *DefaultBackendAddressPool.*
Backend-adresspoolen representerar IP-adresserna på backend-servrarna.
Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.
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
Adresspool-IDt kan returneras med hjälp av Get-AzApplicationGatewayBackendAddressPool cmdlet.
När du har ID:t kan du sedan använda parametern *DefaultBackendAddressPoolId* i stället för *parametern DefaultBackendAddressPool.*
Till exempel: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateway/appgwtest/backendAddressPools/ContosoAddressPool" Backend-adresspoolen representerar IP-adresserna på backend-servrarna.
Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.

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
Du kan skapa den här objektreferensen genom att använda cmdleten New-AzApplicationGatewayBackendHttpSettings och syntaxen ungefär så här: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings kan sedan användas som parametervärde för parametervärdet för *parametern DefaultBackendAddressPool:* -DefaultBackendHttpSettings $HttpSettings HTTP-inställningarna för backend konfigurerar egenskaper som port, protokoll och cookie-baserad tillhörighet för en backend-pool.
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

### -FirewallPolicy
Anger objektreferensen till en brandväggsprincip på översta nivån. Du kan skapa objektreferensen med hjälp New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.
$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level. kommandot ovan skulle skapa standardinställningar för principen och hanterade regler.
I stället för standardvärdena kan användare ange PolicySettings, ManagedRules med hjälp New-AzApplicationGatewayFirewallPolicySettings och New-AzApplicationGatewayFirewallPolicyManagedRules respektive.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyId
Anger ID för en befintlig brandväggsresurs på toppnivå i webbprogram.
Brandväggsprincip-IDS kan returneras med hjälp av Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet. När vi har ID:t kan du använda *FirewallPolicyId-parametern* i stället för *FirewallPolicy-parametern.*
Till exempel: -FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

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

[New-AzApplicationGatewayBackendHttpSetting](./New-AzApplicationGatewayBackendHttpSetting.md)

[New-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[New-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


