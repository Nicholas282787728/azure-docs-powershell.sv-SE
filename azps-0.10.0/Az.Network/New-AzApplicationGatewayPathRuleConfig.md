---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922163"
---
# New-AzApplicationGatewayPathRuleConfig

## Sammanfattning
Skapar en Sök vägs regel för Programgateway.

## FRÅGESYNTAXEN

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzApplicationGatewayPathRuleConfig** skapar en Sök vägs regel för Programgateway.
Regler som skapas av denna cmdlet kan läggas till i en uppsättning konfigurations inställningar för URL-sökvägar och sedan tilldelas en gateway.

Konfigurations inställningar för Sök vägs karta används för belastnings utjämning i Application Gateway.

## BESKRIVS

### Exempel 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

De här kommandona skapar en ny Application Gateway Sök vägs regel och använder sedan cmdleten **Add-AzApplicationGatewayUrlPathMapConfig** för att tilldela den regeln till en Programgateway.
För att göra detta skapar det första kommandot en objekt referens till gateway-ContosoApplicationGateway.
Denna objekt referens lagras i en variabel som heter $Gateway.

Nästa två kommandon skapar en adresspool och ett objekt med HTTP-inställningar för en server del. de här objekten (lagrade i variabeln $AddressPool och $HttpSettings) behövs för att skapa ett Sök vägs regel objekt.

Det fjärde kommandot skapar Sök vägs regel objekt och lagras i en variabel som heter $PathRuleConfig.

Med det femte kommandot används **Add-AzApplicationGatewayUrlPathMapConfig** för att lägga till konfigurations inställningarna och den nya Sök vägs regeln i dessa inställningar för ContosoApplicationGateway.

## MALLPARAMETRAR

### -BackendAddressPool
Anger en objekt referens till en samling inställningar för adresspool som ska läggas till i inställningar för gateway-sökvägar.
Du kan skapa denna objekt referens genom att använda New-AzApplicationGatewayBackendAddressPool cmdlet och syntax som liknar den här:

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

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
Adresspool-ID: n kan returneras med Get-AzApplicationGatewayBackendAddressPool cmdlet.
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
Du kan skapa denna objekt referens genom att använda New-AzApplicationGatewayBackendHttpSetting cmdlet och syntax som liknar den här:

$HttpSettings = New-AzApplicationGatewayBackendHttpSetting-namn "ContosoHttpSetings"-port 80-Protocol "http"-CookieBasedAffinity "Disabled"

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
HTTP inställnings-ID: n kan returneras med Get-AzApplicationGatewayBackendHttpSetting cmdlet.
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

###  
**New-AzApplicationGatewayPathRuleConfig** accepterar inte förloppet.

## VÄRDEN

###  
**New-AzApplicationGatewayPathRuleConfig** skapar nya instanser av **Microsoft. Azure. commands. Network. Models. PSApplicationGatewayPathRule** .

## ANMÄRKNINGAR

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


