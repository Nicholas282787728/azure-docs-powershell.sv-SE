---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: d78e4d8e84508e9a737bb15dc31b0dad1c9bdedc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929645"
---
# Set-AzureRmPublicIpAddress

## Sammanfattning
Anger mål tillstånd för en offentlig IP-adress.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmPublicIpAddress** anger mål tillståndet för en offentlig IP-adress.

## BESKRIVS

### 1: ändra tilldelnings metod för en offentlig IP-adress
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.
Andra kommando anger tilldelnings metod för det offentliga IP-adress-objektet till "statisk".
Set-AzureRmPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet och ändrar tilldelnings metoden till "statisk". En offentlig IP-adress tilldelas omedelbart.

### 2: ändra DNS-domännamn för en offentlig IP-adress
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.
Med det andra kommandot anges egenskapen DomainNameLabel till det obligatoriska DNS-prefixet.
Set-AzureRmPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet. DomainNameLabel & FQDN ändras som förväntat.

## MALLPARAMETRAR

### -AsJob
Kör cmdlet i bakgrunden

```yaml
Type: SwitchParameter
Parameter Sets: (All)
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

### -PublicIpAddress
Anger ett **PublicIpAddress** -objekt som representerar mål tillståndet som den offentliga IP-adressen ska anges för.

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### PSPublicIpAddress
Parametern ' PublicIpAddress ' godkänner värdet av typen ' PSPublicIpAddress ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmPublicIpAddress](./Get-AzureRmPublicIpAddress.md)

[New-AzureRmPublicIpAddress](./New-AzureRmPublicIpAddress.md)

[Remove-AzureRmPublicIpAddress](./Remove-AzureRmPublicIpAddress.md)


