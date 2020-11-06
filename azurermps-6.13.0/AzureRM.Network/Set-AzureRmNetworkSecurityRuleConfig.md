---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: f9c0e2b2071bdcae348d6bbd5237a355601e9fad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576157"
---
# <span data-ttu-id="3730a-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3730a-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="3730a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3730a-102">SYNOPSIS</span></span>
<span data-ttu-id="3730a-103">Anger mål tillstånd för en nätverks säkerhets regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3730a-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3730a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3730a-104">SYNTAX</span></span>

### <span data-ttu-id="3730a-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="3730a-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="3730a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3730a-106">SetByResourceId</span></span>
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

## <span data-ttu-id="3730a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3730a-107">DESCRIPTION</span></span>
<span data-ttu-id="3730a-108">Cmdleten **set-AzureRmNetworkSecurityRuleConfig** anger mål tillståndet för en Azure Network Security Rule-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3730a-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="3730a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3730a-109">EXAMPLES</span></span>

### <span data-ttu-id="3730a-110">Exempel 1: ändra åtkomst konfigurationen i en nätverks säkerhets regel</span><span class="sxs-lookup"><span data-stu-id="3730a-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="3730a-111">Det första kommandot får nätverks säkerhets gruppen med namnet NSG-klient del och lagrar den sedan i variabeln $nsg.</span><span class="sxs-lookup"><span data-stu-id="3730a-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="3730a-112">Det andra kommandot använder pipeline-operatorn för att överföra säkerhets gruppen i $nsg till get-AzureRmNetworkSecurityRuleConfig, som hämtar säkerhets regel konfigurationen med namnet RDP-regel.</span><span class="sxs-lookup"><span data-stu-id="3730a-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="3730a-113">Det tredje kommandot ändrar åtkomst konfigurationen för RDP-regeln för att neka.</span><span class="sxs-lookup"><span data-stu-id="3730a-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="3730a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3730a-114">PARAMETERS</span></span>

### <span data-ttu-id="3730a-115">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="3730a-115">-Access</span></span>
<span data-ttu-id="3730a-116">Anger om nätverks trafik tillåts eller nekas.</span><span class="sxs-lookup"><span data-stu-id="3730a-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="3730a-117">De acceptabla värdena för den här parametern är: Allow och Deny.</span><span class="sxs-lookup"><span data-stu-id="3730a-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="3730a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3730a-118">-DefaultProfile</span></span>
<span data-ttu-id="3730a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3730a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3730a-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3730a-120">-Description</span></span>
<span data-ttu-id="3730a-121">Anger en beskrivning av en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3730a-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="3730a-122">Maximal storlek är 140 tecken.</span><span class="sxs-lookup"><span data-stu-id="3730a-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="3730a-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3730a-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="3730a-124">Anger ett prefix för mål adress.</span><span class="sxs-lookup"><span data-stu-id="3730a-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="3730a-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3730a-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3730a-126">CIDR-adress (Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="3730a-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="3730a-127">Ett mål-IP-adressintervall</span><span class="sxs-lookup"><span data-stu-id="3730a-127">A destination IP address range</span></span> 
- <span data-ttu-id="3730a-128">Ett jokertecken (\*) för att matcha en IP-adress du kan använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="3730a-128">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="3730a-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3730a-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="3730a-130">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="3730a-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="3730a-131">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="3730a-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3730a-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3730a-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="3730a-133">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="3730a-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="3730a-134">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="3730a-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3730a-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="3730a-135">-DestinationPortRange</span></span>
<span data-ttu-id="3730a-136">Anger en målport eller ett område.</span><span class="sxs-lookup"><span data-stu-id="3730a-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="3730a-137">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3730a-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3730a-138">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="3730a-138">An integer</span></span> 
- <span data-ttu-id="3730a-139">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="3730a-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="3730a-140">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="3730a-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="3730a-141">-Riktning</span><span class="sxs-lookup"><span data-stu-id="3730a-141">-Direction</span></span>
<span data-ttu-id="3730a-142">Anger om en regel utvärderas för inkommande och utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="3730a-142">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="3730a-143">De acceptabla värdena för den här parametern är: inkommande och utgående.</span><span class="sxs-lookup"><span data-stu-id="3730a-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="3730a-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="3730a-144">-Name</span></span>
<span data-ttu-id="3730a-145">Anger namnet på den nätverks säkerhets regel som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="3730a-145">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="3730a-146">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3730a-146">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3730a-147">Anger det **NetworkSecurityGroup** -objekt som innehåller nätverks säkerhets regel konfigurationen som ska anges.</span><span class="sxs-lookup"><span data-stu-id="3730a-147">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="3730a-148">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="3730a-148">-Priority</span></span>
<span data-ttu-id="3730a-149">Anger prioriteten för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3730a-149">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="3730a-150">De acceptabla värdena för den här parametern är: ett heltal mellan 100 och 4096.</span><span class="sxs-lookup"><span data-stu-id="3730a-150">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="3730a-151">Prioritets numret måste vara unikt för varje regel i samlingen.</span><span class="sxs-lookup"><span data-stu-id="3730a-151">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="3730a-152">Ju lägre prioritets nummer desto högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="3730a-152">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="3730a-153">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3730a-153">-Protocol</span></span>
<span data-ttu-id="3730a-154">Anger det nätverks protokoll som en regel konfiguration gäller för.</span><span class="sxs-lookup"><span data-stu-id="3730a-154">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="3730a-155">De acceptabla värdena för denna parameter är:--TCP</span><span class="sxs-lookup"><span data-stu-id="3730a-155">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="3730a-156">UDP</span><span class="sxs-lookup"><span data-stu-id="3730a-156">Udp</span></span>
- <span data-ttu-id="3730a-157">Ett jokertecken (\*) för att matcha båda</span><span class="sxs-lookup"><span data-stu-id="3730a-157">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="3730a-158">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3730a-158">-SourceAddressPrefix</span></span>
<span data-ttu-id="3730a-159">Anger ett käll adress prefix.</span><span class="sxs-lookup"><span data-stu-id="3730a-159">Specifies a source address prefix.</span></span>
<span data-ttu-id="3730a-160">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3730a-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3730a-161">EN CIDR</span><span class="sxs-lookup"><span data-stu-id="3730a-161">A CIDR</span></span>
- <span data-ttu-id="3730a-162">Ett käll-IP-intervall</span><span class="sxs-lookup"><span data-stu-id="3730a-162">A source IP range</span></span>
- <span data-ttu-id="3730a-163">Ett jokertecken (\*) för att matcha en IP-adress du kan också använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="3730a-163">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="3730a-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3730a-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="3730a-165">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="3730a-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="3730a-166">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="3730a-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3730a-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3730a-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="3730a-168">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="3730a-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="3730a-169">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="3730a-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3730a-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="3730a-170">-SourcePortRange</span></span>
<span data-ttu-id="3730a-171">Anger käll port eller-intervall.</span><span class="sxs-lookup"><span data-stu-id="3730a-171">Specifies the source port or range.</span></span>
<span data-ttu-id="3730a-172">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3730a-172">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3730a-173">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="3730a-173">An integer</span></span>
- <span data-ttu-id="3730a-174">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="3730a-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="3730a-175">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="3730a-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="3730a-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3730a-176">CommonParameters</span></span>
<span data-ttu-id="3730a-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3730a-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3730a-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3730a-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3730a-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3730a-179">INPUTS</span></span>

### <span data-ttu-id="3730a-180">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3730a-180">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="3730a-181">Parametrar: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3730a-181">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="3730a-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3730a-182">OUTPUTS</span></span>

### <span data-ttu-id="3730a-183">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3730a-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="3730a-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3730a-184">NOTES</span></span>

## <span data-ttu-id="3730a-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3730a-185">RELATED LINKS</span></span>

[<span data-ttu-id="3730a-186">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3730a-186">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3730a-187">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3730a-187">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3730a-188">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3730a-188">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3730a-189">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3730a-189">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)


