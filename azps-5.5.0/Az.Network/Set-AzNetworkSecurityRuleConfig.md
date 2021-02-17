---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236494"
---
# Set-AzNetworkSecurityRuleConfig

## SYNOPSIS
Uppdaterar en konfiguration av en nätverkssäkerhetsregel för en nätverkssäkerhetsgrupp.

## SYNTAX

### SetByResource (standard)
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzNetworkSecurityRuleConfig** uppdaterar en konfiguration av nätverkssäkerhetsregel för en nätverkssäkerhetsgrupp.

## EXEMPEL

### Exempel 1: Ändra åtkomstkonfigurationen i en nätverkssäkerhetsregel
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

Det första kommandot får nätverkssäkerhetsgruppen NSG-FrontEnd och lagrar den sedan i den variabla $nsg.
Det andra kommandot använder pipelineoperatorn för att överföra säkerhetsgruppen i $nsg till Get-AzNetworkSecurityRuleConfig, som hämtar säkerhetsregelkonfigurationen med namnet rdp-regel.
Det tredje kommandot ändrar åtkomstkonfigurationen av rdp-regeln till Neka.

### Exempel 2

Uppdaterar en konfiguration av en nätverkssäkerhetsregel för en nätverkssäkerhetsgrupp. (autogenererat)

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## PARAMETERS

### -Access
Anger om nätverkstrafik är tillåten eller nekad. De godtagbara värdena för den här parametern är: Tillåt och Neka.

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
Anger en beskrivning för en regelkonfiguration.
Maxstorleken är 140 tecken.

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
- Ett MÅL-IP-adressintervall 
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
Den programsäkerhetsgrupp som angetts som mål för regeln. Det kan inte användas med parametern DestinationAddressPrefix.

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
Anger namnet på konfigurationen av nätverkssäkerhetsregeln som den här cmdleten anger.

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

### -NetworkSecurityGroup
Anger det **NetworkSecurityGroup-objekt** som innehåller den konfiguration av nätverkssäkerhetsregeln som ska ställas in.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Priority
Anger prioriteten för en regelkonfiguration.
De godtagbara värdena för den här parametern är:Ett heltal mellan 100 och 4096.
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
Anger det nätverksprotokoll som en regelkonfiguration gäller för.
De godtagbara värdena för den här parametern är: --Tcp
- Udp
- Ett jokertecken (*) som matchar båda

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
- Ett jokertecken (*) för att matcha en IP-adress Du kan också använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.

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

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)


