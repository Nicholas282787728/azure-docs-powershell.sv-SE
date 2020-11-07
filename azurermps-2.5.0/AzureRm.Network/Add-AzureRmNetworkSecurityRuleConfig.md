---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: bf796547f0dddc6b7a51d32d4d10f056df37ef1c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929402"
---
# <span data-ttu-id="c066f-101">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c066f-101">Add-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="c066f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c066f-102">SYNOPSIS</span></span>
<span data-ttu-id="c066f-103">Lägger till en nätverks säkerhets regel i en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="c066f-103">Adds a network security rule configuration to a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c066f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c066f-104">SYNTAX</span></span>

### <span data-ttu-id="c066f-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="c066f-105">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c066f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c066f-106">SetByResourceId</span></span>
```
Add-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c066f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c066f-107">DESCRIPTION</span></span>
<span data-ttu-id="c066f-108">Cmdleten **Add-AzureRmNetworkSecurityRuleConfig** lägger till en nätverks säkerhets regel konfiguration i en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="c066f-108">The **Add-AzureRmNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="c066f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c066f-109">EXAMPLES</span></span>

### <span data-ttu-id="c066f-110">1: lägga till en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="c066f-110">1: Adding a network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 | 
Add-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="c066f-111">Det första kommandot hämtar en Azure nätverks säkerhets grupp med namnet "nsg1" från resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="c066f-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="c066f-112">Det andra kommandot lägger till en nätverks säkerhets regel med namnet "RDP-Rule" som tillåter trafik från Internet på port 3389 till det hämtade objektet för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="c066f-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="c066f-113">Behåller den ändrade Azure Network Security-gruppen.</span><span class="sxs-lookup"><span data-stu-id="c066f-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="c066f-114">1: lägga till en ny säkerhets regel med program säkerhets grupper</span><span class="sxs-lookup"><span data-stu-id="c066f-114">1: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 |
Add-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="c066f-115">Först skapar vi två nya program säkerhets grupper.</span><span class="sxs-lookup"><span data-stu-id="c066f-115">First, we create two new application security groups.</span></span> <span data-ttu-id="c066f-116">Sedan hämtar vi en Azure nätverks säkerhets grupp med namnet "nsg1" från resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="c066f-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="c066f-117">och Lägg till en nätverks säkerhets regel med namnet "RDP-Rule" till den.</span><span class="sxs-lookup"><span data-stu-id="c066f-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="c066f-118">Regeln tillåter trafik från alla IP-konfigurationer i program säkerhets gruppen "srcAsg" till alla IP-konfigurationer i "destAsg" på port 3389.</span><span class="sxs-lookup"><span data-stu-id="c066f-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="c066f-119">När du har lagt till regeln behåller vi den ändrade Azure Network Security-gruppen.</span><span class="sxs-lookup"><span data-stu-id="c066f-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="c066f-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c066f-120">PARAMETERS</span></span>

### <span data-ttu-id="c066f-121">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="c066f-121">-Access</span></span>
<span data-ttu-id="c066f-122">Anger om nätverks trafik tillåts eller nekas.</span><span class="sxs-lookup"><span data-stu-id="c066f-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="c066f-123">De acceptabla värdena för den här parametern är: Allow och Deny.</span><span class="sxs-lookup"><span data-stu-id="c066f-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c066f-124">-DefaultProfile</span></span>
<span data-ttu-id="c066f-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c066f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c066f-126">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c066f-126">-Description</span></span>
<span data-ttu-id="c066f-127">Anger en beskrivning av en nätverks säkerhets regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c066f-127">Specifies a description of a network security rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c066f-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="c066f-129">Anger ett prefix för mål adress.</span><span class="sxs-lookup"><span data-stu-id="c066f-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="c066f-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c066f-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c066f-131">CIDR-adress (Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="c066f-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="c066f-132">Ett mål-IP-adressintervall</span><span class="sxs-lookup"><span data-stu-id="c066f-132">A destination IP address range</span></span>
- <span data-ttu-id="c066f-133">Ett jokertecken (\*) för att matcha alla IP-adresser</span><span class="sxs-lookup"><span data-stu-id="c066f-133">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="c066f-134">Du kan använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="c066f-134">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-135">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c066f-135">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="c066f-136">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="c066f-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="c066f-137">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="c066f-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-138">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c066f-138">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="c066f-139">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="c066f-139">The application security group set as destination for the rule.</span></span> <span data-ttu-id="c066f-140">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="c066f-140">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-141">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="c066f-141">-DestinationPortRange</span></span>
<span data-ttu-id="c066f-142">Anger en målport eller ett område.</span><span class="sxs-lookup"><span data-stu-id="c066f-142">Specifies a destination port or range.</span></span>
<span data-ttu-id="c066f-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c066f-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c066f-144">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="c066f-144">An integer</span></span>
- <span data-ttu-id="c066f-145">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="c066f-145">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="c066f-146">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="c066f-146">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-147">-Riktning</span><span class="sxs-lookup"><span data-stu-id="c066f-147">-Direction</span></span>
<span data-ttu-id="c066f-148">Anger om en regel utvärderas för inkommande eller utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="c066f-148">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="c066f-149">De acceptabla värdena för den här parametern är: inkommande och utgående.</span><span class="sxs-lookup"><span data-stu-id="c066f-149">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="c066f-150">-Name</span></span>
<span data-ttu-id="c066f-151">Anger namnet på en nätverks säkerhets regel.</span><span class="sxs-lookup"><span data-stu-id="c066f-151">Specifies the name of a network security rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-152">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c066f-152">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c066f-153">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c066f-153">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="c066f-154">Denna cmdlet lägger till en nätverks säkerhets regel för det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c066f-154">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-155">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="c066f-155">-Priority</span></span>
<span data-ttu-id="c066f-156">Anger prioriteten för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c066f-156">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="c066f-157">De acceptabla värdena för den här parametern är: ett heltal mellan 100 och 4096.</span><span class="sxs-lookup"><span data-stu-id="c066f-157">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="c066f-158">Prioritets numret måste vara unikt för varje regel i samlingen.</span><span class="sxs-lookup"><span data-stu-id="c066f-158">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="c066f-159">Ju lägre prioritets nummer desto högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="c066f-159">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-160">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c066f-160">-Protocol</span></span>
<span data-ttu-id="c066f-161">Anger det nätverks protokoll som en regel konfiguration gäller för.</span><span class="sxs-lookup"><span data-stu-id="c066f-161">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="c066f-162">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c066f-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c066f-163">TCP</span><span class="sxs-lookup"><span data-stu-id="c066f-163">Tcp</span></span>
- <span data-ttu-id="c066f-164">UDP</span><span class="sxs-lookup"><span data-stu-id="c066f-164">Udp</span></span>
- <span data-ttu-id="c066f-165">Jokertecken (\*) för att matcha båda</span><span class="sxs-lookup"><span data-stu-id="c066f-165">Wildcard character (\*) to match both</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-166">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c066f-166">-SourceAddressPrefix</span></span>
<span data-ttu-id="c066f-167">Anger ett käll adress prefix.</span><span class="sxs-lookup"><span data-stu-id="c066f-167">Specifies a source address prefix.</span></span>
<span data-ttu-id="c066f-168">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c066f-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c066f-169">EN CIDR</span><span class="sxs-lookup"><span data-stu-id="c066f-169">A CIDR</span></span>
- <span data-ttu-id="c066f-170">Ett käll-IP-intervall</span><span class="sxs-lookup"><span data-stu-id="c066f-170">A source IP range</span></span>
- <span data-ttu-id="c066f-171">Ett jokertecken (\*) för att matcha alla IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="c066f-171">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="c066f-172">Du kan också använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="c066f-172">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-173">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c066f-173">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="c066f-174">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="c066f-174">The application security group set as source for the rule.</span></span> <span data-ttu-id="c066f-175">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="c066f-175">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-176">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c066f-176">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="c066f-177">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="c066f-177">The application security group set as source for the rule.</span></span> <span data-ttu-id="c066f-178">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="c066f-178">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-179">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="c066f-179">-SourcePortRange</span></span>
<span data-ttu-id="c066f-180">Anger en källport eller ett område.</span><span class="sxs-lookup"><span data-stu-id="c066f-180">Specifies a source port or range.</span></span>
<span data-ttu-id="c066f-181">Det här värdet uttrycks som ett heltal, som ett intervall mellan 0 och 65535, eller som ett jokertecken (\*) för att matcha alla käll portar.</span><span class="sxs-lookup"><span data-stu-id="c066f-181">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c066f-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c066f-182">CommonParameters</span></span>
<span data-ttu-id="c066f-183">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c066f-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c066f-184">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c066f-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c066f-185">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c066f-185">INPUTS</span></span>

### <span data-ttu-id="c066f-186">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c066f-186">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="c066f-187">Parametern ' NetworkSecurityGroup ' godkänner värdet av typen ' PSNetworkSecurityGroup ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c066f-187">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="c066f-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c066f-188">OUTPUTS</span></span>

### <span data-ttu-id="c066f-189">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c066f-189">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="c066f-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c066f-190">NOTES</span></span>

## <span data-ttu-id="c066f-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c066f-191">RELATED LINKS</span></span>

[<span data-ttu-id="c066f-192">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c066f-192">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c066f-193">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c066f-193">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c066f-194">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c066f-194">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c066f-195">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c066f-195">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


