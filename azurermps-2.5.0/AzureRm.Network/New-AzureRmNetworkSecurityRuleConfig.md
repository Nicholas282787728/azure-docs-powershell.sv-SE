---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 34397a467cb25a6b93963f8944096975663ccf5a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930177"
---
# <span data-ttu-id="7dafc-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7dafc-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="7dafc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7dafc-102">SYNOPSIS</span></span>
<span data-ttu-id="7dafc-103">Skapar en nätverks säkerhets regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7dafc-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dafc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7dafc-104">SYNTAX</span></span>

### <span data-ttu-id="7dafc-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="7dafc-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7dafc-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7dafc-106">SetByResourceId</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dafc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7dafc-107">DESCRIPTION</span></span>
<span data-ttu-id="7dafc-108">Cmdleten **New-AzureRmNetworkSecurityRuleConfig** skapar en Azure Network Security Rule-konfiguration för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="7dafc-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="7dafc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7dafc-109">EXAMPLES</span></span>

### <span data-ttu-id="7dafc-110">1: skapa en nätverks säkerhets regel för att tillåta RDP</span><span class="sxs-lookup"><span data-stu-id="7dafc-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="7dafc-111">Det här kommandot skapar en säkerhets regel som tillåter åtkomst från Internet till port 3389</span><span class="sxs-lookup"><span data-stu-id="7dafc-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="7dafc-112">2: skapa en nätverks säkerhets regel som tillåter HTTP</span><span class="sxs-lookup"><span data-stu-id="7dafc-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="7dafc-113">Det här kommandot skapar en säkerhets regel som tillåter åtkomst från Internet till port 80</span><span class="sxs-lookup"><span data-stu-id="7dafc-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="7dafc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7dafc-114">PARAMETERS</span></span>

### <span data-ttu-id="7dafc-115">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="7dafc-115">-Access</span></span>
<span data-ttu-id="7dafc-116">Anger om nätverks trafik tillåts eller nekas.</span><span class="sxs-lookup"><span data-stu-id="7dafc-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="7dafc-117">De acceptabla värdena för den här parametern är: Allow och Deny.</span><span class="sxs-lookup"><span data-stu-id="7dafc-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="7dafc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dafc-118">-DefaultProfile</span></span>
<span data-ttu-id="7dafc-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7dafc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dafc-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="7dafc-120">-Description</span></span>
<span data-ttu-id="7dafc-121">Anger en beskrivning av nätverks säkerhets regelns konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="7dafc-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="7dafc-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7dafc-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="7dafc-123">Anger ett prefix för mål adress.</span><span class="sxs-lookup"><span data-stu-id="7dafc-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="7dafc-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7dafc-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7dafc-125">CIDR-adress (Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="7dafc-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="7dafc-126">Ett mål-IP-adressintervall</span><span class="sxs-lookup"><span data-stu-id="7dafc-126">A destination IP address range</span></span> 
- <span data-ttu-id="7dafc-127">Ett jokertecken (\*) för att matcha alla IP-adresser</span><span class="sxs-lookup"><span data-stu-id="7dafc-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="7dafc-128">Du kan använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="7dafc-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="7dafc-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7dafc-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="7dafc-130">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="7dafc-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="7dafc-131">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="7dafc-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7dafc-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7dafc-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="7dafc-133">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="7dafc-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="7dafc-134">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="7dafc-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7dafc-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="7dafc-135">-DestinationPortRange</span></span>
<span data-ttu-id="7dafc-136">Anger en målport eller ett område.</span><span class="sxs-lookup"><span data-stu-id="7dafc-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="7dafc-137">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7dafc-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7dafc-138">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="7dafc-138">An integer</span></span>
- <span data-ttu-id="7dafc-139">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="7dafc-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="7dafc-140">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="7dafc-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="7dafc-141">-Riktning</span><span class="sxs-lookup"><span data-stu-id="7dafc-141">-Direction</span></span>
<span data-ttu-id="7dafc-142">Anger om en regel utvärderas för inkommande eller utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="7dafc-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="7dafc-143">De acceptabla värdena för den här parametern är: inkommande och utgående.</span><span class="sxs-lookup"><span data-stu-id="7dafc-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="7dafc-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="7dafc-144">-Name</span></span>
<span data-ttu-id="7dafc-145">Anger namnet på den nätverks säkerhets regel som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="7dafc-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7dafc-146">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="7dafc-146">-Priority</span></span>
<span data-ttu-id="7dafc-147">Anger prioriteten för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7dafc-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="7dafc-148">De acceptabla värdena för den här parametern är: ett heltal mellan 100 och 4096.</span><span class="sxs-lookup"><span data-stu-id="7dafc-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="7dafc-149">Prioritets numret måste vara unikt för varje regel i samlingen.</span><span class="sxs-lookup"><span data-stu-id="7dafc-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="7dafc-150">Ju lägre prioritets nummer desto högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="7dafc-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="7dafc-151">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7dafc-151">-Protocol</span></span>
<span data-ttu-id="7dafc-152">Anger det nätverks protokoll som en ny regel konfiguration gäller för.</span><span class="sxs-lookup"><span data-stu-id="7dafc-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="7dafc-153">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7dafc-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7dafc-154">TCP</span><span class="sxs-lookup"><span data-stu-id="7dafc-154">Tcp</span></span>
- <span data-ttu-id="7dafc-155">UDP</span><span class="sxs-lookup"><span data-stu-id="7dafc-155">Udp</span></span>
- <span data-ttu-id="7dafc-156">jokertecken (\*) för att passa båda.</span><span class="sxs-lookup"><span data-stu-id="7dafc-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="7dafc-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7dafc-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="7dafc-158">Anger ett käll adress prefix.</span><span class="sxs-lookup"><span data-stu-id="7dafc-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="7dafc-159">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7dafc-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7dafc-160">EN CIDR</span><span class="sxs-lookup"><span data-stu-id="7dafc-160">A CIDR</span></span>
- <span data-ttu-id="7dafc-161">Ett käll-IP-intervall</span><span class="sxs-lookup"><span data-stu-id="7dafc-161">A source IP range</span></span>
- <span data-ttu-id="7dafc-162">Ett jokertecken (\*) för att matcha alla IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="7dafc-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="7dafc-163">Du kan också använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="7dafc-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="7dafc-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7dafc-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="7dafc-165">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="7dafc-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="7dafc-166">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="7dafc-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7dafc-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7dafc-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="7dafc-168">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="7dafc-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="7dafc-169">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="7dafc-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7dafc-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="7dafc-170">-SourcePortRange</span></span>
<span data-ttu-id="7dafc-171">Anger käll port eller-intervall.</span><span class="sxs-lookup"><span data-stu-id="7dafc-171">Specifies the source port or range.</span></span>
<span data-ttu-id="7dafc-172">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7dafc-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7dafc-173">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="7dafc-173">An integer</span></span>
- <span data-ttu-id="7dafc-174">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="7dafc-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="7dafc-175">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="7dafc-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="7dafc-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dafc-176">CommonParameters</span></span>
<span data-ttu-id="7dafc-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dafc-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dafc-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dafc-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dafc-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7dafc-179">INPUTS</span></span>

## <span data-ttu-id="7dafc-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7dafc-180">OUTPUTS</span></span>

### <span data-ttu-id="7dafc-181">Microsoft. Azure. commands. Networks. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="7dafc-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="7dafc-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7dafc-182">NOTES</span></span>

## <span data-ttu-id="7dafc-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7dafc-183">RELATED LINKS</span></span>

[<span data-ttu-id="7dafc-184">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7dafc-184">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7dafc-185">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7dafc-185">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7dafc-186">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7dafc-186">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7dafc-187">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7dafc-187">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


