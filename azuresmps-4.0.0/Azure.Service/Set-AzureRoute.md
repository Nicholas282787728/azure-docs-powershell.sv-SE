---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099053"
---
# Set-AzureRoute

## Sammanfattning
Skapar en väg i en routningstabell.

## FRÅGESYNTAXEN

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRoute** skapar en väg i en routningstabell.
Den nya vägen börjar gälla nästan omedelbart på de virtuella datorerna som är kopplade till väg tabellen.

## BESKRIVS

### Exempel 1: lägga till en virtuell enhet nästa hopp väg
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

Det här kommandot skapar en routningstabell som heter ApplianceRouteTable på den angivna platsen.
Kommandot skickar den väg tabellen till den aktuella cmdleten.
Den aktuella cmdleten lägger till en väg med namnet ApplianceRoute03, som är en VirtualAppliance nästa hopp typ.
Kommandot anger nästa hopp-IP-adress och adressprefixet för vägen.

### Exempel 2: lägga till en Internet-routning nästa hopp
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

Det här kommandot får en routningstabell med namnet ApplianceRouteTable.
Kommandot skickar den väg tabellen till den aktuella cmdleten.
Den aktuella cmdleten lägger till en väg som heter InternetRoute, som är en typ av Internet hopp.
Kommandot anger adressprefixet för vägen.

## MALLPARAMETRAR

### -AddressPrefix
Anger ett adressprefix för den nya vägen.

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

### -NextHopIpAddress
Anger IP-adressen för den enhet som är nästa hopp för trafik som använder vägen.
Ange bara det här värdet om du anger ett värde för VirtualAppliance för parametern *NextHopType* .

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

### -NextHopType
Anger nästa hopp typ för trafik som använder vägen.
Giltiga värden är: 

- VPNGateway
- VNETLocal
- Internet
- VirtualAppliance
- Kan

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

### -RouteName
Anger ett namn för den nya vägen som läggs till av denna cmdlet.

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

### -RouteTable
Anger den routningstabell till vilken denna cmdlet lägger till det nya flödet.

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Remove-AzureRoute](./Remove-AzureRoute.md)


