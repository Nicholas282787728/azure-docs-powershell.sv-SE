---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 48e8fc8685073a0fad742152191fe68c368fbb3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748071"
---
# <span data-ttu-id="d9315-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d9315-101">New-AzFirewall</span></span>

## <span data-ttu-id="d9315-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9315-102">SYNOPSIS</span></span>
<span data-ttu-id="d9315-103">Skapar en ny brand vägg i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d9315-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="d9315-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9315-104">SYNTAX</span></span>

### <span data-ttu-id="d9315-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="d9315-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9315-106">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="d9315-106">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9315-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9315-107">DESCRIPTION</span></span>
<span data-ttu-id="d9315-108">Cmdleten **New-AzFirewall** skapar en Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="d9315-108">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="d9315-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9315-109">EXAMPLES</span></span>

### <span data-ttu-id="d9315-110">1: skapa en brand vägg som är ansluten till ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="d9315-110">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="d9315-111">I det här exemplet skapas en brand vägg som är kopplad till det virtuella nätverket "VNet" i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="d9315-111">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="d9315-112">Eftersom inga regler angavs blockerar brand väggen all trafik (standard beteende).</span><span class="sxs-lookup"><span data-stu-id="d9315-112">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="d9315-113">Hotet Intel körs också i standard läge – varning – vilket innebär att illvillig trafik loggas, men inte nekas.</span><span class="sxs-lookup"><span data-stu-id="d9315-113">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="d9315-114">2: skapa en brand vägg som tillåter all HTTPS-trafik</span><span class="sxs-lookup"><span data-stu-id="d9315-114">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="d9315-115">I det här exemplet skapas en brand vägg som tillåter all HTTPS-trafik på port 443.</span><span class="sxs-lookup"><span data-stu-id="d9315-115">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="d9315-116">Hotet Intel körs i standard läge – varning-vilket innebär att illvillig trafik loggas, men inte nekas.</span><span class="sxs-lookup"><span data-stu-id="d9315-116">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="d9315-117">3: DNAT-omdirigera trafik till 10.1.2.3:80 till 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="d9315-117">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="d9315-118">I det här exemplet skapas en brand vägg som översatte mål-IP och port för alla paket som är avsedda att 10.1.2.3:80 till 10.2.3.4:8080 Threat Intel är inaktiverat i det här exemplet.</span><span class="sxs-lookup"><span data-stu-id="d9315-118">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="d9315-119">4: skapa en brand vägg utan regler och med Intels hot-Intel i aviserings läget</span><span class="sxs-lookup"><span data-stu-id="d9315-119">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ThreatIntelMode Alert
```

<span data-ttu-id="d9315-120">I det här exemplet skapas en brand vägg som blockerar all trafik (standard beteende) och har hotet att Intel körs i aviserings läget.</span><span class="sxs-lookup"><span data-stu-id="d9315-120">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="d9315-121">Detta innebär att aviserings loggar släpps för illvillig trafik innan de andra reglerna tillämpas (i det här fallet är standard regeln-neka alla)</span><span class="sxs-lookup"><span data-stu-id="d9315-121">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="d9315-122">5: skapa en brand vägg som tillåter all HTTP-trafik på Port 8080, men blockerar skadlig domän identifieras av Threat Intel</span><span class="sxs-lookup"><span data-stu-id="d9315-122">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="d9315-123">I det här exemplet skapas en brand vägg som tillåter all HTTP-trafik på Port 8080 såvida den inte betraktas som skadlig för Threat Intel.</span><span class="sxs-lookup"><span data-stu-id="d9315-123">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="d9315-124">När du kör i läget neka, till skillnad mot varning, loggas inte den trafik som anses vara skadlig via Intel, men även blockeras.</span><span class="sxs-lookup"><span data-stu-id="d9315-124">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

## <span data-ttu-id="d9315-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9315-125">PARAMETERS</span></span>

### <span data-ttu-id="d9315-126">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d9315-126">-ApplicationRuleCollection</span></span>
<span data-ttu-id="d9315-127">Anger program reglerna för den nya brand väggen.</span><span class="sxs-lookup"><span data-stu-id="d9315-127">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="d9315-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9315-128">-AsJob</span></span>
<span data-ttu-id="d9315-129">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d9315-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9315-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9315-130">-DefaultProfile</span></span>
<span data-ttu-id="d9315-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9315-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9315-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d9315-132">-Force</span></span>
<span data-ttu-id="d9315-133">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d9315-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9315-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="d9315-134">-Location</span></span>
<span data-ttu-id="d9315-135">Anger området för brand väggen.</span><span class="sxs-lookup"><span data-stu-id="d9315-135">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="d9315-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9315-136">-Name</span></span>
<span data-ttu-id="d9315-137">Anger namnet på den Azure Firewall som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="d9315-137">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d9315-138">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d9315-138">-NatRuleCollection</span></span>
<span data-ttu-id="d9315-139">Listan med AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="d9315-139">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="d9315-140">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d9315-140">-NetworkRuleCollection</span></span>
<span data-ttu-id="d9315-141">Listan med AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="d9315-141">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="d9315-142">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="d9315-142">-PublicIpName</span></span>
<span data-ttu-id="d9315-143">Offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d9315-143">Public Ip Name.</span></span> <span data-ttu-id="d9315-144">Den offentliga IP-adressen måste använda standard-SKU och måste tillhöra samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="d9315-144">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9315-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9315-145">-ResourceGroupName</span></span>
<span data-ttu-id="d9315-146">Anger namnet på en resurs grupp som ska innehålla brand väggen.</span><span class="sxs-lookup"><span data-stu-id="d9315-146">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="d9315-147">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d9315-147">-Tag</span></span>
<span data-ttu-id="d9315-148">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d9315-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d9315-149">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="d9315-149">For example:</span></span>

<span data-ttu-id="d9315-150">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="d9315-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d9315-151">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="d9315-151">-ThreatIntelMode</span></span>
<span data-ttu-id="d9315-152">Anger åtgärds läget för Threat intelligence.</span><span class="sxs-lookup"><span data-stu-id="d9315-152">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="d9315-153">Standard läget är varning, inte av.</span><span class="sxs-lookup"><span data-stu-id="d9315-153">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9315-154">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d9315-154">-VirtualNetworkName</span></span>
<span data-ttu-id="d9315-155">Anger namnet på det virtuella nätverk som brand väggen ska distribueras för.</span><span class="sxs-lookup"><span data-stu-id="d9315-155">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="d9315-156">Virtuellt nätverk och brand vägg måste tillhöra samma resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d9315-156">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9315-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9315-157">-Confirm</span></span>
<span data-ttu-id="d9315-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9315-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9315-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9315-159">-WhatIf</span></span>
<span data-ttu-id="d9315-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9315-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9315-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9315-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9315-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9315-162">CommonParameters</span></span>
<span data-ttu-id="d9315-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9315-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9315-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9315-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9315-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9315-165">INPUTS</span></span>

### <span data-ttu-id="d9315-166">System. String</span><span class="sxs-lookup"><span data-stu-id="d9315-166">System.String</span></span>

### <span data-ttu-id="d9315-167">Microsoft. Azure. commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="d9315-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="d9315-168">Microsoft. Azure. commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="d9315-168">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="d9315-169">Microsoft. Azure. commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="d9315-169">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="d9315-170">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="d9315-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d9315-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9315-171">OUTPUTS</span></span>

### <span data-ttu-id="d9315-172">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="d9315-172">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="d9315-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9315-173">NOTES</span></span>

## <span data-ttu-id="d9315-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9315-174">RELATED LINKS</span></span>

[<span data-ttu-id="d9315-175">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d9315-175">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="d9315-176">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d9315-176">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="d9315-177">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d9315-177">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="d9315-178">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d9315-178">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="d9315-179">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d9315-179">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="d9315-180">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d9315-180">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
