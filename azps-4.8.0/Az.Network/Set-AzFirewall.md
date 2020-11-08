---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262503"
---
# Set-AzFirewall

## Sammanfattning
Sparar en modifierad brand vägg.

## FRÅGESYNTAXEN

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzFirewall** uppdaterar en Azure Firewall.

## BESKRIVS

### 1: uppdatera prioritet för en regel samling för en brand Väggs program
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

Det här exemplet uppdaterar prioriteten för en befintlig regel samling av en Azure-brandvägg.
Om du antar Azure Firewall "AzureFirewall" i resurs gruppen "RG" innehåller en program regel samling med namnet "ruleCollectionName", kommer de ovanstående kommandona att ändra prioriteten för den regel samlingen och uppdatera Azure Firewall efteråt. Utan kommandot Set-AzFirewall återspeglas inte alla åtgärder som utförs på det lokala $azFw-objektet på servern.

### 2: skapa en Azure-brandvägg och konfigurera en samling med program regler senare
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

I det här exemplet skapas en brand vägg först utan några program regel samlingar. Därefter skapas en program regel-och program regel samling, och därefter ändras brand Väggs objekt i minnet utan att det påverkar den verkliga konfigurationen i molnet. Set-AzFirewall måste anropas för att ändringarna ska synas i molnet.

### 3: uppdatera hotet Intels arbets läge i Azure Firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

I det här exemplet uppdateras hotet Intels arbets läge för Azure Firewall "AzureFirewall" i resurs gruppen "RG".
Utan kommandot Set-AzFirewall återspeglas inte alla åtgärder som utförs på det lokala $azFw-objektet på servern.

### 4: frigöra och tilldela brand väggen
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
I det här exemplet hämtas en brand vägg, avsätter brand väggen och sparar den. Kommandot frigör tar bort den aktiva tjänsten men bevarar brand väggens konfiguration. Set-AzFirewall måste anropas för att ändringarna ska synas i molnet.
Om användaren vill starta tjänsten igen ska metoden allocate anropas i brand väggen.
Den nya VNet-och offentlige tjänsten måste finnas i samma resurs grupp som brand väggen. För att ändringarna ska synas i molnet måste Set-AzFirewall anropas.

### 5: tilldela med en offentlig IP-adress för hantering av tvingande tunnel scenarion
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
I det här exemplet allokeras brand väggen med en offentlig IP-adress och undernät för tvingande tunnlar. VNet måste innehålla ett undernät som heter "AzureFirewallManagementSubnet".

### 6: lägga till en offentlig IP-adress i en Azure-brandvägg
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

I det här exemplet är den offentliga IP-adressen "azFwPublicIp1" enligt brand väggen.

### 7: ta bort en offentlig IP-adress från en Azure-brandvägg
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

I det här exemplet är den offentliga IP-adressen "azFwPublicIp1" som frånkopplad från brand väggen.

### 8: ändra den offentliga Management-IP-adressen i en Azure-brandvägg
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

I det här exemplet ändras brand väggens offentliga IP-adress för hanteringen till "AzFwMgmtPublicIp2"

### 9: lägga till DNS-konfiguration till en Azure-brandvägg
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

I det här exemplet är DNS-proxy och DNS-serverkonfiguration anslutna till brand väggen.

### 10: uppdatera destinationen för en befintlig regel i en regel samling för en brand Väggs program
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

Det här exemplet uppdaterar destinationen för en befintlig regel i en regel samling av en Azure-brandvägg. Då kan du automatiskt uppdatera reglerna när IP-adresser ändras dynamiskt.

### 11: Tillåt Active FTP på Azure Firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

I det här exemplet tillåts Active FTP på brand väggen.

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

### -AzureFirewall
AzureFirewall

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

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

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
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Networks. Models. PSAzureFirewall

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSAzureFirewall

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
