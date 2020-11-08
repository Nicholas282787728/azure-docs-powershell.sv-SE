---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260731"
---
# <span data-ttu-id="3dffb-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dffb-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="3dffb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3dffb-102">SYNOPSIS</span></span>
<span data-ttu-id="3dffb-103">Skapar en nätverks säkerhets regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3dffb-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="3dffb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3dffb-104">SYNTAX</span></span>

### <span data-ttu-id="3dffb-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="3dffb-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dffb-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3dffb-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dffb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3dffb-107">DESCRIPTION</span></span>
<span data-ttu-id="3dffb-108">Cmdleten **New-AzNetworkSecurityRuleConfig** skapar en Azure Network Security Rule-konfiguration för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="3dffb-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="3dffb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3dffb-109">EXAMPLES</span></span>

### <span data-ttu-id="3dffb-110">Exempel 1: skapa en nätverks säkerhets regel för att tillåta RDP</span><span class="sxs-lookup"><span data-stu-id="3dffb-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="3dffb-111">Det här kommandot skapar en säkerhets regel som tillåter åtkomst från Internet till port 3389</span><span class="sxs-lookup"><span data-stu-id="3dffb-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="3dffb-112">Exempel 2: skapa en nätverks säkerhets regel som tillåter HTTP</span><span class="sxs-lookup"><span data-stu-id="3dffb-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="3dffb-113">Det här kommandot skapar en säkerhets regel som tillåter åtkomst från Internet till port 80</span><span class="sxs-lookup"><span data-stu-id="3dffb-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="3dffb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3dffb-114">PARAMETERS</span></span>

### <span data-ttu-id="3dffb-115">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="3dffb-115">-Access</span></span>
<span data-ttu-id="3dffb-116">Anger om nätverks trafik tillåts eller nekas.</span><span class="sxs-lookup"><span data-stu-id="3dffb-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="3dffb-117">De acceptabla värdena för den här parametern är: Allow och Deny.</span><span class="sxs-lookup"><span data-stu-id="3dffb-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="3dffb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dffb-118">-DefaultProfile</span></span>
<span data-ttu-id="3dffb-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3dffb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dffb-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3dffb-120">-Description</span></span>
<span data-ttu-id="3dffb-121">Anger en beskrivning av nätverks säkerhets regelns konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3dffb-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="3dffb-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3dffb-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="3dffb-123">Anger ett prefix för mål adress.</span><span class="sxs-lookup"><span data-stu-id="3dffb-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="3dffb-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3dffb-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3dffb-125">CIDR-adress (Classless Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="3dffb-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="3dffb-126">Ett mål-IP-adressintervall</span><span class="sxs-lookup"><span data-stu-id="3dffb-126">A destination IP address range</span></span> 
- <span data-ttu-id="3dffb-127">Ett jokertecken (\*) för att matcha en IP-adress du kan använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="3dffb-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="3dffb-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3dffb-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="3dffb-129">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="3dffb-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="3dffb-130">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="3dffb-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3dffb-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3dffb-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="3dffb-132">Säkerhets gruppen program ange som mål för regeln.</span><span class="sxs-lookup"><span data-stu-id="3dffb-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="3dffb-133">Den kan inte användas med parametern ' DestinationAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="3dffb-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3dffb-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="3dffb-134">-DestinationPortRange</span></span>
<span data-ttu-id="3dffb-135">Anger en målport eller ett område.</span><span class="sxs-lookup"><span data-stu-id="3dffb-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="3dffb-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3dffb-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3dffb-137">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="3dffb-137">An integer</span></span>
- <span data-ttu-id="3dffb-138">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="3dffb-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="3dffb-139">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="3dffb-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="3dffb-140">-Riktning</span><span class="sxs-lookup"><span data-stu-id="3dffb-140">-Direction</span></span>
<span data-ttu-id="3dffb-141">Anger om en regel utvärderas för inkommande eller utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="3dffb-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="3dffb-142">De acceptabla värdena för den här parametern är: inkommande och utgående.</span><span class="sxs-lookup"><span data-stu-id="3dffb-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="3dffb-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="3dffb-143">-Name</span></span>
<span data-ttu-id="3dffb-144">Anger namnet på den nätverks säkerhets regel som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="3dffb-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3dffb-145">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="3dffb-145">-Priority</span></span>
<span data-ttu-id="3dffb-146">Anger prioriteten för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3dffb-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="3dffb-147">De acceptabla värdena för den här parametern är: ett heltal mellan 100 och 4096.</span><span class="sxs-lookup"><span data-stu-id="3dffb-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="3dffb-148">Prioritets numret måste vara unikt för varje regel i samlingen.</span><span class="sxs-lookup"><span data-stu-id="3dffb-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="3dffb-149">Ju lägre prioritets nummer desto högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="3dffb-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="3dffb-150">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3dffb-150">-Protocol</span></span>
<span data-ttu-id="3dffb-151">Anger det nätverks protokoll som en ny regel konfiguration gäller för.</span><span class="sxs-lookup"><span data-stu-id="3dffb-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="3dffb-152">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3dffb-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3dffb-153">TCP</span><span class="sxs-lookup"><span data-stu-id="3dffb-153">Tcp</span></span>
- <span data-ttu-id="3dffb-154">UDP</span><span class="sxs-lookup"><span data-stu-id="3dffb-154">Udp</span></span>
- <span data-ttu-id="3dffb-155">jokertecken (\*) för att passa båda.</span><span class="sxs-lookup"><span data-stu-id="3dffb-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="3dffb-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3dffb-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="3dffb-157">Anger ett käll adress prefix.</span><span class="sxs-lookup"><span data-stu-id="3dffb-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="3dffb-158">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3dffb-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3dffb-159">EN CIDR</span><span class="sxs-lookup"><span data-stu-id="3dffb-159">A CIDR</span></span>
- <span data-ttu-id="3dffb-160">Ett käll-IP-intervall</span><span class="sxs-lookup"><span data-stu-id="3dffb-160">A source IP range</span></span>
- <span data-ttu-id="3dffb-161">Ett jokertecken (\*) för att matcha alla IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="3dffb-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="3dffb-162">Du kan också använda taggar som VirtualNetwork, AzureLoadBalancer och Internet.</span><span class="sxs-lookup"><span data-stu-id="3dffb-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="3dffb-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3dffb-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="3dffb-164">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="3dffb-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="3dffb-165">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="3dffb-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3dffb-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3dffb-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="3dffb-167">Säkerhets gruppen program ange som källa för regeln.</span><span class="sxs-lookup"><span data-stu-id="3dffb-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="3dffb-168">Den kan inte användas med parametern ' SourceAddressPrefix '.</span><span class="sxs-lookup"><span data-stu-id="3dffb-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3dffb-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="3dffb-169">-SourcePortRange</span></span>
<span data-ttu-id="3dffb-170">Anger käll port eller-intervall.</span><span class="sxs-lookup"><span data-stu-id="3dffb-170">Specifies the source port or range.</span></span>
<span data-ttu-id="3dffb-171">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3dffb-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3dffb-172">Ett heltal</span><span class="sxs-lookup"><span data-stu-id="3dffb-172">An integer</span></span>
- <span data-ttu-id="3dffb-173">Ett intervall med heltal mellan 0 och 65535</span><span class="sxs-lookup"><span data-stu-id="3dffb-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="3dffb-174">Ett jokertecken (\*) för att matcha valfri port</span><span class="sxs-lookup"><span data-stu-id="3dffb-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="3dffb-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dffb-175">CommonParameters</span></span>
<span data-ttu-id="3dffb-176">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dffb-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dffb-177">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dffb-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dffb-178">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3dffb-178">INPUTS</span></span>

### <span data-ttu-id="3dffb-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="3dffb-179">None</span></span>

## <span data-ttu-id="3dffb-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3dffb-180">OUTPUTS</span></span>

### <span data-ttu-id="3dffb-181">Microsoft. Azure. commands. Networks. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="3dffb-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="3dffb-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3dffb-182">NOTES</span></span>

## <span data-ttu-id="3dffb-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3dffb-183">RELATED LINKS</span></span>

[<span data-ttu-id="3dffb-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dffb-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3dffb-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dffb-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3dffb-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dffb-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3dffb-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3dffb-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


