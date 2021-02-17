---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226094"
---
# Add-AzNetworkSecurityRuleConfig

## SYNOPSIS
Lägger till en konfiguration av en nätverkssäkerhetsregel i en nätverkssäkerhetsgrupp.

## SYNTAX

### SetByResource (standard)
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Add-AzNetworkSecurityRuleConfig** lägger till en konfiguration av nätverkssäkerhetsregel i en Azure-nätverkssäkerhetsgrupp.

## EXEMPEL

### 1: Lägga till en nätverkssäkerhetsgrupp
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

Det första kommandot hämtar en Azure-nätverkssäkerhetsgrupp med namnet "nsg1" från resursgruppen "rg1". Det andra kommandot lägger till en nätverkssäkerhetsregel med namnet "rdp-regel" som tillåter trafik från Internet till port 3389 till det hämtade nätverkssäkerhetsgruppsobjektet. Beständiga den modifierade Azure-nätverkssäkerhetsgruppen.

### 2: Lägga till en ny säkerhetsregel med programsäkerhetsgrupper
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

Först skapar vi två nya programsäkerhetsgrupper. Därefter hämtar vi azure-nätverkssäkerhetsgruppen "nsg1" från resursgruppen "rg1". och lägger till en nätverkssäkerhetsregel med namnet "rdp-regel" i den. Regeln tillåter trafik från alla IP-konfigurationer i programsäkerhetsgruppen "srcAsg" till alla IP-konfigurationer i "destAsg" i port 3389. När vi har lagt till regeln beständiga vi den ändrade Azure-nätverkssäkerhetsgruppen.

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
Anger en beskrivning av en konfiguration av en nätverkssäkerhetsregel.

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
Anger namnet på en konfiguration av en nätverkssäkerhetsregel.

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
Anger ett **NetworkSecurityGroup-objekt.**
Den här cmdleten lägger till en konfiguration av nätverkssäkerhetsregeln för objektet som den här parametern anger.

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
De godtagbara värdena för den här parametern är: ett heltal mellan 100 och 4096.
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
De godtagbara värdena för den här parametern är:
- Tcp
- Udp
- Jokertecken (*) för att matcha båda

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
Programsäkerhetsgruppen som angetts som källa för regeln. Det kan inte användas med parametern SourceAddressPrefix.

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
Anger en källport eller ett källområde.
Det här värdet uttrycks som ett heltal, som ett intervall mellan 0 och 65535 eller som ett jokertecken (*) för att matcha en källport.

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

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


