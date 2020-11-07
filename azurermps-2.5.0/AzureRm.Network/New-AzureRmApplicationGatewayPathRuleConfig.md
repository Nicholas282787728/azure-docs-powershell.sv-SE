---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaypathruleconfig
schema: 2.0.0
ms.openlocfilehash: 95865de8e99ad09a755329b742f69ebe1e935d72
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928737"
---
# New-AzureRmApplicationGatewayPathRuleConfig

## Sammanfattning
Skapar en Sök vägs regel för Programgateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### SetByResourceId
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmApplicationGatewayPathRuleConfig** skapar en Sök vägs regel för Programgateway.
Regler som skapas av denna cmdlet kan läggas till i en uppsättning konfigurations inställningar för URL-sökvägar och sedan tilldelas en gateway.

Konfigurations inställningar för Sök vägs karta används för belastnings utjämning i Application Gateway.

## BESKRIVS

### Exempel 1
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

De här kommandona skapar en ny Application Gateway Sök vägs regel och använder sedan cmdleten **Add-AzureRmApplicationGatewayUrlPathMapConfig** för att tilldela den regeln till en Programgateway.
För att göra detta skapar det första kommandot en objekt referens till gateway-ContosoApplicationGateway.
Denna objekt referens lagras i en variabel som heter $Gateway.

Nästa två kommandon skapar en adresspool och ett objekt med HTTP-inställningar för en server del. de här objekten (lagrade i variabeln $AddressPool och $HttpSettings) behövs för att skapa ett Sök vägs regel objekt.

Det fjärde kommandot skapar Sök vägs regel objekt och lagras i en variabel som heter $PathRuleConfig.

Med det femte kommandot används **Add-AzureRmApplicationGatewayUrlPathMapConfig** för att lägga till konfigurations inställningarna och den nya Sök vägs regeln i dessa inställningar för ContosoApplicationGateway.

## MALLPARAMETRAR

### -BackendAddressPool
Anger en objekt referens till en samling inställningar för adresspool som ska läggas till i inställningar för gateway-sökvägar.
Du kan skapa denna objekt referens genom att använda New-AzureRmApplicationGatewayBackendAddressPool cmdlet och syntax som liknar den här:

`$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

Med föregående kommando läggs två IP-adresser (192.16.1.1 och 192.168.1.2) till i adresspoolen.
Observera att IP-adressen omges av citat tecken och avgränsas med kommatecken.

Den resulterande variabeln $AddressPool och kan sedan användas som parameter värde för parametern *DefaultBackendAddressPool* .

Server delens adresspool representerar IP-adresserna på backend-servrarna.
Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.
Om du använder den här parametern kan du inte använda parametern *DefaultBackendAddressPoolId* i samma kommando.

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
Anger ID för en befintlig backend-adresspool som kan läggas till i inställningar för gateway-brandväggsregel.
Adresspool-ID: n kan returneras med Get-AzureRmApplicationGatewayBackendAddressPool cmdlet.
När du har ID-numret kan du använda parametern *DefaultBackendAddressPoolId* i stället för parametern *DefaultBackendAddressPool* .
Till exempel:

-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"

Server delens adresspool representerar IP-adresserna på backend-servrarna.
Dessa IP-adresser ska antingen tillhöra det virtuella nätverkets undernät eller vara offentliga IP-adresser.

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

### -BackendHttpSettings
Anger en objekt referens till en samling av Server dels HTTP-inställningar som ska läggas till i konfigurations inställningarna för gateway-brandväggsregel.
Du kan skapa denna objekt referens genom att använda New-AzureRmApplicationGatewayBackendHttpSettings cmdlet och syntax som liknar den här:

$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-namn "ContosoHttpSetings"-port 80-Protocol "http"-CookieBasedAffinity "Disabled"

Den resulterande variabeln, $HttpSettings, kan sedan användas som parameter värde för parametern *DefaultBackendAddressPool* :

-DefaultBackendHttpSettings $HttpSettings

Server delens HTTP-inställningar konfigurera egenskaper som port, protokoll och cookie-baserad tillhörighet för en server del.
Om du använder den här parametern kan du inte använda parametern *DefaultBackendHttpSettingsId* i samma kommando.

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
Anger ID för en befintlig HTTP-konfigurationsfil i Server delen som kan läggas till i inställningarna för gateway-brandväggsregel.
HTTP inställnings-ID: n kan returneras med Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet.
När du har ID-numret kan du använda parametern *DefaultBackendHttpSettingsId* i stället för parametern *DefaultBackendHttpSettings* .
Till exempel:

-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"

Server delens HTTP-inställningar konfigurera egenskaper som port, protokoll och cookie-baserad tillhörighet för en server del.
Om du använder den här parametern kan du inte använda parametern *DefaultBackendHttpSettings* i samma kommando.

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

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på den Sök vägs regel som den här cmdleten skapar.

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

### -Banor
Anger en eller flera Sök vägs regler för Application Gateway.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
RedirectConfiguration för Application Gateway

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
ID för Application Gateway RedirectConfiguration

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

###  
**New-AzureRmApplicationGatewayPathRuleConfig** accepterar inte förloppet.

## VÄRDEN

###  
**New-AzureRmApplicationGatewayPathRuleConfig** skapar nya instanser av **Microsoft. Azure. commands. Network. Models. PSApplicationGatewayPathRule** .

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmApplicationGatewayUrlPathMapConfig](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[Get-AzureRmApplicationGatewayUrlPathMapConfig](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[New-AzureRmApplicationGatewayBackendAddressPool](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[New-AzureRmApplicationGatewayBackendHttpSettings](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[New-AzureRmApplicationGatewayPathRuleConfig](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[New-AzureRmApplicationGatewayUrlPathMapConfig](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Remove-AzureRmApplicationGatewayUrlPathMapConfig](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Set-AzureRmApplicationGatewayUrlPathMapConfig](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


