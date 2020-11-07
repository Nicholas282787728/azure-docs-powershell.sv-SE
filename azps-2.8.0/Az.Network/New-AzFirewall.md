---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 8d8d3ce0a236acb511eac715385b53c821f1dceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918297"
---
# <span data-ttu-id="10d13-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="10d13-101">New-AzFirewall</span></span>

## <span data-ttu-id="10d13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10d13-102">SYNOPSIS</span></span>
<span data-ttu-id="10d13-103">Skapar en ny brand vägg i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="10d13-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="10d13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10d13-104">SYNTAX</span></span>

### <span data-ttu-id="10d13-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="10d13-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10d13-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="10d13-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10d13-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="10d13-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10d13-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10d13-108">DESCRIPTION</span></span>
<span data-ttu-id="10d13-109">Cmdleten **New-AzFirewall** skapar en Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="10d13-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="10d13-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10d13-110">EXAMPLES</span></span>

### <span data-ttu-id="10d13-111">1: skapa en brand vägg som är ansluten till ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="10d13-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="10d13-112">I det här exemplet skapas en brand vägg som är kopplad till det virtuella nätverket "VNet" i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="10d13-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="10d13-113">Eftersom inga regler angavs blockerar brand väggen all trafik (standard beteende).</span><span class="sxs-lookup"><span data-stu-id="10d13-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="10d13-114">Hotet Intel körs också i standard läge – varning – vilket innebär att illvillig trafik loggas, men inte nekas.</span><span class="sxs-lookup"><span data-stu-id="10d13-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="10d13-115">2: skapa en brand vägg som tillåter all HTTPS-trafik</span><span class="sxs-lookup"><span data-stu-id="10d13-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="10d13-116">I det här exemplet skapas en brand vägg som tillåter all HTTPS-trafik på port 443.</span><span class="sxs-lookup"><span data-stu-id="10d13-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="10d13-117">Hotet Intel körs i standard läge – varning-vilket innebär att illvillig trafik loggas, men inte nekas.</span><span class="sxs-lookup"><span data-stu-id="10d13-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="10d13-118">3: DNAT-omdirigera trafik till 10.1.2.3:80 till 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="10d13-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="10d13-119">I det här exemplet skapas en brand vägg som översatte mål-IP och port för alla paket som är avsedda att 10.1.2.3:80 till 10.2.3.4:8080 Threat Intel är inaktiverat i det här exemplet.</span><span class="sxs-lookup"><span data-stu-id="10d13-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="10d13-120">4: skapa en brand vägg utan regler och med Intels hot-Intel i aviserings läget</span><span class="sxs-lookup"><span data-stu-id="10d13-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="10d13-121">I det här exemplet skapas en brand vägg som blockerar all trafik (standard beteende) och har hotet att Intel körs i aviserings läget.</span><span class="sxs-lookup"><span data-stu-id="10d13-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="10d13-122">Detta innebär att aviserings loggar släpps för illvillig trafik innan de andra reglerna tillämpas (i det här fallet är standard regeln-neka alla)</span><span class="sxs-lookup"><span data-stu-id="10d13-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="10d13-123">5: skapa en brand vägg som tillåter all HTTP-trafik på Port 8080, men blockerar skadlig domän identifieras av Threat Intel</span><span class="sxs-lookup"><span data-stu-id="10d13-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="10d13-124">I det här exemplet skapas en brand vägg som tillåter all HTTP-trafik på Port 8080 såvida den inte betraktas som skadlig för Threat Intel.</span><span class="sxs-lookup"><span data-stu-id="10d13-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="10d13-125">När du kör i läget neka, till skillnad mot varning, loggas inte den trafik som anses vara skadlig via Intel, men även blockeras.</span><span class="sxs-lookup"><span data-stu-id="10d13-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="10d13-126">6: skapa en brand vägg utan regler och tillgänglighets zoner</span><span class="sxs-lookup"><span data-stu-id="10d13-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="10d13-127">I det här exemplet skapas en brand vägg med alla tillgängliga tillgänglighets zoner.</span><span class="sxs-lookup"><span data-stu-id="10d13-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="10d13-128">7: skapa en brand vägg med två eller fler offentliga IP-adresser</span><span class="sxs-lookup"><span data-stu-id="10d13-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="10d13-129">I det här exemplet skapas en brand vägg som är ansluten till virtuellt nätverk (VNet) med två offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="10d13-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="10d13-130">8: skapa en brand vägg som tillåter MSSQL-trafik till specifik SQL-databas</span><span class="sxs-lookup"><span data-stu-id="10d13-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="10d13-131">I det här exemplet skapas en brand vägg som tillåter MSSQL-trafik på standard porten 1433 till SQL-sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="10d13-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

## <span data-ttu-id="10d13-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10d13-132">PARAMETERS</span></span>

### <span data-ttu-id="10d13-133">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="10d13-133">-ApplicationRuleCollection</span></span>
<span data-ttu-id="10d13-134">Anger program reglerna för den nya brand väggen.</span><span class="sxs-lookup"><span data-stu-id="10d13-134">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="10d13-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10d13-135">-AsJob</span></span>
<span data-ttu-id="10d13-136">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="10d13-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10d13-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d13-137">-DefaultProfile</span></span>
<span data-ttu-id="10d13-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10d13-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10d13-139">-Force</span><span class="sxs-lookup"><span data-stu-id="10d13-139">-Force</span></span>
<span data-ttu-id="10d13-140">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="10d13-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10d13-141">-Plats</span><span class="sxs-lookup"><span data-stu-id="10d13-141">-Location</span></span>
<span data-ttu-id="10d13-142">Anger området för brand väggen.</span><span class="sxs-lookup"><span data-stu-id="10d13-142">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="10d13-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="10d13-143">-Name</span></span>
<span data-ttu-id="10d13-144">Anger namnet på den Azure Firewall som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="10d13-144">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="10d13-145">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="10d13-145">-NatRuleCollection</span></span>
<span data-ttu-id="10d13-146">Listan med AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="10d13-146">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="10d13-147">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="10d13-147">-NetworkRuleCollection</span></span>
<span data-ttu-id="10d13-148">Listan med AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="10d13-148">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="10d13-149">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="10d13-149">-PublicIpAddress</span></span>
<span data-ttu-id="10d13-150">En eller flera offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="10d13-150">One or more Public IP Addresses.</span></span> <span data-ttu-id="10d13-151">De offentliga IP-adresserna måste använda standard-SKU och måste tillhöra samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="10d13-151">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="10d13-152">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="10d13-152">-PublicIpName</span></span>
<span data-ttu-id="10d13-153">Offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="10d13-153">Public Ip Name.</span></span> <span data-ttu-id="10d13-154">Den offentliga IP-adressen måste använda standard-SKU och måste tillhöra samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="10d13-154">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="10d13-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d13-155">-ResourceGroupName</span></span>
<span data-ttu-id="10d13-156">Anger namnet på en resurs grupp som ska innehålla brand väggen.</span><span class="sxs-lookup"><span data-stu-id="10d13-156">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="10d13-157">-Zone</span><span class="sxs-lookup"><span data-stu-id="10d13-157">-Zone</span></span>
<span data-ttu-id="10d13-158">En lista över tillgänglighets zoner som betecknar var brand väggen behöver komma.</span><span class="sxs-lookup"><span data-stu-id="10d13-158">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="10d13-159">-Tagg</span><span class="sxs-lookup"><span data-stu-id="10d13-159">-Tag</span></span>
<span data-ttu-id="10d13-160">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="10d13-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="10d13-161">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="10d13-161">For example:</span></span>

<span data-ttu-id="10d13-162">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="10d13-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="10d13-163">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="10d13-163">-ThreatIntelMode</span></span>
<span data-ttu-id="10d13-164">Anger åtgärds läget för Threat intelligence.</span><span class="sxs-lookup"><span data-stu-id="10d13-164">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="10d13-165">Standard läget är varning, inte av.</span><span class="sxs-lookup"><span data-stu-id="10d13-165">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="10d13-166">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="10d13-166">-VirtualNetwork</span></span>
<span data-ttu-id="10d13-167">Virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="10d13-167">Virtual Network</span></span>

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

### <span data-ttu-id="10d13-168">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="10d13-168">-VirtualNetworkName</span></span>
<span data-ttu-id="10d13-169">Anger namnet på det virtuella nätverk som brand väggen ska distribueras för.</span><span class="sxs-lookup"><span data-stu-id="10d13-169">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="10d13-170">Virtuellt nätverk och brand vägg måste tillhöra samma resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="10d13-170">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="10d13-171">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10d13-171">-Confirm</span></span>
<span data-ttu-id="10d13-172">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10d13-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10d13-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10d13-173">-WhatIf</span></span>
<span data-ttu-id="10d13-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10d13-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10d13-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10d13-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10d13-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d13-176">CommonParameters</span></span>
<span data-ttu-id="10d13-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10d13-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d13-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10d13-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d13-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10d13-179">INPUTS</span></span>

### <span data-ttu-id="10d13-180">System. String</span><span class="sxs-lookup"><span data-stu-id="10d13-180">System.String</span></span>

### <span data-ttu-id="10d13-181">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="10d13-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="10d13-182">Microsoft. Azure. commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="10d13-182">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="10d13-183">Microsoft. Azure. commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="10d13-183">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="10d13-184">Microsoft. Azure. commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="10d13-184">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="10d13-185">Microsoft. Azure. commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="10d13-185">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="10d13-186">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="10d13-186">System.Collections.Hashtable</span></span>

## <span data-ttu-id="10d13-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10d13-187">OUTPUTS</span></span>

### <span data-ttu-id="10d13-188">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="10d13-188">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="10d13-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10d13-189">NOTES</span></span>

## <span data-ttu-id="10d13-190">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10d13-190">RELATED LINKS</span></span>

[<span data-ttu-id="10d13-191">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="10d13-191">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="10d13-192">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="10d13-192">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="10d13-193">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="10d13-193">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="10d13-194">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="10d13-194">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="10d13-195">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="10d13-195">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="10d13-196">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="10d13-196">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
