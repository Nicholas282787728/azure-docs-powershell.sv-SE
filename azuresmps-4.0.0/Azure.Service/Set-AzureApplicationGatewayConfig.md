---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099659"
---
# Set-AzureApplicationGatewayConfig

## Sammanfattning
Konfigurerar en Programgateway.

## FRÅGESYNTAXEN

### configFile
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### configObject
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureApplicationGatewayConfig** konfigurerar en Programgateway.

## BESKRIVS

### Exempel 1: Konfigurera en Programgateway genom att använda ett konfigurations objekt
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

Det första kommandot får konfigurationsobjektet för den Programgateway som heter ApplicationGateway02 med hjälp av cmdleten **Get-AzureApplicationGatewayConfig** .
Kommandot sparar det i $ConfigReturnObject variabel.

Det andra kommandot anger konfigurationen för programmet som heter ApplicationGateway06 genom att använda ett konfigurations objekt för Programgateway som lagras i $ConfigReturnObject variabeln.

### Exempel 2: Konfigurera en Programgateway genom att använda en konfigurations fil
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

Det här kommandot anger konfigurationen för programmet med namnet ApplicationGateway06 genom att använda en konfigurations fil för Programgateway på den angivna platsen.

### Exempel 3: ändra en konfiguration genom att använda ett konfigurations objekt
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

Det första kommandot får konfigurationsobjektet för den Programgateway som heter ApplicationGateway06 med hjälp av cmdleten **Get-AzureApplicationGatewayConfig** .
Kommandot sparar det i $ConfigReturnObject variabel.

Det andra kommandot tilldelar ett port värde till en **port** egenskap i objektet som lagras i $ConfigReturnObject.

Det sista kommandot skickar den uppdaterade $ConfigReturnObject till den aktuella cmdleten.

## MALLPARAMETRAR

### -Config
Anger ett konfigurations objekt för Programgateway.
Denna cmdlet tilldelar den konfiguration som den här parametern anger till en Programgateway.

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigFile
Anger sökvägen till en konfigurations fil i XML-format för en Programgateway.
Denna cmdlet tilldelar den konfiguration som den här parametern anger till en Programgateway.

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den Application Gateway som denna cmdlet konfigurerar.

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

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser. Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
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

### System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration

## VÄRDEN

### Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureApplicationGatewayConfig](./Get-AzureApplicationGatewayConfig.md)


