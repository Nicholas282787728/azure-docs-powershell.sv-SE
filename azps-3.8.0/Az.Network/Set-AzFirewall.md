---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 36ba29104fbc9e87ae2776504dc48bed8a5b9ffa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089057"
---
# <span data-ttu-id="ff66a-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ff66a-101">Set-AzFirewall</span></span>

## <span data-ttu-id="ff66a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff66a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff66a-103">Sparar en modifierad brand vägg.</span><span class="sxs-lookup"><span data-stu-id="ff66a-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="ff66a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff66a-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff66a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff66a-105">DESCRIPTION</span></span>
<span data-ttu-id="ff66a-106">Cmdleten **set-AzFirewall** uppdaterar en Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="ff66a-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="ff66a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff66a-107">EXAMPLES</span></span>

### <span data-ttu-id="ff66a-108">1: uppdatera prioritet för en regel samling för en brand Väggs program</span><span class="sxs-lookup"><span data-stu-id="ff66a-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="ff66a-109">Det här exemplet uppdaterar prioriteten för en befintlig regel samling av en Azure-brandvägg.</span><span class="sxs-lookup"><span data-stu-id="ff66a-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="ff66a-110">Om du antar Azure Firewall "AzureFirewall" i resurs gruppen "RG" innehåller en program regel samling med namnet "ruleCollectionName", kommer de ovanstående kommandona att ändra prioriteten för den regel samlingen och uppdatera Azure Firewall efteråt.</span><span class="sxs-lookup"><span data-stu-id="ff66a-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="ff66a-111">Utan kommandot Set-AzFirewall återspeglas inte alla åtgärder som utförs på det lokala $azFw-objektet på servern.</span><span class="sxs-lookup"><span data-stu-id="ff66a-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="ff66a-112">2: skapa en Azure-brandvägg och konfigurera en samling med program regler senare</span><span class="sxs-lookup"><span data-stu-id="ff66a-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="ff66a-113">I det här exemplet skapas en brand vägg först utan några program regel samlingar.</span><span class="sxs-lookup"><span data-stu-id="ff66a-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="ff66a-114">Därefter skapas en program regel-och program regel samling, och därefter ändras brand Väggs objekt i minnet utan att det påverkar den verkliga konfigurationen i molnet.</span><span class="sxs-lookup"><span data-stu-id="ff66a-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="ff66a-115">Set-AzFirewall måste anropas för att ändringarna ska synas i molnet.</span><span class="sxs-lookup"><span data-stu-id="ff66a-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="ff66a-116">3: uppdatera hotet Intels arbets läge i Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="ff66a-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="ff66a-117">I det här exemplet uppdateras hotet Intels arbets läge för Azure Firewall "AzureFirewall" i resurs gruppen "RG".</span><span class="sxs-lookup"><span data-stu-id="ff66a-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="ff66a-118">Utan kommandot Set-AzFirewall återspeglas inte alla åtgärder som utförs på det lokala $azFw-objektet på servern.</span><span class="sxs-lookup"><span data-stu-id="ff66a-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="ff66a-119">4: frigöra och tilldela brand väggen</span><span class="sxs-lookup"><span data-stu-id="ff66a-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="ff66a-120">I det här exemplet hämtas en brand vägg, avsätter brand väggen och sparar den.</span><span class="sxs-lookup"><span data-stu-id="ff66a-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="ff66a-121">Kommandot frigör tar bort den aktiva tjänsten men bevarar brand väggens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ff66a-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="ff66a-122">Set-AzFirewall måste anropas för att ändringarna ska synas i molnet.</span><span class="sxs-lookup"><span data-stu-id="ff66a-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="ff66a-123">Om användaren vill starta tjänsten igen ska metoden allocate anropas i brand väggen.</span><span class="sxs-lookup"><span data-stu-id="ff66a-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="ff66a-124">Den nya VNet-och offentlige tjänsten måste finnas i samma resurs grupp som brand väggen.</span><span class="sxs-lookup"><span data-stu-id="ff66a-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="ff66a-125">För att ändringarna ska synas i molnet måste Set-AzFirewall anropas.</span><span class="sxs-lookup"><span data-stu-id="ff66a-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="ff66a-126">5: tilldela med en offentlig IP-adress för hantering av tvingande tunnel scenarion</span><span class="sxs-lookup"><span data-stu-id="ff66a-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="ff66a-127">I det här exemplet allokeras brand väggen med en offentlig IP-adress och undernät för tvingande tunnlar.</span><span class="sxs-lookup"><span data-stu-id="ff66a-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="ff66a-128">VNet måste innehålla ett undernät som heter "AzureFirewallManagementSubnet".</span><span class="sxs-lookup"><span data-stu-id="ff66a-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="ff66a-129">6: lägga till en offentlig IP-adress i en Azure-brandvägg</span><span class="sxs-lookup"><span data-stu-id="ff66a-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="ff66a-130">I det här exemplet är den offentliga IP-adressen "azFwPublicIp1" enligt brand väggen.</span><span class="sxs-lookup"><span data-stu-id="ff66a-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="ff66a-131">7: ta bort en offentlig IP-adress från en Azure-brandvägg</span><span class="sxs-lookup"><span data-stu-id="ff66a-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="ff66a-132">I det här exemplet är den offentliga IP-adressen "azFwPublicIp1" som frånkopplad från brand väggen.</span><span class="sxs-lookup"><span data-stu-id="ff66a-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="ff66a-133">8: ändra den offentliga Management-IP-adressen i en Azure-brandvägg</span><span class="sxs-lookup"><span data-stu-id="ff66a-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="ff66a-134">I det här exemplet ändras brand väggens offentliga IP-adress för hanteringen till "AzFwMgmtPublicIp2"</span><span class="sxs-lookup"><span data-stu-id="ff66a-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>


## <span data-ttu-id="ff66a-135">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff66a-135">PARAMETERS</span></span>

### <span data-ttu-id="ff66a-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff66a-136">-AsJob</span></span>
<span data-ttu-id="ff66a-137">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ff66a-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff66a-138">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ff66a-138">-AzureFirewall</span></span>
<span data-ttu-id="ff66a-139">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ff66a-139">The AzureFirewall</span></span>

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

### <span data-ttu-id="ff66a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff66a-140">-DefaultProfile</span></span>
<span data-ttu-id="ff66a-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff66a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff66a-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff66a-142">-Confirm</span></span>
<span data-ttu-id="ff66a-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff66a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff66a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff66a-144">-WhatIf</span></span>
<span data-ttu-id="ff66a-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff66a-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff66a-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff66a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff66a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff66a-147">CommonParameters</span></span>
<span data-ttu-id="ff66a-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff66a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff66a-149">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff66a-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff66a-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff66a-150">INPUTS</span></span>

### <span data-ttu-id="ff66a-151">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ff66a-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="ff66a-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff66a-152">OUTPUTS</span></span>

### <span data-ttu-id="ff66a-153">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ff66a-153">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="ff66a-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff66a-154">NOTES</span></span>

## <span data-ttu-id="ff66a-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff66a-155">RELATED LINKS</span></span>

[<span data-ttu-id="ff66a-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ff66a-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="ff66a-157">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ff66a-157">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="ff66a-158">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ff66a-158">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
