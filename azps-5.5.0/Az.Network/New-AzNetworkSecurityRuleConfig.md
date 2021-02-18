---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223726"
---
# New-AzNetworkSecurityRuleConfig

## SYNOPSIS
Skapar en konfiguration av en nätverkssäkerhetsregel.

## SYNTAX

### SetByResource (standard)
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzNetworkSecurityRuleConfig** skapar en konfiguration av nätverkssäkerhetsregel för Azure för en nätverkssäkerhetsgrupp.

## EXEMPEL

### Exempel 1: Skapa en nätverkssäkerhetsregel som tillåter RDP
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

Med det här kommandot skapas en säkerhetsregel som tillåter åtkomst från Internet till port 3389

### Exempel 2: Skapa en nätverkssäkerhetsregel som tillåter HTTP
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

Det här kommandot skapar en säkerhetsregel som tillåter åtkomst från Internet till port 80

## PARAMETERS

### -Access
Anger om nätverkstrafik är tillåten eller nekad.
De godtagbara värdena för den här parametern är: Tillåt och Neka.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

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

### -Beskrivning
Anger en beskrivning av konfigurationen av nätverkssäkerhetsregeln som ska skapas.

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

### -DestinationAddressPrefix
Anger ett måladressprefix.
De godtagbara värdena för den här parametern är:
- En CIDR-adress (Classless Interdomain Routing) 
- Ett IP-adressintervall för destinationen 
- Ett jokertecken (*) för att matcha en IP-adress Du kan använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroup
Programmets säkerhetsgrupp som angetts som mål för regeln. Det kan inte användas med parametern DestinationAddressPrefix.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroupId
Programmets säkerhetsgrupp som angetts som mål för regeln. Det kan inte användas med parametern DestinationAddressPrefix.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
Anger en målport eller ett målområde.
De godtagbara värdena för den här parametern är:
- Ett heltal
- Ett heltal mellan 0 och 65 535
- Ett jokertecken (*) som matchar en port

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Direction
Anger om en regel utvärderas för inkommande eller utgående trafik.
De godtagbara värdena för den här parametern är: Inkommande och utgående.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Anger namnet på konfigurationen av nätverkssäkerhetsregeln som cmdleten skapar.

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

### -Priority
Anger prioriteten för en regelkonfiguration.
De godtagbara värdena för den här parametern är: Ett heltal mellan 100 och 4096.
Prioritetsnumret måste vara unikt för varje regel i samlingen.
Ju lägre prioritetsnummer, desto högre prioritet gäller regeln.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Anger det nätverksprotokoll som en ny regelkonfiguration gäller för.
De godtagbara värdena för den här parametern är:
- Tcp
- Udp
- jokertecken (*) för att matcha båda.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
Anger ett källadressprefix.
De godtagbara värdena för den här parametern är:
- En CIDR
- Ett KÄLL-IP-intervall
- Ett jokertecken (*) som matchar en IP-adress.
Du kan också använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroup
Programsäkerhetsgruppen som angetts som källa för regeln. Det kan inte användas med parametern SourceAddressPrefix.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroupId
Programsäkerhetsgruppen som anges som källa för regeln. Det kan inte användas med parametern SourceAddressPrefix.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
Anger källporten eller källområdet.
De godtagbara värdena för den här parametern är:
- Ett heltal
- Ett heltal mellan 0 och 65 535
- Ett jokertecken (*) som matchar en port

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSSecurityrule

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


