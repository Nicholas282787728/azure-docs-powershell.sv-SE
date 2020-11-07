---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 3b4014b56a36228fe53221430ffe79a43118f8fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925589"
---
# <span data-ttu-id="c3ada-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c3ada-101">New-AzFirewall</span></span>

## <span data-ttu-id="c3ada-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3ada-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ada-103">Skapar en ny brand vägg i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c3ada-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="c3ada-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3ada-104">SYNTAX</span></span>

### <span data-ttu-id="c3ada-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="c3ada-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3ada-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="c3ada-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3ada-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="c3ada-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3ada-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3ada-108">DESCRIPTION</span></span>
<span data-ttu-id="c3ada-109">Cmdleten **New-AzFirewall** skapar en Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="c3ada-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="c3ada-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3ada-110">EXAMPLES</span></span>

### <span data-ttu-id="c3ada-111">1: skapa en brand vägg som är ansluten till ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="c3ada-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="c3ada-112">I det här exemplet skapas en brand vägg som är kopplad till det virtuella nätverket "VNet" i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c3ada-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c3ada-113">Eftersom inga regler angavs blockerar brand väggen all trafik (standard beteende).</span><span class="sxs-lookup"><span data-stu-id="c3ada-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="c3ada-114">Hotet Intel körs också i standard läge – varning – vilket innebär att illvillig trafik loggas, men inte nekas.</span><span class="sxs-lookup"><span data-stu-id="c3ada-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="c3ada-115">2: skapa en brand vägg som tillåter all HTTPS-trafik</span><span class="sxs-lookup"><span data-stu-id="c3ada-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="c3ada-116">I det här exemplet skapas en brand vägg som tillåter all HTTPS-trafik på port 443.</span><span class="sxs-lookup"><span data-stu-id="c3ada-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="c3ada-117">Hotet Intel körs i standard läge – varning-vilket innebär att illvillig trafik loggas, men inte nekas.</span><span class="sxs-lookup"><span data-stu-id="c3ada-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="c3ada-118">3: DNAT-omdirigera trafik till 10.1.2.3:80 till 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="c3ada-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="c3ada-119">I det här exemplet skapas en brand vägg som översatte mål-IP och port för alla paket som är avsedda att 10.1.2.3:80 till 10.2.3.4:8080 Threat Intel är inaktiverat i det här exemplet.</span><span class="sxs-lookup"><span data-stu-id="c3ada-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="c3ada-120">4: skapa en brand vägg utan regler och med Intels hot-Intel i aviserings läget</span><span class="sxs-lookup"><span data-stu-id="c3ada-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="c3ada-121">I det här exemplet skapas en brand vägg som blockerar all trafik (standard beteende) och har hotet att Intel körs i aviserings läget.</span><span class="sxs-lookup"><span data-stu-id="c3ada-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="c3ada-122">Detta innebär att aviserings loggar släpps för illvillig trafik innan de andra reglerna tillämpas (i det här fallet är standard regeln-neka alla)</span><span class="sxs-lookup"><span data-stu-id="c3ada-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="c3ada-123">5: skapa en brand vägg som tillåter all HTTP-trafik på Port 8080, men blockerar skadlig domän identifieras av Threat Intel</span><span class="sxs-lookup"><span data-stu-id="c3ada-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="c3ada-124">I det här exemplet skapas en brand vägg som tillåter all HTTP-trafik på Port 8080 såvida den inte betraktas som skadlig för Threat Intel.</span><span class="sxs-lookup"><span data-stu-id="c3ada-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="c3ada-125">När du kör i läget neka, till skillnad mot varning, loggas inte den trafik som anses vara skadlig via Intel, men även blockeras.</span><span class="sxs-lookup"><span data-stu-id="c3ada-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="c3ada-126">6: skapa en brand vägg utan regler och tillgänglighets zoner</span><span class="sxs-lookup"><span data-stu-id="c3ada-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="c3ada-127">I det här exemplet skapas en brand vägg med alla tillgängliga tillgänglighets zoner.</span><span class="sxs-lookup"><span data-stu-id="c3ada-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="c3ada-128">7: skapa en brand vägg med två eller fler offentliga IP-adresser</span><span class="sxs-lookup"><span data-stu-id="c3ada-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="c3ada-129">I det här exemplet skapas en brand vägg som är ansluten till virtuellt nätverk (VNet) med två offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="c3ada-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="c3ada-130">8: skapa en brand vägg som tillåter MSSQL-trafik till specifik SQL-databas</span><span class="sxs-lookup"><span data-stu-id="c3ada-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="c3ada-131">I det här exemplet skapas en brand vägg som tillåter MSSQL-trafik på standard porten 1433 till SQL-sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="c3ada-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="c3ada-132">9: skapa en brand vägg som är kopplad till ett virtuellt nav</span><span class="sxs-lookup"><span data-stu-id="c3ada-132">9:  Create a Firewall attached to a virtual hub</span></span>
```
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="c3ada-133">I det här exemplet skapas en brand vägg som är ansluten till virtuella hubben "vHub".</span><span class="sxs-lookup"><span data-stu-id="c3ada-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="c3ada-134">En brand Väggs princip $fp kopplas till brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c3ada-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="c3ada-135">Denna brand vägg tillåter/nekar trafiken baserat på reglerna som nämns i brand Väggs principens $fp.</span><span class="sxs-lookup"><span data-stu-id="c3ada-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="c3ada-136">Det virtuella navet och brand väggen bör vara i samma regioner.</span><span class="sxs-lookup"><span data-stu-id="c3ada-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="c3ada-137">10: skapa en brand vägg med Lägg för hot intelligens</span><span class="sxs-lookup"><span data-stu-id="c3ada-137">10: Create a Firewall with threat intelligence whitelist setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="c3ada-138">I det här exemplet skapas en brand vägg som Lägg "www.microsoft.com" och "8.8.8.8" från Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="c3ada-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="c3ada-139">11: skapa en brand vägg med anpassade inställningar för privat område</span><span class="sxs-lookup"><span data-stu-id="c3ada-139">11: Create a Firewall with customized private range setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="c3ada-140">I det här exemplet skapas en brand vägg som hanterar "99.99.99.0/24" och "66.66.0.0/16" som privata IP-adressintervall och inte är med i trafik till dessa adresser</span><span class="sxs-lookup"><span data-stu-id="c3ada-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="c3ada-141">12: skapa en brand vägg med ett hanterings nät och en offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="c3ada-141">12:  Create a Firewall with a management subnet and Public IP address</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="c3ada-142">I det här exemplet skapas en brand vägg som är kopplad till det virtuella nätverket "VNet" i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c3ada-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c3ada-143">Eftersom inga regler angavs blockerar brand väggen all trafik (standard beteende).</span><span class="sxs-lookup"><span data-stu-id="c3ada-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="c3ada-144">Hotet Intel körs också i standard läge – varning – vilket innebär att illvillig trafik loggas, men inte nekas.</span><span class="sxs-lookup"><span data-stu-id="c3ada-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="c3ada-145">För att stödja upptvingade tunnlar-scenarion använder den här brand väggen under nätet "AzureFirewallManagementSubnet" och den offentliga hanterings-IP-adressen för dess hanterings trafik</span><span class="sxs-lookup"><span data-stu-id="c3ada-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="c3ada-146">13: skapa en brand vägg med brand Väggs princip som är ansluten till ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="c3ada-146">13:  Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="c3ada-147">I det här exemplet skapas en brand vägg som är kopplad till det virtuella nätverket "VNet" i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c3ada-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c3ada-148">Reglerna och hotets intelligens som kommer att tillämpas på brand väggen hämtas från brand Väggs principen</span><span class="sxs-lookup"><span data-stu-id="c3ada-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

## <span data-ttu-id="c3ada-149">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3ada-149">PARAMETERS</span></span>

### <span data-ttu-id="c3ada-150">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c3ada-150">-ApplicationRuleCollection</span></span>
<span data-ttu-id="c3ada-151">Anger program reglerna för den nya brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c3ada-151">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="c3ada-152">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3ada-152">-AsJob</span></span>
<span data-ttu-id="c3ada-153">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c3ada-153">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3ada-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ada-154">-DefaultProfile</span></span>
<span data-ttu-id="c3ada-155">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3ada-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3ada-156">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c3ada-156">-FirewallPolicyId</span></span>
<span data-ttu-id="c3ada-157">Brand Väggs principen ansluten till brand väggen</span><span class="sxs-lookup"><span data-stu-id="c3ada-157">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="c3ada-158">-Force</span><span class="sxs-lookup"><span data-stu-id="c3ada-158">-Force</span></span>
<span data-ttu-id="c3ada-159">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c3ada-159">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3ada-160">-Plats</span><span class="sxs-lookup"><span data-stu-id="c3ada-160">-Location</span></span>
<span data-ttu-id="c3ada-161">Anger området för brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c3ada-161">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="c3ada-162">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c3ada-162">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="c3ada-163">En eller flera offentliga IP-adresser som ska användas för hanterings trafik.</span><span class="sxs-lookup"><span data-stu-id="c3ada-163">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="c3ada-164">De offentliga IP-adresserna måste använda standard-SKU och måste tillhöra samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c3ada-164">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="c3ada-165">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3ada-165">-Name</span></span>
<span data-ttu-id="c3ada-166">Anger namnet på den Azure Firewall som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="c3ada-166">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c3ada-167">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c3ada-167">-NatRuleCollection</span></span>
<span data-ttu-id="c3ada-168">Listan med AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="c3ada-168">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="c3ada-169">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c3ada-169">-NetworkRuleCollection</span></span>
<span data-ttu-id="c3ada-170">Listan med AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="c3ada-170">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="c3ada-171">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="c3ada-171">-PrivateRange</span></span>
<span data-ttu-id="c3ada-172">De privata IP-adresser som trafik inte SNAT'ed</span><span class="sxs-lookup"><span data-stu-id="c3ada-172">The private IP ranges to which traffic won't be SNAT'ed</span></span>

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

### <span data-ttu-id="c3ada-173">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c3ada-173">-PublicIpAddress</span></span>
<span data-ttu-id="c3ada-174">En eller flera offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="c3ada-174">One or more Public IP Addresses.</span></span> <span data-ttu-id="c3ada-175">De offentliga IP-adresserna måste använda standard-SKU och måste tillhöra samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c3ada-175">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="c3ada-176">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="c3ada-176">-PublicIpName</span></span>
<span data-ttu-id="c3ada-177">Offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="c3ada-177">Public Ip Name.</span></span> <span data-ttu-id="c3ada-178">Den offentliga IP-adressen måste använda standard-SKU och måste tillhöra samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c3ada-178">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="c3ada-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3ada-179">-ResourceGroupName</span></span>
<span data-ttu-id="c3ada-180">Anger namnet på en resurs grupp som ska innehålla brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c3ada-180">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="c3ada-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="c3ada-181">-Sku</span></span>
<span data-ttu-id="c3ada-182">SKU-typen för brand vägg</span><span class="sxs-lookup"><span data-stu-id="c3ada-182">The sku type for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ada-183">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c3ada-183">-Tag</span></span>
<span data-ttu-id="c3ada-184">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c3ada-184">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c3ada-185">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="c3ada-185">For example:</span></span>

<span data-ttu-id="c3ada-186">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="c3ada-186">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c3ada-187">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="c3ada-187">-ThreatIntelMode</span></span>
<span data-ttu-id="c3ada-188">Anger åtgärds läget för Threat intelligence.</span><span class="sxs-lookup"><span data-stu-id="c3ada-188">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="c3ada-189">Standard läget är varning, inte av.</span><span class="sxs-lookup"><span data-stu-id="c3ada-189">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="c3ada-190">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="c3ada-190">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="c3ada-191">Lägg för Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="c3ada-191">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="c3ada-192">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="c3ada-192">-VirtualHubId</span></span>
<span data-ttu-id="c3ada-193">Det virtuella nav som en brand vägg är kopplad till</span><span class="sxs-lookup"><span data-stu-id="c3ada-193">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="c3ada-194">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c3ada-194">-VirtualNetwork</span></span>
<span data-ttu-id="c3ada-195">Virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="c3ada-195">Virtual Network</span></span>

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

### <span data-ttu-id="c3ada-196">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c3ada-196">-VirtualNetworkName</span></span>
<span data-ttu-id="c3ada-197">Anger namnet på det virtuella nätverk som brand väggen ska distribueras för.</span><span class="sxs-lookup"><span data-stu-id="c3ada-197">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="c3ada-198">Virtuellt nätverk och brand vägg måste tillhöra samma resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c3ada-198">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="c3ada-199">-Zone</span><span class="sxs-lookup"><span data-stu-id="c3ada-199">-Zone</span></span>
<span data-ttu-id="c3ada-200">En lista över tillgänglighets zoner som betecknar var brand väggen behöver komma.</span><span class="sxs-lookup"><span data-stu-id="c3ada-200">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="c3ada-201">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3ada-201">-Confirm</span></span>
<span data-ttu-id="c3ada-202">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3ada-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3ada-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3ada-203">-WhatIf</span></span>
<span data-ttu-id="c3ada-204">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3ada-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3ada-205">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3ada-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3ada-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ada-206">CommonParameters</span></span>
<span data-ttu-id="c3ada-207">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3ada-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ada-208">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3ada-208">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ada-209">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3ada-209">INPUTS</span></span>

### <span data-ttu-id="c3ada-210">System. String</span><span class="sxs-lookup"><span data-stu-id="c3ada-210">System.String</span></span>

### <span data-ttu-id="c3ada-211">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c3ada-211">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="c3ada-212">Microsoft. Azure. commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="c3ada-212">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="c3ada-213">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c3ada-213">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="c3ada-214">Microsoft. Azure. commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="c3ada-214">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="c3ada-215">Microsoft. Azure. commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="c3ada-215">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="c3ada-216">Microsoft. Azure. commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="c3ada-216">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="c3ada-217">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="c3ada-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c3ada-218">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3ada-218">OUTPUTS</span></span>

### <span data-ttu-id="c3ada-219">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c3ada-219">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="c3ada-220">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3ada-220">NOTES</span></span>

## <span data-ttu-id="c3ada-221">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3ada-221">RELATED LINKS</span></span>

[<span data-ttu-id="c3ada-222">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c3ada-222">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="c3ada-223">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c3ada-223">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="c3ada-224">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c3ada-224">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="c3ada-225">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c3ada-225">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="c3ada-226">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c3ada-226">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="c3ada-227">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c3ada-227">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
