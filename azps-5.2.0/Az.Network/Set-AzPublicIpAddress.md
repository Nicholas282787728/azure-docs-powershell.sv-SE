---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413067"
---
# Set-AzPublicIpAddress

## Sammanfattning
Uppdaterar en offentlig IP-adress.

## FRÅGESYNTAXEN

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzPublicIpAddress** uppdaterar en offentlig IP-adress.

## BESKRIVS

### 1: ändra tilldelnings metod för en offentlig IP-adress
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.
Andra kommando anger tilldelnings metod för det offentliga IP-adress-objektet till "statisk".
Set-AzPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet och ändrar tilldelnings metoden till "statisk". En offentlig IP-adress tilldelas omedelbart.

### 2: lägga till DNS-domännamn för en offentlig IP-adress
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.
Med det andra kommandot anges egenskapen DomainNameLabel till det obligatoriska DNS-prefixet.
Set-AzPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet. DomainNameLabel & FQDN ändras som förväntat.
    
### 3: ändra DNS-domännamn för en offentlig IP-adress
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Första kommandot får den offentliga IP-adressresursen med namnet $publicIPName i resurs gruppen $rgName.
Med det andra kommandot anges egenskapen DomainNameLabel till det obligatoriska DNS-prefixet.
Set-AzPublicIPAddress kommando uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet. DomainNameLabel & FQDN ändras som förväntat.

## MALLPARAMETRAR

### -AsJob
Kör cmdlet i bakgrunden

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
Anger ett offentlig IP-adress-objekt som representerar tillståndet som den offentliga IP-adressen ska anges för.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[New-AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


