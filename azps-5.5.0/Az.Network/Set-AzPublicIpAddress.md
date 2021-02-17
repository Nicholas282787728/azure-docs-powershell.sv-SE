---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227422"
---
# Set-AzPublicIpAddress

## SYNOPSIS
Uppdaterar en offentlig IP-adress.

## SYNTAX

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Set-AzPublicIpAddress** uppdaterar en offentlig IP-adress.

## EXEMPEL

### 1: Ändra tilldelningsmetod för en offentlig IP-adress
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Första kommandot hämtar den offentliga IP-adressresursen med $publicIPName namn i resursgruppen $rgName.
Det andra kommandot anger tilldelningsmetoden för det offentliga IP-adressobjektet till "Statisk".
Set-AzPublicIPAddress uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet och ändrar tilldelningsmetoden till Statisk. En offentlig IP-adress tilldelas omedelbart.

### 2: Lägg till DNS-domänetiketten för en offentlig IP-adress
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Första kommandot hämtar den offentliga IP-adressresursen med $publicIPName namn i resursgruppen $rgName.
Det andra kommandot anger egenskapen DomainNameLabel till ett obligatoriskt dns-prefix.
Set-AzPublicIPAddress uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet. DomainNameLabel & Fqdn ändras som förväntat.
    
### 3: Ändra DNS-domänetiketten för en offentlig IP-adress
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Första kommandot hämtar den offentliga IP-adressresursen med $publicIPName namn i resursgruppen $rgName.
Det andra kommandot anger egenskapen DomainNameLabel till ett obligatoriskt dns-prefix.
Set-AzPublicIPAddress uppdaterar den offentliga IP-adressresursen med det uppdaterade objektet. DomainNameLabel & Fqdn ändras som förväntat.

## PARAMETERS

### -As Ent
Kör cmdleten i bakgrunden

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
Anger ett offentligt IP-adressobjekt som representerar det tillstånd som den offentliga IP-adressen ska anges till.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[New-AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


