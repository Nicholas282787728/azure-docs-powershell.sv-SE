---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 031c926d25fe55a9572fe12922ccee26b6371a2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271563"
---
# <span data-ttu-id="1af7d-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1af7d-101">New-AzFirewall</span></span>

## <span data-ttu-id="1af7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1af7d-102">SYNOPSIS</span></span>
<span data-ttu-id="1af7d-103">Skapar en ny brand vägg i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1af7d-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="1af7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1af7d-104">SYNTAX</span></span>

### <span data-ttu-id="1af7d-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="1af7d-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1af7d-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="1af7d-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1af7d-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="1af7d-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1af7d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1af7d-108">DESCRIPTION</span></span>
<span data-ttu-id="1af7d-109">Cmdleten **New-AzFirewall** skapar en Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="1af7d-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="1af7d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1af7d-110">EXAMPLES</span></span>

### <span data-ttu-id="1af7d-111">Exempel 1: skapa en brand vägg som är ansluten till ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="1af7d-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="1af7d-112">I det här exemplet skapas en brand vägg som är kopplad till det virtuella nätverket "VNet" i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="1af7d-113">Eftersom inga regler angavs blockerar brand väggen all trafik (standard beteende).</span><span class="sxs-lookup"><span data-stu-id="1af7d-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="1af7d-114">Hotet Intel körs också i standard läge – varning – vilket innebär att illvillig trafik loggas, men inte nekas.</span><span class="sxs-lookup"><span data-stu-id="1af7d-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="1af7d-115">Exempel 2: skapa en brand vägg som tillåter all HTTPS-trafik</span><span class="sxs-lookup"><span data-stu-id="1af7d-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="1af7d-116">I det här exemplet skapas en brand vägg som tillåter all HTTPS-trafik på port 443.</span><span class="sxs-lookup"><span data-stu-id="1af7d-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="1af7d-117">Hotet Intel körs i standard läge – varning-vilket innebär att illvillig trafik loggas, men inte nekas.</span><span class="sxs-lookup"><span data-stu-id="1af7d-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="1af7d-118">Exempel 3: DNAT-omdirigera trafik till 10.1.2.3:80 till 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="1af7d-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="1af7d-119">I det här exemplet skapas en brand vägg som översatte mål-IP och port för alla paket som är avsedda att 10.1.2.3:80 till 10.2.3.4:8080 Threat Intel är inaktiverat i det här exemplet.</span><span class="sxs-lookup"><span data-stu-id="1af7d-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="1af7d-120">Exempel 4: skapa en brand vägg utan regler och med hotet Intels i aviserings läge</span><span class="sxs-lookup"><span data-stu-id="1af7d-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="1af7d-121">I det här exemplet skapas en brand vägg som blockerar all trafik (standard beteende) och har hotet att Intel körs i aviserings läget.</span><span class="sxs-lookup"><span data-stu-id="1af7d-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="1af7d-122">Detta innebär att aviserings loggar släpps för illvillig trafik innan de andra reglerna tillämpas (i det här fallet är standard regeln-neka alla)</span><span class="sxs-lookup"><span data-stu-id="1af7d-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="1af7d-123">Exempel 5: skapa en brand vägg som tillåter all HTTP-trafik på Port 8080, men blockerar skadlig domän identifieras av Threat Intel</span><span class="sxs-lookup"><span data-stu-id="1af7d-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="1af7d-124">I det här exemplet skapas en brand vägg som tillåter all HTTP-trafik på Port 8080 såvida den inte betraktas som skadlig för Threat Intel.</span><span class="sxs-lookup"><span data-stu-id="1af7d-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="1af7d-125">När du kör i läget neka, till skillnad mot varning, loggas inte den trafik som anses vara skadlig via Intel, men även blockeras.</span><span class="sxs-lookup"><span data-stu-id="1af7d-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="1af7d-126">Exempel 6: skapa en brand vägg utan regler och med tillgänglighets zoner</span><span class="sxs-lookup"><span data-stu-id="1af7d-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="1af7d-127">I det här exemplet skapas en brand vägg med alla tillgängliga tillgänglighets zoner.</span><span class="sxs-lookup"><span data-stu-id="1af7d-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="1af7d-128">Exempel 7: skapa en brand vägg med två eller fler offentliga IP-adresser</span><span class="sxs-lookup"><span data-stu-id="1af7d-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="1af7d-129">I det här exemplet skapas en brand vägg som är ansluten till virtuellt nätverk (VNet) med två offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="1af7d-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="1af7d-130">Exempel 8: skapa en brand vägg som möjliggör MSSQL-trafik till specifik SQL-databas</span><span class="sxs-lookup"><span data-stu-id="1af7d-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="1af7d-131">I det här exemplet skapas en brand vägg som tillåter MSSQL-trafik på standard porten 1433 till SQL-sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="1af7d-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="1af7d-132">Exempel 9: skapa en brand vägg som är kopplad till ett virtuellt nav</span><span class="sxs-lookup"><span data-stu-id="1af7d-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -SkuName AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="1af7d-133">I det här exemplet skapas en brand vägg som är ansluten till virtuella hubben "vHub".</span><span class="sxs-lookup"><span data-stu-id="1af7d-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="1af7d-134">En brand Väggs princip $fp kopplas till brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="1af7d-135">Denna brand vägg tillåter/nekar trafiken baserat på reglerna som nämns i brand Väggs principens $fp.</span><span class="sxs-lookup"><span data-stu-id="1af7d-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="1af7d-136">Det virtuella navet och brand väggen bör vara i samma regioner.</span><span class="sxs-lookup"><span data-stu-id="1af7d-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="1af7d-137">Exempel 10: skapa en brand vägg med Lägg för hot intelligens</span><span class="sxs-lookup"><span data-stu-id="1af7d-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="1af7d-138">I det här exemplet skapas en brand vägg som Lägg "www.microsoft.com" och "8.8.8.8" från Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="1af7d-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="1af7d-139">Exempel 11: skapa en brand vägg med anpassade inställningar för privat område</span><span class="sxs-lookup"><span data-stu-id="1af7d-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="1af7d-140">I det här exemplet skapas en brand vägg som hanterar "99.99.99.0/24" och "66.66.0.0/16" som privata IP-adressintervall och inte är med i trafik till dessa adresser</span><span class="sxs-lookup"><span data-stu-id="1af7d-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="1af7d-141">Exempel 12: skapa en brand vägg med ett hanterings nät och en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="1af7d-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="1af7d-142">I det här exemplet skapas en brand vägg som är kopplad till det virtuella nätverket "VNet" i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="1af7d-143">Eftersom inga regler angavs blockerar brand väggen all trafik (standard beteende).</span><span class="sxs-lookup"><span data-stu-id="1af7d-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="1af7d-144">Hotet Intel körs också i standard läge – varning – vilket innebär att illvillig trafik loggas, men inte nekas.</span><span class="sxs-lookup"><span data-stu-id="1af7d-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="1af7d-145">För att stödja upptvingade tunnlar-scenarion använder den här brand väggen under nätet "AzureFirewallManagementSubnet" och den offentliga hanterings-IP-adressen för dess hanterings trafik</span><span class="sxs-lookup"><span data-stu-id="1af7d-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="1af7d-146">Exempel 13: skapa en brand vägg med brand Väggs princip som är ansluten till ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="1af7d-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="1af7d-147">I det här exemplet skapas en brand vägg som är kopplad till det virtuella nätverket "VNet" i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="1af7d-148">Reglerna och hotets intelligens som kommer att tillämpas på brand väggen hämtas från brand Väggs principen</span><span class="sxs-lookup"><span data-stu-id="1af7d-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="1af7d-149">Exempel 14: skapa en brand vägg med DNS-proxy och DNS-servrar</span><span class="sxs-lookup"><span data-stu-id="1af7d-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="1af7d-150">I det här exemplet skapas en brand vägg som är kopplad till det virtuella nätverket "VNet" i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="1af7d-151">DNS-proxy är aktiverat för den här brand väggen och två DNS-servrar tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="1af7d-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="1af7d-152">Dessutom krävs DNS-proxy för nätverks regler så om det finns nätverks regler med FQDN: er används DNS-proxy också för dem.</span><span class="sxs-lookup"><span data-stu-id="1af7d-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="1af7d-153">Exempel 15: skapa en brand vägg med flera IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="1af7d-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="1af7d-154">Brand väggen kan associeras med det virtuella navet</span><span class="sxs-lookup"><span data-stu-id="1af7d-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -SkuName AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="1af7d-155">I det här exemplet skapas en brand vägg som är ansluten till virtuellt nav (hub) i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="1af7d-156">Brand väggen tilldelas två offentliga IP-adresser som har skapats implicit.</span><span class="sxs-lookup"><span data-stu-id="1af7d-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="1af7d-157">16: skapa en brand vägg med Tillåt aktiv FTP.</span><span class="sxs-lookup"><span data-stu-id="1af7d-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="1af7d-158">I det här exemplet skapas en brand vägg med flaggan Tillåt Active FTP.</span><span class="sxs-lookup"><span data-stu-id="1af7d-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="1af7d-159">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1af7d-159">PARAMETERS</span></span>

### <span data-ttu-id="1af7d-160">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="1af7d-160">-AllowActiveFTP</span></span>
<span data-ttu-id="1af7d-161">Tillåter Active FTP i brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-161">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="1af7d-162">Den är som standard inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="1af7d-162">By default it is disabled.</span></span>


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

### <span data-ttu-id="1af7d-163">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1af7d-163">-ApplicationRuleCollection</span></span>
<span data-ttu-id="1af7d-164">Anger program reglerna för den nya brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-164">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1af7d-165">-AsJob</span></span>
<span data-ttu-id="1af7d-166">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1af7d-166">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1af7d-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af7d-167">-DefaultProfile</span></span>
<span data-ttu-id="1af7d-168">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1af7d-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1af7d-169">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="1af7d-169">-DnsServer</span></span>
<span data-ttu-id="1af7d-170">Listan med DNS-servrar som ska användas för DNS-matchning,</span><span class="sxs-lookup"><span data-stu-id="1af7d-170">The list of DNS Servers to be used for DNS resolution,</span></span>

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

### <span data-ttu-id="1af7d-171">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="1af7d-171">-EnableDnsProxy</span></span>
<span data-ttu-id="1af7d-172">Aktivera DNS-proxy.</span><span class="sxs-lookup"><span data-stu-id="1af7d-172">Enable DNS Proxy.</span></span> <span data-ttu-id="1af7d-173">Den är som standard inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="1af7d-173">By default it is disabled.</span></span>


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

### <span data-ttu-id="1af7d-174">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="1af7d-174">-FirewallPolicyId</span></span>
<span data-ttu-id="1af7d-175">Brand Väggs principen ansluten till brand väggen</span><span class="sxs-lookup"><span data-stu-id="1af7d-175">The firewall policy attached to the firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-176">-Force</span><span class="sxs-lookup"><span data-stu-id="1af7d-176">-Force</span></span>
<span data-ttu-id="1af7d-177">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1af7d-177">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1af7d-178">-HubIPAddress</span><span class="sxs-lookup"><span data-stu-id="1af7d-178">-HubIPAddress</span></span>
<span data-ttu-id="1af7d-179">IP-adresserna för den brand vägg som är ansluten till ett virtuellt nav</span><span class="sxs-lookup"><span data-stu-id="1af7d-179">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-180">-Plats</span><span class="sxs-lookup"><span data-stu-id="1af7d-180">-Location</span></span>
<span data-ttu-id="1af7d-181">Anger området för brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-181">Specifies the region for the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-182">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1af7d-182">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="1af7d-183">En eller flera offentliga IP-adresser som ska användas för hanterings trafik.</span><span class="sxs-lookup"><span data-stu-id="1af7d-183">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="1af7d-184">De offentliga IP-adresserna måste använda standard-SKU och måste tillhöra samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-184">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-185">-Namn</span><span class="sxs-lookup"><span data-stu-id="1af7d-185">-Name</span></span>
<span data-ttu-id="1af7d-186">Anger namnet på den Azure Firewall som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="1af7d-186">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-187">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1af7d-187">-NatRuleCollection</span></span>
<span data-ttu-id="1af7d-188">Listan med AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="1af7d-188">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-189">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1af7d-189">-NetworkRuleCollection</span></span>
<span data-ttu-id="1af7d-190">Listan med AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="1af7d-190">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-191">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="1af7d-191">-PrivateRange</span></span>
<span data-ttu-id="1af7d-192">De privata IP-adresser som trafik inte SNAT'ed</span><span class="sxs-lookup"><span data-stu-id="1af7d-192">The private IP ranges to which traffic won't be SNAT'ed</span></span>

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

### <span data-ttu-id="1af7d-193">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1af7d-193">-PublicIpAddress</span></span>
<span data-ttu-id="1af7d-194">En eller flera offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="1af7d-194">One or more Public IP Addresses.</span></span> <span data-ttu-id="1af7d-195">De offentliga IP-adresserna måste använda standard-SKU och måste tillhöra samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-195">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-196">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="1af7d-196">-PublicIpName</span></span>
<span data-ttu-id="1af7d-197">Offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="1af7d-197">Public Ip Name.</span></span> <span data-ttu-id="1af7d-198">Den offentliga IP-adressen måste använda standard-SKU och måste tillhöra samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-198">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af7d-199">-ResourceGroupName</span></span>
<span data-ttu-id="1af7d-200">Anger namnet på en resurs grupp som ska innehålla brand väggen.</span><span class="sxs-lookup"><span data-stu-id="1af7d-200">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-201">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1af7d-201">-SkuName</span></span>
<span data-ttu-id="1af7d-202">SKU-namnet för brand väggen</span><span class="sxs-lookup"><span data-stu-id="1af7d-202">The sku name for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Sku
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-203">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="1af7d-203">-SkuTier</span></span>
<span data-ttu-id="1af7d-204">SKU-nivån för brand vägg</span><span class="sxs-lookup"><span data-stu-id="1af7d-204">The sku tier for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-205">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1af7d-205">-Tag</span></span>
<span data-ttu-id="1af7d-206">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1af7d-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1af7d-207">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="1af7d-207">For example:</span></span>

<span data-ttu-id="1af7d-208">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="1af7d-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="1af7d-209">-ThreatIntelMode</span></span>
<span data-ttu-id="1af7d-210">Anger åtgärds läget för Threat intelligence.</span><span class="sxs-lookup"><span data-stu-id="1af7d-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="1af7d-211">Standard läget är varning, inte av.</span><span class="sxs-lookup"><span data-stu-id="1af7d-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="1af7d-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="1af7d-213">Lägg för Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="1af7d-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="1af7d-214">-VirtualHubId</span></span>
<span data-ttu-id="1af7d-215">Det virtuella nav som en brand vägg är kopplad till</span><span class="sxs-lookup"><span data-stu-id="1af7d-215">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1af7d-216">-VirtualNetwork</span></span>
<span data-ttu-id="1af7d-217">Virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="1af7d-217">Virtual Network</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1af7d-218">-VirtualNetworkName</span></span>
<span data-ttu-id="1af7d-219">Anger namnet på det virtuella nätverk som brand väggen ska distribueras för.</span><span class="sxs-lookup"><span data-stu-id="1af7d-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="1af7d-220">Virtuellt nätverk och brand vägg måste tillhöra samma resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1af7d-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="1af7d-221">-Zone</span></span>
<span data-ttu-id="1af7d-222">En lista över tillgänglighets zoner som betecknar var brand väggen behöver komma.</span><span class="sxs-lookup"><span data-stu-id="1af7d-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="1af7d-223">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1af7d-223">-Confirm</span></span>
<span data-ttu-id="1af7d-224">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1af7d-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af7d-225">-WhatIf</span></span>
<span data-ttu-id="1af7d-226">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1af7d-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af7d-227">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1af7d-227">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af7d-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af7d-228">CommonParameters</span></span>
<span data-ttu-id="1af7d-229">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af7d-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af7d-230">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1af7d-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af7d-231">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1af7d-231">INPUTS</span></span>

### <span data-ttu-id="1af7d-232">System. String</span><span class="sxs-lookup"><span data-stu-id="1af7d-232">System.String</span></span>

### <span data-ttu-id="1af7d-233">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1af7d-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="1af7d-234">Microsoft. Azure. commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="1af7d-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="1af7d-235">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1af7d-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="1af7d-236">Microsoft. Azure. commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="1af7d-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="1af7d-237">Microsoft. Azure. commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="1af7d-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="1af7d-238">Microsoft. Azure. commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="1af7d-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="1af7d-239">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="1af7d-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1af7d-240">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1af7d-240">OUTPUTS</span></span>

### <span data-ttu-id="1af7d-241">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1af7d-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="1af7d-242">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1af7d-242">NOTES</span></span>

## <span data-ttu-id="1af7d-243">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1af7d-243">RELATED LINKS</span></span>

[<span data-ttu-id="1af7d-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1af7d-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="1af7d-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1af7d-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="1af7d-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1af7d-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="1af7d-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1af7d-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="1af7d-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1af7d-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="1af7d-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1af7d-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
