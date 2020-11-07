---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 14af257cf6c5d5e547f81b76fd82a910580b3790
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578115"
---
# <span data-ttu-id="289f7-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="289f7-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="289f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="289f7-102">SYNOPSIS</span></span>
<span data-ttu-id="289f7-103">Skapar en nätverks säkerhets regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="289f7-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="289f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="289f7-104">SYNTAX</span></span>

### <span data-ttu-id="289f7-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="289f7-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="289f7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="289f7-106">SetByResourceId</span></span>
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

## <span data-ttu-id="289f7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="289f7-107">DESCRIPTION</span></span>
<span data-ttu-id="289f7-108">Cmdleten **New-AzureRmNetworkSecurityRuleConfig** skapar en Azure Network Security Rule-konfiguration för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="289f7-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="289f7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="289f7-109">EXAMPLES</span></span>

### <span data-ttu-id="289f7-110">1: skapa en nätverks säkerhets regel för att tillåta RDP</span><span class="sxs-lookup"><span data-stu-id="289f7-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="289f7-111">Det här kommandot skapar en säkerhets regel som tillåter åtkomst från Internet till port 3389</span><span class="sxs-lookup"><span data-stu-id="289f7-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="289f7-112">2: skapa en nätverks säkerhets regel som tillåter HTTP</span><span class="sxs-lookup"><span data-stu-id="289f7-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="289f7-113">Det här kommandot skapar en säkerhets regel som tillåter åtkomst från Internet till port 80</span><span class="sxs-lookup"><span data-stu-id="289f7-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="289f7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="289f7-114">PARAMETERS</span></span>

### <span data-ttu-id="289f7-115">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="289f7-115">-Access</span></span>
<span data-ttu-id="289f7-116">Anger om nätverks trafik tillåts eller nekas.</span><span class="sxs-lookup"><span data-stu-id="289f7-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="289f7-117">De acceptabla värdena för den här parametern är: Allow och Deny.</span><span class="sxs-lookup"><span data-stu-id="289f7-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="289f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="289f7-118">-DefaultProfile</span></span>
<span data-ttu-id="289f7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="289f7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="289f7-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="289f7-120">-Description</span></span>
<span data-ttu-id="289f7-121">Anger en beskrivning av nätverks säkerhets regelns konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="289f7-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="289f7-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="289f7-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="289f7-123">Anger ett prefix för mål adress.</span><span class="sxs-lookup"><span data-stu-id="289f7-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="289f7-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="289f7-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="289f7-125">CIDR-adress (Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="289f7-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="289f7-126">Ett mål-IP-adressintervall</span><span class="sxs-lookup"><span data-stu-id="289f7-126">A destination IP address range</span></span> 
- <span data-ttu-id="289f7-127">Ett jokertecken (\*) för att matcha alla IP-adresser</span><span class="sxs-lookup"><span data-stu-id="289f7-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="289f7-128">Du kan använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="289f7-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="289f7-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="289f7-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="289f7-130">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="289f7-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="289f7-131">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="289f7-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="289f7-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="289f7-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="289f7-133">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="289f7-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="289f7-134">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="289f7-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="289f7-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="289f7-135">-DestinationPortRange</span></span>
<span data-ttu-id="289f7-136">Anger en målport eller ett område.</span><span class="sxs-lookup"><span data-stu-id="289f7-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="289f7-137">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="289f7-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="289f7-138">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="289f7-138">An integer</span></span>
- <span data-ttu-id="289f7-139">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="289f7-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="289f7-140">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="289f7-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="289f7-141">-Riktning</span><span class="sxs-lookup"><span data-stu-id="289f7-141">-Direction</span></span>
<span data-ttu-id="289f7-142">Anger om en regel utvärderas för inkommande eller utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="289f7-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="289f7-143">De acceptabla värdena för den här parametern är: inkommande och utgående.</span><span class="sxs-lookup"><span data-stu-id="289f7-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="289f7-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="289f7-144">-Name</span></span>
<span data-ttu-id="289f7-145">Anger namnet på den nätverks säkerhets regel som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="289f7-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="289f7-146">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="289f7-146">-Priority</span></span>
<span data-ttu-id="289f7-147">Anger prioriteten för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="289f7-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="289f7-148">De acceptabla värdena för den här parametern är: ett heltal mellan 100 och 4096.</span><span class="sxs-lookup"><span data-stu-id="289f7-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="289f7-149">Prioritets numret måste vara unikt för varje regel i samlingen.</span><span class="sxs-lookup"><span data-stu-id="289f7-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="289f7-150">Ju lägre prioritets nummer desto högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="289f7-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="289f7-151">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="289f7-151">-Protocol</span></span>
<span data-ttu-id="289f7-152">Anger det nätverks protokoll som en ny regel konfiguration gäller för.</span><span class="sxs-lookup"><span data-stu-id="289f7-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="289f7-153">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="289f7-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="289f7-154">TCP</span><span class="sxs-lookup"><span data-stu-id="289f7-154">Tcp</span></span>
- <span data-ttu-id="289f7-155">UDP</span><span class="sxs-lookup"><span data-stu-id="289f7-155">Udp</span></span>
- <span data-ttu-id="289f7-156">jokertecken (\*) för att passa båda.</span><span class="sxs-lookup"><span data-stu-id="289f7-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="289f7-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="289f7-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="289f7-158">Anger ett käll adress prefix.</span><span class="sxs-lookup"><span data-stu-id="289f7-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="289f7-159">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="289f7-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="289f7-160">EN CIDR</span><span class="sxs-lookup"><span data-stu-id="289f7-160">A CIDR</span></span>
- <span data-ttu-id="289f7-161">Ett käll-IP-intervall</span><span class="sxs-lookup"><span data-stu-id="289f7-161">A source IP range</span></span>
- <span data-ttu-id="289f7-162">Ett jokertecken (\*) för att matcha alla IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="289f7-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="289f7-163">Du kan också använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="289f7-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="289f7-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="289f7-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="289f7-165">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="289f7-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="289f7-166">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="289f7-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="289f7-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="289f7-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="289f7-168">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="289f7-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="289f7-169">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="289f7-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="289f7-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="289f7-170">-SourcePortRange</span></span>
<span data-ttu-id="289f7-171">Anger käll port eller-intervall.</span><span class="sxs-lookup"><span data-stu-id="289f7-171">Specifies the source port or range.</span></span>
<span data-ttu-id="289f7-172">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="289f7-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="289f7-173">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="289f7-173">An integer</span></span>
- <span data-ttu-id="289f7-174">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="289f7-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="289f7-175">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="289f7-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="289f7-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="289f7-176">CommonParameters</span></span>
<span data-ttu-id="289f7-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="289f7-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="289f7-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="289f7-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="289f7-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="289f7-179">INPUTS</span></span>

### <span data-ttu-id="289f7-180">Ingen</span><span class="sxs-lookup"><span data-stu-id="289f7-180">None</span></span>
<span data-ttu-id="289f7-181">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="289f7-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="289f7-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="289f7-182">OUTPUTS</span></span>

### <span data-ttu-id="289f7-183">Microsoft. Azure. commands. Networks. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="289f7-183">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="289f7-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="289f7-184">NOTES</span></span>

## <span data-ttu-id="289f7-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="289f7-185">RELATED LINKS</span></span>

[<span data-ttu-id="289f7-186">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="289f7-186">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="289f7-187">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="289f7-187">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="289f7-188">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="289f7-188">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="289f7-189">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="289f7-189">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

