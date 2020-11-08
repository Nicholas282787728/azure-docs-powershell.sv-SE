---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093391"
---
# Get-AzureApplicationGatewayConfig

## Sammanfattning
Hämtar en konfigurations kontext för Programgateway.

## FRÅGESYNTAXEN

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureApplicationGatewayConfig** hämtar en konfigurations kontext för Azure Application Gateway.
En kontext innehåller både ett konfigurations objekt och en XML-konfiguration.
Du kan spara XML-konfigurationen i en fil.

## BESKRIVS

### Exempel 1: Hämta en konfiguration för Programgateway och spara den i en fil
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

Det här kommandot hämtar konfigurationen för en Programgateway som heter ApplicationGateway06.
Kommandot sparar det i filen på den angivna sökvägen.

## MALLPARAMETRAR

### -ExportToFile
Anger en fil Sök väg som den här cmdleten sparar konfigurationen i XML-format för.

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

### -Namn
Anger namnet på den Programgateway för vilken denna cmdlet hämtar konfigurations information.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

## VÄRDEN

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzureApplicationGatewayConfig](./Set-AzureApplicationGatewayConfig.md)


