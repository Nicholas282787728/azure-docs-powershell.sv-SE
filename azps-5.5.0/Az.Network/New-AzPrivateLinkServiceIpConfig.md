---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: 94375ba7d54095af131d7a61c7b06d50e2ba9521
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218431"
---
# New-AzPrivateLinkServiceIpConfig

## SYNOPSIS
Skapa en ip-konfiguration för en privat länktjänst.

## SYNTAX

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten New-AzPrivateLinkServiceIpConfig** skapar en ip-konfiguration för privat länktjänst. Den här konfigurationen används för att käll-NAT-ing för inkommande trafik från privat slutpunkt. 

## EXEMPEL

### Exempel 1
```powershell
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

I det här exemplet skapas en ip-konfiguration av en privat länktjänst i minnet.

### Exempel 2

Skapa en ip-konfiguration för en privat länktjänst. (autogenererat)

<!-- Aladdin Generated Example -->
```powershell
New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -PrivateIpAddress '10.0.0.5' -Subnet <PSSubnet>
```

## PARAMETERS

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

### -Name
Namnet på IpConfiguration

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddress
Ip-adressen för privat ipConfiguration om statisk tilldelning anges.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddressVersion
IP-versionen av ip-konfigurationen

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Primary
Ange att aktuell ip-konfiguration är primär eller inte.

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

### -Subnet
Undernät

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzPrivateLinkService](./New-AzPrivateLinkService.md)