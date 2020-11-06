---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
ms.openlocfilehash: 6486c7db87e8c71b0703b90a765fa30287b82769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584936"
---
# <span data-ttu-id="c92dd-101">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c92dd-101">New-AzureRmFirewall</span></span>

## <span data-ttu-id="c92dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c92dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c92dd-103">Skapar en ny brand vägg i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c92dd-103">Creates a new Firewall in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c92dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c92dd-104">SYNTAX</span></span>

```
New-AzureRmFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-VirtualNetworkName <String>] [-PublicIpName <String>]
 [-ApplicationRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]>]
 [-NatRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]>]
 [-NetworkRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c92dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c92dd-105">DESCRIPTION</span></span>
<span data-ttu-id="c92dd-106">Cmdleten **New-AzureRmFirewall** skapar en Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="c92dd-106">The **New-AzureRmFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="c92dd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c92dd-107">EXAMPLES</span></span>

### <span data-ttu-id="c92dd-108">1: skapa en brand vägg som är ansluten till ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="c92dd-108">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="c92dd-109">I det här exemplet skapas en brand vägg som är kopplad till det virtuella nätverket "VNet" i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c92dd-109">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c92dd-110">Eftersom inga regler angavs blockerar brand väggen all trafik (standard beteende).</span><span class="sxs-lookup"><span data-stu-id="c92dd-110">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>

### <span data-ttu-id="c92dd-111">2: skapa en brand vägg som tillåter all HTTPS-trafik</span><span class="sxs-lookup"><span data-stu-id="c92dd-111">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="c92dd-112">I det här exemplet skapas en brand vägg som tillåter all HTTPS-trafik på port 443.</span><span class="sxs-lookup"><span data-stu-id="c92dd-112">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>

### <span data-ttu-id="c92dd-113">3: DNAT-omdirigera trafik till 10.1.2.3:80 till 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="c92dd-113">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection
```

<span data-ttu-id="c92dd-114">I det här exemplet skapas en brand vägg som översatte mål-IP och port för alla paket som är avsedda att 10.1.2.3:80 till 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="c92dd-114">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>

## <span data-ttu-id="c92dd-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c92dd-115">PARAMETERS</span></span>

### <span data-ttu-id="c92dd-116">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c92dd-116">-ApplicationRuleCollection</span></span>
<span data-ttu-id="c92dd-117">Anger program reglerna för den nya brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c92dd-117">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c92dd-118">-AsJob</span></span>
<span data-ttu-id="c92dd-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c92dd-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c92dd-120">-DefaultProfile</span></span>
<span data-ttu-id="c92dd-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c92dd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c92dd-122">-Force</span></span>
<span data-ttu-id="c92dd-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c92dd-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="c92dd-124">-Location</span></span>
<span data-ttu-id="c92dd-125">Anger området för brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c92dd-125">Specifies the region for the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="c92dd-126">-Name</span></span>
<span data-ttu-id="c92dd-127">Anger namnet på den Azure Firewall som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="c92dd-127">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-128">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c92dd-128">-NatRuleCollection</span></span>
<span data-ttu-id="c92dd-129">Listan med AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="c92dd-129">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-130">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c92dd-130">-NetworkRuleCollection</span></span>
<span data-ttu-id="c92dd-131">Listan med AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="c92dd-131">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-132">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="c92dd-132">-PublicIpName</span></span>
<span data-ttu-id="c92dd-133">Offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="c92dd-133">Public Ip Name.</span></span> <span data-ttu-id="c92dd-134">Den offentliga IP-adressen måste använda standard-SKU och måste tillhöra samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c92dd-134">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c92dd-135">-ResourceGroupName</span></span>
<span data-ttu-id="c92dd-136">Anger namnet på en resurs grupp som ska innehålla brand väggen.</span><span class="sxs-lookup"><span data-stu-id="c92dd-136">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c92dd-137">-Tag</span></span>
<span data-ttu-id="c92dd-138">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c92dd-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c92dd-139">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="c92dd-139">For example:</span></span>

<span data-ttu-id="c92dd-140">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="c92dd-140">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c92dd-141">-VirtualNetworkName</span></span>
<span data-ttu-id="c92dd-142">Anger namnet på det virtuella nätverk som brand väggen ska distribueras för.</span><span class="sxs-lookup"><span data-stu-id="c92dd-142">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="c92dd-143">Virtuellt nätverk och brand vägg måste tillhöra samma resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c92dd-143">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c92dd-144">-Confirm</span></span>
<span data-ttu-id="c92dd-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c92dd-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c92dd-146">-WhatIf</span></span>
<span data-ttu-id="c92dd-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c92dd-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c92dd-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c92dd-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c92dd-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c92dd-149">CommonParameters</span></span>
<span data-ttu-id="c92dd-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c92dd-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c92dd-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c92dd-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c92dd-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c92dd-152">INPUTS</span></span>

### <span data-ttu-id="c92dd-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="c92dd-153">None</span></span>
<span data-ttu-id="c92dd-154">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c92dd-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c92dd-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c92dd-155">OUTPUTS</span></span>

### <span data-ttu-id="c92dd-156">Microsoft. Azure. commands. Networks. Models. PSFirewall</span><span class="sxs-lookup"><span data-stu-id="c92dd-156">Microsoft.Azure.Commands.Network.Models.PSFirewall</span></span>

## <span data-ttu-id="c92dd-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c92dd-157">NOTES</span></span>

## <span data-ttu-id="c92dd-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c92dd-158">RELATED LINKS</span></span>

[<span data-ttu-id="c92dd-159">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c92dd-159">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="c92dd-160">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c92dd-160">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="c92dd-161">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c92dd-161">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)

[<span data-ttu-id="c92dd-162">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c92dd-162">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="c92dd-163">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c92dd-163">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="c92dd-164">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c92dd-164">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)
