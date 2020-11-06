---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: fa1416d7bd65236d3a4e1198d6f70efb1a860985
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575965"
---
# <span data-ttu-id="cd352-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd352-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="cd352-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd352-102">SYNOPSIS</span></span>
<span data-ttu-id="cd352-103">Anger mål tillstånd för en nätverks säkerhets regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd352-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd352-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd352-104">SYNTAX</span></span>

### <span data-ttu-id="cd352-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="cd352-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
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

### <span data-ttu-id="cd352-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd352-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd352-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd352-107">DESCRIPTION</span></span>
<span data-ttu-id="cd352-108">Cmdleten **set-AzureRmNetworkSecurityRuleConfig** anger mål tillståndet för en Azure Network Security Rule-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd352-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="cd352-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd352-109">EXAMPLES</span></span>

### <span data-ttu-id="cd352-110">Exempel 1: ändra åtkomst konfigurationen i en nätverks säkerhets regel</span><span class="sxs-lookup"><span data-stu-id="cd352-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="cd352-111">Det första kommandot får nätverks säkerhets gruppen med namnet NSG-klient del och lagrar den sedan i variabeln $nsg.</span><span class="sxs-lookup"><span data-stu-id="cd352-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="cd352-112">Det andra kommandot använder pipeline-operatorn för att överföra säkerhets gruppen i $nsg till get-AzureRmNetworkSecurityRuleConfig, som hämtar säkerhets regel konfigurationen med namnet RDP-regel.</span><span class="sxs-lookup"><span data-stu-id="cd352-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="cd352-113">Det tredje kommandot ändrar åtkomst konfigurationen för RDP-regeln för att neka.</span><span class="sxs-lookup"><span data-stu-id="cd352-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="cd352-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd352-114">PARAMETERS</span></span>

### <span data-ttu-id="cd352-115">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="cd352-115">-Access</span></span>
<span data-ttu-id="cd352-116">Anger om nätverks trafik tillåts eller nekas.</span><span class="sxs-lookup"><span data-stu-id="cd352-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="cd352-117">De acceptabla värdena för den här parametern är: Allow och Deny.</span><span class="sxs-lookup"><span data-stu-id="cd352-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="cd352-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd352-118">-DefaultProfile</span></span>
<span data-ttu-id="cd352-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd352-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd352-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="cd352-120">-Description</span></span>
<span data-ttu-id="cd352-121">Anger en beskrivning av en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd352-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="cd352-122">Maximal storlek är 140 tecken.</span><span class="sxs-lookup"><span data-stu-id="cd352-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="cd352-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cd352-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="cd352-124">Anger ett prefix för mål adress.</span><span class="sxs-lookup"><span data-stu-id="cd352-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="cd352-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cd352-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cd352-126">CIDR-adress (Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="cd352-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="cd352-127">Ett mål-IP-adressintervall</span><span class="sxs-lookup"><span data-stu-id="cd352-127">A destination IP address range</span></span> 
- <span data-ttu-id="cd352-128">Ett jokertecken (\*) för att matcha alla IP-adresser</span><span class="sxs-lookup"><span data-stu-id="cd352-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="cd352-129">Du kan använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="cd352-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="cd352-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cd352-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="cd352-131">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="cd352-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="cd352-132">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="cd352-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cd352-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cd352-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="cd352-134">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="cd352-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="cd352-135">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="cd352-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cd352-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="cd352-136">-DestinationPortRange</span></span>
<span data-ttu-id="cd352-137">Anger en målport eller ett område.</span><span class="sxs-lookup"><span data-stu-id="cd352-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="cd352-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cd352-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cd352-139">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="cd352-139">An integer</span></span> 
- <span data-ttu-id="cd352-140">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="cd352-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="cd352-141">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="cd352-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="cd352-142">-Riktning</span><span class="sxs-lookup"><span data-stu-id="cd352-142">-Direction</span></span>
<span data-ttu-id="cd352-143">Anger om en regel utvärderas för inkommande och utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="cd352-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="cd352-144">De acceptabla värdena för den här parametern är: inkommande och utgående.</span><span class="sxs-lookup"><span data-stu-id="cd352-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="cd352-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd352-145">-Name</span></span>
<span data-ttu-id="cd352-146">Anger namnet på den nätverks säkerhets regel som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="cd352-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="cd352-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cd352-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="cd352-148">Anger det **NetworkSecurityGroup** -objekt som innehåller nätverks säkerhets regel konfigurationen som ska anges.</span><span class="sxs-lookup"><span data-stu-id="cd352-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="cd352-149">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="cd352-149">-Priority</span></span>
<span data-ttu-id="cd352-150">Anger prioriteten för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd352-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="cd352-151">De acceptabla värdena för den här parametern är: ett heltal mellan 100 och 4096.</span><span class="sxs-lookup"><span data-stu-id="cd352-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="cd352-152">Prioritets numret måste vara unikt för varje regel i samlingen.</span><span class="sxs-lookup"><span data-stu-id="cd352-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="cd352-153">Ju lägre prioritets nummer desto högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="cd352-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="cd352-154">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="cd352-154">-Protocol</span></span>
<span data-ttu-id="cd352-155">Anger det nätverks protokoll som en regel konfiguration gäller för.</span><span class="sxs-lookup"><span data-stu-id="cd352-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="cd352-156">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cd352-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="cd352-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="cd352-157">--Tcp</span></span>
- <span data-ttu-id="cd352-158">UDP</span><span class="sxs-lookup"><span data-stu-id="cd352-158">Udp</span></span>
- <span data-ttu-id="cd352-159">Ett jokertecken (\*) för att matcha båda</span><span class="sxs-lookup"><span data-stu-id="cd352-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="cd352-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cd352-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="cd352-161">Anger ett käll adress prefix.</span><span class="sxs-lookup"><span data-stu-id="cd352-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="cd352-162">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cd352-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cd352-163">EN CIDR</span><span class="sxs-lookup"><span data-stu-id="cd352-163">A CIDR</span></span>
- <span data-ttu-id="cd352-164">Ett käll-IP-intervall</span><span class="sxs-lookup"><span data-stu-id="cd352-164">A source IP range</span></span>
- <span data-ttu-id="cd352-165">Ett jokertecken (\*) för att matcha alla IP-adresser</span><span class="sxs-lookup"><span data-stu-id="cd352-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="cd352-166">Du kan också använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="cd352-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="cd352-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cd352-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="cd352-168">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="cd352-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="cd352-169">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="cd352-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cd352-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cd352-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="cd352-171">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="cd352-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="cd352-172">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="cd352-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cd352-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="cd352-173">-SourcePortRange</span></span>
<span data-ttu-id="cd352-174">Anger käll port eller-intervall.</span><span class="sxs-lookup"><span data-stu-id="cd352-174">Specifies the source port or range.</span></span>
<span data-ttu-id="cd352-175">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cd352-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cd352-176">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="cd352-176">An integer</span></span>
- <span data-ttu-id="cd352-177">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="cd352-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="cd352-178">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="cd352-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="cd352-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd352-179">CommonParameters</span></span>
<span data-ttu-id="cd352-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd352-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd352-181">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd352-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd352-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd352-182">INPUTS</span></span>

### <span data-ttu-id="cd352-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cd352-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="cd352-184">Parametern ' NetworkSecurityGroup ' godkänner värdet av typen ' PSNetworkSecurityGroup ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="cd352-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="cd352-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd352-185">OUTPUTS</span></span>

### <span data-ttu-id="cd352-186">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cd352-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="cd352-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd352-187">NOTES</span></span>

## <span data-ttu-id="cd352-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd352-188">RELATED LINKS</span></span>

[<span data-ttu-id="cd352-189">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd352-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cd352-190">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd352-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cd352-191">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd352-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cd352-192">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd352-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)


