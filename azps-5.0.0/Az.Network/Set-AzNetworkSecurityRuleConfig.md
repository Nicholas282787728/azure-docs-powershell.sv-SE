---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269966"
---
# <span data-ttu-id="ff1cc-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff1cc-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="ff1cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff1cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff1cc-103">Uppdaterar en nätverks säkerhets regel för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="ff1cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff1cc-104">SYNTAX</span></span>

### <span data-ttu-id="ff1cc-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="ff1cc-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff1cc-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ff1cc-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff1cc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff1cc-107">DESCRIPTION</span></span>
<span data-ttu-id="ff1cc-108">Cmdleten **set-AzNetworkSecurityRuleConfig** uppdaterar en nätverks säkerhets regel för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="ff1cc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff1cc-109">EXAMPLES</span></span>

### <span data-ttu-id="ff1cc-110">Exempel 1: ändra åtkomst konfigurationen i en nätverks säkerhets regel</span><span class="sxs-lookup"><span data-stu-id="ff1cc-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="ff1cc-111">Det första kommandot får nätverks säkerhets gruppen med namnet NSG-klient del och lagrar den sedan i variabeln $nsg.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="ff1cc-112">Det andra kommandot använder pipeline-operatorn för att överföra säkerhets gruppen i $nsg till get-AzNetworkSecurityRuleConfig, som hämtar säkerhets regel konfigurationen med namnet RDP-regel.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="ff1cc-113">Det tredje kommandot ändrar åtkomst konfigurationen för RDP-regeln för att neka.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="ff1cc-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ff1cc-114">Example 2</span></span>

<span data-ttu-id="ff1cc-115">Uppdaterar en nätverks säkerhets regel för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="ff1cc-116">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="ff1cc-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="ff1cc-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff1cc-117">PARAMETERS</span></span>

### <span data-ttu-id="ff1cc-118">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="ff1cc-118">-Access</span></span>
<span data-ttu-id="ff1cc-119">Anger om nätverks trafik tillåts eller nekas.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="ff1cc-120">De acceptabla värdena för den här parametern är: Allow och Deny.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="ff1cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff1cc-121">-DefaultProfile</span></span>
<span data-ttu-id="ff1cc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff1cc-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ff1cc-123">-Description</span></span>
<span data-ttu-id="ff1cc-124">Anger en beskrivning av en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="ff1cc-125">Maximal storlek är 140 tecken.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="ff1cc-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ff1cc-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="ff1cc-127">Anger ett prefix för mål adress.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="ff1cc-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ff1cc-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff1cc-129">CIDR-adress (Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="ff1cc-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="ff1cc-130">Ett mål-IP-adressintervall</span><span class="sxs-lookup"><span data-stu-id="ff1cc-130">A destination IP address range</span></span> 
- <span data-ttu-id="ff1cc-131">Ett jokertecken (\*) för att matcha en IP-adress du kan använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="ff1cc-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ff1cc-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="ff1cc-133">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="ff1cc-134">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ff1cc-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ff1cc-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="ff1cc-136">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="ff1cc-137">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ff1cc-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="ff1cc-138">-DestinationPortRange</span></span>
<span data-ttu-id="ff1cc-139">Anger en målport eller ett område.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="ff1cc-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ff1cc-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff1cc-141">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="ff1cc-141">An integer</span></span> 
- <span data-ttu-id="ff1cc-142">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="ff1cc-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="ff1cc-143">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="ff1cc-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="ff1cc-144">-Riktning</span><span class="sxs-lookup"><span data-stu-id="ff1cc-144">-Direction</span></span>
<span data-ttu-id="ff1cc-145">Anger om en regel utvärderas för inkommande och utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="ff1cc-146">De acceptabla värdena för den här parametern är: inkommande och utgående.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="ff1cc-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff1cc-147">-Name</span></span>
<span data-ttu-id="ff1cc-148">Anger namnet på den nätverks säkerhets regel som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="ff1cc-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ff1cc-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ff1cc-150">Anger det **NetworkSecurityGroup** -objekt som innehåller nätverks säkerhets regel konfigurationen som ska anges.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="ff1cc-151">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="ff1cc-151">-Priority</span></span>
<span data-ttu-id="ff1cc-152">Anger prioriteten för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="ff1cc-153">De acceptabla värdena för den här parametern är: ett heltal mellan 100 och 4096.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="ff1cc-154">Prioritets numret måste vara unikt för varje regel i samlingen.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="ff1cc-155">Ju lägre prioritets nummer desto högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="ff1cc-156">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ff1cc-156">-Protocol</span></span>
<span data-ttu-id="ff1cc-157">Anger det nätverks protokoll som en regel konfiguration gäller för.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="ff1cc-158">De acceptabla värdena för denna parameter är:--TCP</span><span class="sxs-lookup"><span data-stu-id="ff1cc-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="ff1cc-159">UDP</span><span class="sxs-lookup"><span data-stu-id="ff1cc-159">Udp</span></span>
- <span data-ttu-id="ff1cc-160">Ett jokertecken (\*) för att matcha båda</span><span class="sxs-lookup"><span data-stu-id="ff1cc-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="ff1cc-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ff1cc-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="ff1cc-162">Anger ett käll adress prefix.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="ff1cc-163">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ff1cc-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff1cc-164">EN CIDR</span><span class="sxs-lookup"><span data-stu-id="ff1cc-164">A CIDR</span></span>
- <span data-ttu-id="ff1cc-165">Ett käll-IP-intervall</span><span class="sxs-lookup"><span data-stu-id="ff1cc-165">A source IP range</span></span>
- <span data-ttu-id="ff1cc-166">Ett jokertecken (\*) för att matcha en IP-adress du kan också använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="ff1cc-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ff1cc-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="ff1cc-168">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="ff1cc-169">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ff1cc-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ff1cc-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="ff1cc-171">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="ff1cc-172">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ff1cc-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="ff1cc-173">-SourcePortRange</span></span>
<span data-ttu-id="ff1cc-174">Anger käll port eller-intervall.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-174">Specifies the source port or range.</span></span>
<span data-ttu-id="ff1cc-175">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ff1cc-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff1cc-176">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="ff1cc-176">An integer</span></span>
- <span data-ttu-id="ff1cc-177">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="ff1cc-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="ff1cc-178">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="ff1cc-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="ff1cc-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff1cc-179">CommonParameters</span></span>
<span data-ttu-id="ff1cc-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff1cc-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff1cc-181">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff1cc-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff1cc-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff1cc-182">INPUTS</span></span>

### <span data-ttu-id="ff1cc-183">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ff1cc-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ff1cc-184">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff1cc-184">OUTPUTS</span></span>

### <span data-ttu-id="ff1cc-185">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ff1cc-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ff1cc-186">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff1cc-186">NOTES</span></span>

## <span data-ttu-id="ff1cc-187">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff1cc-187">RELATED LINKS</span></span>

[<span data-ttu-id="ff1cc-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff1cc-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ff1cc-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff1cc-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ff1cc-190">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff1cc-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ff1cc-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff1cc-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


