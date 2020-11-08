---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099040"
---
# Set-AzureVNetGatewayKey

## Sammanfattning
Ställer in den fördelade nyckeln för anslutningen mellan en Azure VPN-gateway och en lokal nätverks webbplats.

## FRÅGESYNTAXEN

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureVNetGatewayKey** anger den fördelade nyckeln för anslutningen mellan en virtuell Azure-Gateway (VPN) och en lokal nätverks webbplats.
Nyckeln måste vara lika med nyckeln som har kon figurer ATS på den lokala nätverks platsens Gateway.
Om nycklarna inte matchar kan ingen anslutning upprättas.

## BESKRIVS

## MALLPARAMETRAR

### -LocalNetworkSiteName
Anger namnet på den lokala nätverks platsen som ansluter till den virtuella Nätverksgatewayen.

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

### -SharedKey
Anger den delade nyckeln som ska kopplas till VPN gateway.
Värdet måste vara en alpha-numerisk sträng som inte är längre än 128 tecken.

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

### -VNetName
Anger det virtuella nätverk som den här cmdleten ställer in den delade nycklar för.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureVNetGatewayKey](./Get-AzureVNetGatewayKey.md)


