---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 963dc6391ef5f500b26068e2a407eacd64ce6c16
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924185"
---
# <span data-ttu-id="36d9e-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36d9e-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="36d9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="36d9e-103">Anger mål tillstånd för en nätverks säkerhets regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="36d9e-103">Sets the goal state for a network security rule configuration.</span></span>

## <span data-ttu-id="36d9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36d9e-104">SYNTAX</span></span>

### <span data-ttu-id="36d9e-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="36d9e-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
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

### <span data-ttu-id="36d9e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="36d9e-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36d9e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36d9e-107">DESCRIPTION</span></span>
<span data-ttu-id="36d9e-108">Cmdleten **set-AzNetworkSecurityRuleConfig** anger mål tillståndet för en Azure Network Security Rule-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="36d9e-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="36d9e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36d9e-109">EXAMPLES</span></span>

### <span data-ttu-id="36d9e-110">Exempel 1: ändra åtkomst konfigurationen i en nätverks säkerhets regel</span><span class="sxs-lookup"><span data-stu-id="36d9e-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="36d9e-111">Det första kommandot får nätverks säkerhets gruppen med namnet NSG-klient del och lagrar den sedan i variabeln $nsg.</span><span class="sxs-lookup"><span data-stu-id="36d9e-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="36d9e-112">Det andra kommandot använder pipeline-operatorn för att överföra säkerhets gruppen i $nsg till get-AzNetworkSecurityRuleConfig, som hämtar säkerhets regel konfigurationen med namnet RDP-regel.</span><span class="sxs-lookup"><span data-stu-id="36d9e-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="36d9e-113">Det tredje kommandot ändrar åtkomst konfigurationen för RDP-regeln för att neka.</span><span class="sxs-lookup"><span data-stu-id="36d9e-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="36d9e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36d9e-114">PARAMETERS</span></span>

### <span data-ttu-id="36d9e-115">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="36d9e-115">-Access</span></span>
<span data-ttu-id="36d9e-116">Anger om nätverks trafik tillåts eller nekas.</span><span class="sxs-lookup"><span data-stu-id="36d9e-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="36d9e-117">De acceptabla värdena för den här parametern är: Allow och Deny.</span><span class="sxs-lookup"><span data-stu-id="36d9e-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="36d9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d9e-118">-DefaultProfile</span></span>
<span data-ttu-id="36d9e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36d9e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36d9e-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="36d9e-120">-Description</span></span>
<span data-ttu-id="36d9e-121">Anger en beskrivning av en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="36d9e-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="36d9e-122">Maximal storlek är 140 tecken.</span><span class="sxs-lookup"><span data-stu-id="36d9e-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="36d9e-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="36d9e-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="36d9e-124">Anger ett prefix för mål adress.</span><span class="sxs-lookup"><span data-stu-id="36d9e-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="36d9e-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="36d9e-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36d9e-126">CIDR-adress (Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="36d9e-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="36d9e-127">Ett mål-IP-adressintervall</span><span class="sxs-lookup"><span data-stu-id="36d9e-127">A destination IP address range</span></span> 
- <span data-ttu-id="36d9e-128">Ett jokertecken (\*) för att matcha alla IP-adresser</span><span class="sxs-lookup"><span data-stu-id="36d9e-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="36d9e-129">Du kan använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="36d9e-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="36d9e-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="36d9e-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="36d9e-131">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="36d9e-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="36d9e-132">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="36d9e-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="36d9e-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="36d9e-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="36d9e-134">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="36d9e-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="36d9e-135">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="36d9e-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="36d9e-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="36d9e-136">-DestinationPortRange</span></span>
<span data-ttu-id="36d9e-137">Anger en målport eller ett område.</span><span class="sxs-lookup"><span data-stu-id="36d9e-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="36d9e-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="36d9e-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36d9e-139">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="36d9e-139">An integer</span></span> 
- <span data-ttu-id="36d9e-140">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="36d9e-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="36d9e-141">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="36d9e-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="36d9e-142">-Riktning</span><span class="sxs-lookup"><span data-stu-id="36d9e-142">-Direction</span></span>
<span data-ttu-id="36d9e-143">Anger om en regel utvärderas för inkommande och utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="36d9e-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="36d9e-144">De acceptabla värdena för den här parametern är: inkommande och utgående.</span><span class="sxs-lookup"><span data-stu-id="36d9e-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="36d9e-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="36d9e-145">-Name</span></span>
<span data-ttu-id="36d9e-146">Anger namnet på den nätverks säkerhets regel som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="36d9e-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="36d9e-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="36d9e-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="36d9e-148">Anger det **NetworkSecurityGroup** -objekt som innehåller nätverks säkerhets regel konfigurationen som ska anges.</span><span class="sxs-lookup"><span data-stu-id="36d9e-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="36d9e-149">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="36d9e-149">-Priority</span></span>
<span data-ttu-id="36d9e-150">Anger prioriteten för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="36d9e-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="36d9e-151">De acceptabla värdena för den här parametern är: ett heltal mellan 100 och 4096.</span><span class="sxs-lookup"><span data-stu-id="36d9e-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="36d9e-152">Prioritets numret måste vara unikt för varje regel i samlingen.</span><span class="sxs-lookup"><span data-stu-id="36d9e-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="36d9e-153">Ju lägre prioritets nummer desto högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="36d9e-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="36d9e-154">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="36d9e-154">-Protocol</span></span>
<span data-ttu-id="36d9e-155">Anger det nätverks protokoll som en regel konfiguration gäller för.</span><span class="sxs-lookup"><span data-stu-id="36d9e-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="36d9e-156">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="36d9e-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="36d9e-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="36d9e-157">--Tcp</span></span>
- <span data-ttu-id="36d9e-158">UDP</span><span class="sxs-lookup"><span data-stu-id="36d9e-158">Udp</span></span>
- <span data-ttu-id="36d9e-159">Ett jokertecken (\*) för att matcha båda</span><span class="sxs-lookup"><span data-stu-id="36d9e-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="36d9e-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="36d9e-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="36d9e-161">Anger ett käll adress prefix.</span><span class="sxs-lookup"><span data-stu-id="36d9e-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="36d9e-162">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="36d9e-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36d9e-163">EN CIDR</span><span class="sxs-lookup"><span data-stu-id="36d9e-163">A CIDR</span></span>
- <span data-ttu-id="36d9e-164">Ett käll-IP-intervall</span><span class="sxs-lookup"><span data-stu-id="36d9e-164">A source IP range</span></span>
- <span data-ttu-id="36d9e-165">Ett jokertecken (\*) för att matcha alla IP-adresser</span><span class="sxs-lookup"><span data-stu-id="36d9e-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="36d9e-166">Du kan också använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="36d9e-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="36d9e-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="36d9e-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="36d9e-168">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="36d9e-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="36d9e-169">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="36d9e-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="36d9e-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="36d9e-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="36d9e-171">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="36d9e-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="36d9e-172">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="36d9e-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="36d9e-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="36d9e-173">-SourcePortRange</span></span>
<span data-ttu-id="36d9e-174">Anger käll port eller-intervall.</span><span class="sxs-lookup"><span data-stu-id="36d9e-174">Specifies the source port or range.</span></span>
<span data-ttu-id="36d9e-175">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="36d9e-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36d9e-176">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="36d9e-176">An integer</span></span>
- <span data-ttu-id="36d9e-177">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="36d9e-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="36d9e-178">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="36d9e-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="36d9e-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d9e-179">CommonParameters</span></span>
<span data-ttu-id="36d9e-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36d9e-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d9e-181">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d9e-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d9e-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36d9e-182">INPUTS</span></span>

### <span data-ttu-id="36d9e-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="36d9e-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="36d9e-184">Parametern ' NetworkSecurityGroup ' godkänner värdet av typen ' PSNetworkSecurityGroup ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="36d9e-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="36d9e-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36d9e-185">OUTPUTS</span></span>

### <span data-ttu-id="36d9e-186">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="36d9e-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="36d9e-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36d9e-187">NOTES</span></span>

## <span data-ttu-id="36d9e-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36d9e-188">RELATED LINKS</span></span>

[<span data-ttu-id="36d9e-189">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36d9e-189">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="36d9e-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36d9e-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="36d9e-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36d9e-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="36d9e-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="36d9e-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


