---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522480"
---
# <span data-ttu-id="aab14-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aab14-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="aab14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aab14-102">SYNOPSIS</span></span>
<span data-ttu-id="aab14-103">Lägger till en nätverks säkerhets regel i en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="aab14-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="aab14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aab14-104">SYNTAX</span></span>

### <span data-ttu-id="aab14-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="aab14-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aab14-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="aab14-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aab14-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aab14-107">DESCRIPTION</span></span>
<span data-ttu-id="aab14-108">Cmdleten **Add-AzNetworkSecurityRuleConfig** lägger till en nätverks säkerhets regel konfiguration i en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="aab14-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="aab14-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aab14-109">EXAMPLES</span></span>

### <span data-ttu-id="aab14-110">1: lägga till en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="aab14-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="aab14-111">Det första kommandot hämtar en Azure nätverks säkerhets grupp med namnet "nsg1" från resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="aab14-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="aab14-112">Det andra kommandot lägger till en nätverks säkerhets regel med namnet "RDP-Rule" som tillåter trafik från Internet på port 3389 till det hämtade objektet för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="aab14-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="aab14-113">Behåller den ändrade Azure Network Security-gruppen.</span><span class="sxs-lookup"><span data-stu-id="aab14-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="aab14-114">2: lägga till en ny säkerhets regel med program säkerhets grupper</span><span class="sxs-lookup"><span data-stu-id="aab14-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="aab14-115">Först skapar vi två nya program säkerhets grupper.</span><span class="sxs-lookup"><span data-stu-id="aab14-115">First, we create two new application security groups.</span></span> <span data-ttu-id="aab14-116">Sedan hämtar vi en Azure nätverks säkerhets grupp med namnet "nsg1" från resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="aab14-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="aab14-117">och Lägg till en nätverks säkerhets regel med namnet "RDP-Rule" till den.</span><span class="sxs-lookup"><span data-stu-id="aab14-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="aab14-118">Regeln tillåter trafik från alla IP-konfigurationer i program säkerhets gruppen "srcAsg" till alla IP-konfigurationer i "destAsg" på port 3389.</span><span class="sxs-lookup"><span data-stu-id="aab14-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="aab14-119">När du har lagt till regeln behåller vi den ändrade Azure Network Security-gruppen.</span><span class="sxs-lookup"><span data-stu-id="aab14-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="aab14-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aab14-120">PARAMETERS</span></span>

### <span data-ttu-id="aab14-121">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="aab14-121">-Access</span></span>
<span data-ttu-id="aab14-122">Anger om nätverks trafik tillåts eller nekas.</span><span class="sxs-lookup"><span data-stu-id="aab14-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="aab14-123">De acceptabla värdena för den här parametern är: Allow och Deny.</span><span class="sxs-lookup"><span data-stu-id="aab14-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="aab14-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab14-124">-DefaultProfile</span></span>
<span data-ttu-id="aab14-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aab14-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aab14-126">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="aab14-126">-Description</span></span>
<span data-ttu-id="aab14-127">Anger en beskrivning av en nätverks säkerhets regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="aab14-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="aab14-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="aab14-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="aab14-129">Anger ett prefix för mål adress.</span><span class="sxs-lookup"><span data-stu-id="aab14-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="aab14-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="aab14-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aab14-131">CIDR-adress (Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="aab14-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="aab14-132">Ett mål-IP-adressintervall</span><span class="sxs-lookup"><span data-stu-id="aab14-132">A destination IP address range</span></span>
- <span data-ttu-id="aab14-133">Ett jokertecken (\*) för att matcha en IP-adress du kan använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="aab14-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="aab14-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aab14-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="aab14-135">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="aab14-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="aab14-136">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="aab14-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="aab14-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="aab14-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="aab14-138">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="aab14-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="aab14-139">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="aab14-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="aab14-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="aab14-140">-DestinationPortRange</span></span>
<span data-ttu-id="aab14-141">Anger en målport eller ett område.</span><span class="sxs-lookup"><span data-stu-id="aab14-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="aab14-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="aab14-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aab14-143">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="aab14-143">An integer</span></span>
- <span data-ttu-id="aab14-144">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="aab14-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="aab14-145">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="aab14-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="aab14-146">-Riktning</span><span class="sxs-lookup"><span data-stu-id="aab14-146">-Direction</span></span>
<span data-ttu-id="aab14-147">Anger om en regel utvärderas för inkommande eller utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="aab14-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="aab14-148">De acceptabla värdena för den här parametern är: inkommande och utgående.</span><span class="sxs-lookup"><span data-stu-id="aab14-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="aab14-149">-Namn</span><span class="sxs-lookup"><span data-stu-id="aab14-149">-Name</span></span>
<span data-ttu-id="aab14-150">Anger namnet på en nätverks säkerhets regel.</span><span class="sxs-lookup"><span data-stu-id="aab14-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="aab14-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aab14-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="aab14-152">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="aab14-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="aab14-153">Denna cmdlet lägger till en nätverks säkerhets regel för det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="aab14-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="aab14-154">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="aab14-154">-Priority</span></span>
<span data-ttu-id="aab14-155">Anger prioriteten för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="aab14-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="aab14-156">De acceptabla värdena för den här parametern är: ett heltal mellan 100 och 4096.</span><span class="sxs-lookup"><span data-stu-id="aab14-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="aab14-157">Prioritets numret måste vara unikt för varje regel i samlingen.</span><span class="sxs-lookup"><span data-stu-id="aab14-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="aab14-158">Ju lägre prioritets nummer desto högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="aab14-158">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="aab14-159">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="aab14-159">-Protocol</span></span>
<span data-ttu-id="aab14-160">Anger det nätverks protokoll som en regel konfiguration gäller för.</span><span class="sxs-lookup"><span data-stu-id="aab14-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="aab14-161">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="aab14-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aab14-162">TCP</span><span class="sxs-lookup"><span data-stu-id="aab14-162">Tcp</span></span>
- <span data-ttu-id="aab14-163">UDP</span><span class="sxs-lookup"><span data-stu-id="aab14-163">Udp</span></span>
- <span data-ttu-id="aab14-164">Jokertecken (\*) för att matcha båda</span><span class="sxs-lookup"><span data-stu-id="aab14-164">Wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="aab14-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="aab14-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="aab14-166">Anger ett käll adress prefix.</span><span class="sxs-lookup"><span data-stu-id="aab14-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="aab14-167">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="aab14-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aab14-168">EN CIDR</span><span class="sxs-lookup"><span data-stu-id="aab14-168">A CIDR</span></span>
- <span data-ttu-id="aab14-169">Ett käll-IP-intervall</span><span class="sxs-lookup"><span data-stu-id="aab14-169">A source IP range</span></span>
- <span data-ttu-id="aab14-170">Ett jokertecken (\*) för att matcha alla IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="aab14-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="aab14-171">Du kan också använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="aab14-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="aab14-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aab14-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="aab14-173">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="aab14-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="aab14-174">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="aab14-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="aab14-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="aab14-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="aab14-176">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="aab14-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="aab14-177">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="aab14-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="aab14-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="aab14-178">-SourcePortRange</span></span>
<span data-ttu-id="aab14-179">Anger en källport eller ett område.</span><span class="sxs-lookup"><span data-stu-id="aab14-179">Specifies a source port or range.</span></span>
<span data-ttu-id="aab14-180">Det här värdet uttrycks som ett heltal, som ett intervall mellan 0 och 65535, eller som ett jokertecken (\*) för att matcha alla käll portar.</span><span class="sxs-lookup"><span data-stu-id="aab14-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="aab14-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab14-181">CommonParameters</span></span>
<span data-ttu-id="aab14-182">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aab14-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab14-183">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aab14-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab14-184">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aab14-184">INPUTS</span></span>

### <span data-ttu-id="aab14-185">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aab14-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="aab14-186">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aab14-186">OUTPUTS</span></span>

### <span data-ttu-id="aab14-187">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aab14-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="aab14-188">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aab14-188">NOTES</span></span>

## <span data-ttu-id="aab14-189">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aab14-189">RELATED LINKS</span></span>

[<span data-ttu-id="aab14-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aab14-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="aab14-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aab14-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="aab14-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aab14-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="aab14-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aab14-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


