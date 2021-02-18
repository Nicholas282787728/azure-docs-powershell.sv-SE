---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 1ab3d82b494d5598081ea229a7ae50d486b8ca20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223590"
---
# Set-AzFirewall

## SYNOPSIS
Sparar en ändrad brandvägg.

## SYNTAX

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzFirewall** uppdaterar en Azure-brandvägg.

## EXEMPEL

### 1: Uppdatera prioriteten för en regelsamling för brandväggsprogram
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

Det här exemplet uppdaterar prioriteten för en befintlig regelsamling i en Azure-brandvägg.
Om vi antar att Azure-brandväggen "AzureFirewall" i resursgruppen "rg" innehåller en programregelsamling med namnet "ruleCollectionName" ändrar kommandona ovan prioriteten för den regelsamlingen och uppdaterar Azure-brandväggen efteråt. Utan kommandot Set-AzFirewall inte alla åtgärder som utförs på det $azFw objektet på servern.

### 2: Skapa en Azure-brandvägg och konfigurera en samling med programregel senare
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

I det här exemplet skapas en brandvägg först utan några programregelsamlingar. Därefter skapas en programregel och en programregelsamling och sedan ändras brandväggsobjektet i minnet, utan att den faktiska konfigurationen i molnet påverkas. Ändringar som ska återspeglas i molnet Set-AzFirewall anropas.

### 3: Uppdateringsläge för Intel-drift av Azure-brandväggen
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

Det här exemplet uppdaterar åtgärdsläget Threat Intel för Azure-brandväggen "AzureFirewall" i resursgruppen "rg".
Utan kommandot Set-AzFirewall inte alla åtgärder som utförs på det $azFw objektet på servern.

### 4: Avtala och tilldela brandväggen
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
I det här exemplet hämtas en brandvägg, brandväggen lokaliseras och sparas. Kommandot Deallocate tar bort tjänsten som körs men behåller brandväggens konfiguration. Ändringar som ska återspeglas i molnet Set-AzFirewall anropas.
Om användaren vill starta tjänsten igen bör tilldelad metod anropas i brandväggen.
Det nya VNet och offentliga IP-adressen måste finnas i samma resursgrupp som brandväggen. För att ändringar ska återspeglas i molnet måste Set-AzFirewall anropas.

### 5: Tilldela med en offentlig IP-adress för hantering av scenarier med tvingad tunnel
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
Det här exemplet avsätter brandväggen med en offentlig IP-adress för hantering och undernät för tvingade tunnlar. VNet måste innehålla ett undernät som kallas "AzureFirewallManagementSubnet".

### 6: Lägga till en offentlig IP-adress i en Azure-brandvägg
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

I det här exemplet ska den offentliga IP-adressen "azFwPublicIp1" kopplas till brandväggen.

### 7: Ta bort en offentlig IP-adress från en Azure-brandvägg
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

I det här exemplet är den offentliga IP-adressen "azFwPublicIp1" frånkopplad från brandväggen.

### 8: Ändra den offentliga IP-adressen för hantering i en Azure-brandvägg
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

I det här exemplet ändras den offentliga IP-adressen för hanteringen av brandväggen till "AzFwMgmtPublicIp2"

### 9: Lägga till DNS-konfiguration i en Azure-brandvägg
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

I det här exemplet är DNS-proxy och DNS-serverkonfiguration kopplad till brandväggen.

### 10: Uppdatera målet för en befintlig regel i en brandväggsprogramregelsamling
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

Det här exemplet uppdaterar destinationen för en befintlig regel i en regelsamling i en Azure-brandvägg. På så sätt kan du uppdatera dina regler automatiskt när IP-adresser ändras dynamiskt.

### 11: Tillåt aktiv FTP i Azure-brandväggen
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

I det här exemplet tillåts Aktiv FTP i brandväggen.

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

### -AzureFirewall
The AzureFirewall

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
