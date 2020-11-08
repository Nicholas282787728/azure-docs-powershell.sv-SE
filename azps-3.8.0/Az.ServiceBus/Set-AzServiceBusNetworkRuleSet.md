---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 87f735a098057beb67b76fd4a0f763732c2e816a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088813"
---
# <span data-ttu-id="36f5e-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="36f5e-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="36f5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="36f5e-103">Uppdatera NetworkruleSet för det angivna namn området i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="36f5e-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="36f5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36f5e-104">SYNTAX</span></span>

### <span data-ttu-id="36f5e-105">NetworkRuleSetPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="36f5e-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36f5e-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="36f5e-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36f5e-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36f5e-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36f5e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36f5e-108">DESCRIPTION</span></span>
<span data-ttu-id="36f5e-109">Uppdatera NetwrokruleSet för det angivna namn området i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="36f5e-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="36f5e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36f5e-110">EXAMPLES</span></span>

### <span data-ttu-id="36f5e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="36f5e-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="36f5e-112">Namn: standard DefaultAction: Tillåt ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="36f5e-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="36f5e-113">Uppdatera NetworkRuleSet med-IPRule och-VirtualNetworkRule-parametrar</span><span class="sxs-lookup"><span data-stu-id="36f5e-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="36f5e-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="36f5e-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="36f5e-115">Namn: standard DefaultAction: Tillåt ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="36f5e-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="36f5e-116">Uppdatera NetworkRuleSet med-InputObject</span><span class="sxs-lookup"><span data-stu-id="36f5e-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="36f5e-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="36f5e-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="36f5e-118">Namn: standard DefaultAction: Tillåt ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="36f5e-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="36f5e-119">Uppdatera NetworkRuleSet med-ResourceId för det andra namn området.</span><span class="sxs-lookup"><span data-stu-id="36f5e-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="36f5e-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36f5e-120">PARAMETERS</span></span>

### <span data-ttu-id="36f5e-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="36f5e-121">-DefaultAction</span></span>
<span data-ttu-id="36f5e-122">Standard åtgärd för NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="36f5e-122">Default Action for NetworkRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f5e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f5e-123">-DefaultProfile</span></span>
<span data-ttu-id="36f5e-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36f5e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36f5e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36f5e-125">-InputObject</span></span>
<span data-ttu-id="36f5e-126">NetworkruleSet-konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="36f5e-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36f5e-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="36f5e-127">-IPRule</span></span>
<span data-ttu-id="36f5e-128">Lista över IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="36f5e-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f5e-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="36f5e-129">-Name</span></span>
<span data-ttu-id="36f5e-130">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="36f5e-130">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f5e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f5e-131">-ResourceGroupName</span></span>
<span data-ttu-id="36f5e-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="36f5e-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f5e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36f5e-133">-ResourceId</span></span>
<span data-ttu-id="36f5e-134">Resurs-ID för namn området</span><span class="sxs-lookup"><span data-stu-id="36f5e-134">Resource ID of Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f5e-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="36f5e-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="36f5e-136">Lista över VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="36f5e-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36f5e-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36f5e-137">-Confirm</span></span>
<span data-ttu-id="36f5e-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="36f5e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36f5e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f5e-139">-WhatIf</span></span>
<span data-ttu-id="36f5e-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="36f5e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36f5e-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="36f5e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36f5e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f5e-142">CommonParameters</span></span>
<span data-ttu-id="36f5e-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f5e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="36f5e-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36f5e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f5e-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36f5e-145">INPUTS</span></span>

### <span data-ttu-id="36f5e-146">Microsoft. Azure. commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="36f5e-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="36f5e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="36f5e-147">System.String</span></span>

## <span data-ttu-id="36f5e-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36f5e-148">OUTPUTS</span></span>

### <span data-ttu-id="36f5e-149">Microsoft. Azure. commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="36f5e-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="36f5e-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36f5e-150">NOTES</span></span>

## <span data-ttu-id="36f5e-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36f5e-151">RELATED LINKS</span></span>