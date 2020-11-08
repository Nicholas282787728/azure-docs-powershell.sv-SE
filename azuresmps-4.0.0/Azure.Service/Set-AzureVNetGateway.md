---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099644"
---
# Set-AzureVNetGateway

## Sammanfattning
Aktiverar eller inaktiverar en VPN-gateway för ett Azure Virtual Network.

## FRÅGESYNTAXEN

### Anslut (standard)
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Koppla ner
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureVNetGateway** aktiverar eller inaktiverar ett virtuellt privat nätverk (VPN) för ett Azure Virtual Network.
En virtuell nätverksgateway är en VPN-slutpunkt för att ansluta till ett virtuellt nätverk.
Ange parametern *Connect* eller *Connect* för att aktivera eller inaktivera VPN-anslutningen mellan en lokal nätverks webbplats och ett virtuellt nätverk.

## BESKRIVS

### Exempel 1: Aktivera en virtuell nätverksgateway för ett virtuellt nätverk
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Det här kommandot aktiverar den virtuella Nätverksgatewayen mellan det virtuella Azure-nätverket med namnet ContosoProdNet och VPN-enheten för den lokala nätverks platsen med namnet ContosoBranchOffice.

### Exempel 2: inaktivera en virtuell nätverksgateway för ett virtuellt nätverk
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Det här kommandot inaktiverar den virtuella Nätverksgatewayen mellan det virtuella Azure-nätverket som heter ContosoProdNet och VPN-enheten för den lokala nätverks platsen med namnet ContosoBranchOffice.

## MALLPARAMETRAR

### -Anslut
Anger att denna cmdlet aktiverar VPN-anslutningen mellan ett virtuellt nätverk och en lokal nätverks webbplats.

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Koppla ner
Anger att denna cmdlet inaktiverar VPN-anslutningen mellan ett virtuellt nätverk och en lokal nätverks webbplats.

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalNetworkSiteName
Anger namnet på den lokala nätverks platsen där denna cmdlet aktiverar eller inaktiverar VPN-anslutningen.

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

### -VNetName
Anger det virtuella nätverk som denna cmdlet aktiverar eller inaktiverar VPN-anslutningen för.

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

[Get-AzureVNetGateway](./Get-AzureVNetGateway.md)

[New-AzureVNetGateway](./New-AzureVNetGateway.md)

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Ändra storlek – AzureVNetGateway](./Resize-AzureVNetGateway.md)


