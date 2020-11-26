---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 87f735a098057beb67b76fd4a0f763732c2e816a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325488"
---
# <span data-ttu-id="b5b44-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b5b44-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="b5b44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5b44-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b44-103">Uppdatera NetworkruleSet för det angivna namn området i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b5b44-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="b5b44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5b44-104">SYNTAX</span></span>

### <span data-ttu-id="b5b44-105">NetworkRuleSetPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b5b44-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5b44-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b5b44-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5b44-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5b44-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5b44-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5b44-108">DESCRIPTION</span></span>
<span data-ttu-id="b5b44-109">Uppdatera NetwrokruleSet för det angivna namn området i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b5b44-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="b5b44-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5b44-110">EXAMPLES</span></span>

### <span data-ttu-id="b5b44-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b5b44-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="b5b44-112">Namn: standard DefaultAction: Tillåt ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="b5b44-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="b5b44-113">Uppdatera NetworkRuleSet med-IPRule och-VirtualNetworkRule-parametrar</span><span class="sxs-lookup"><span data-stu-id="b5b44-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="b5b44-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b5b44-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="b5b44-115">Namn: standard DefaultAction: Tillåt ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="b5b44-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="b5b44-116">Uppdatera NetworkRuleSet med-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5b44-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="b5b44-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="b5b44-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="b5b44-118">Namn: standard DefaultAction: Tillåt ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="b5b44-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="b5b44-119">Uppdatera NetworkRuleSet med-ResourceId för det andra namn området.</span><span class="sxs-lookup"><span data-stu-id="b5b44-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="b5b44-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5b44-120">PARAMETERS</span></span>

### <span data-ttu-id="b5b44-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="b5b44-121">-DefaultAction</span></span>
<span data-ttu-id="b5b44-122">Standard åtgärd för NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b5b44-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="b5b44-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b44-123">-DefaultProfile</span></span>
<span data-ttu-id="b5b44-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b44-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5b44-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5b44-125">-InputObject</span></span>
<span data-ttu-id="b5b44-126">NetworkruleSet-konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="b5b44-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="b5b44-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="b5b44-127">-IPRule</span></span>
<span data-ttu-id="b5b44-128">Lista över IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="b5b44-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="b5b44-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5b44-129">-Name</span></span>
<span data-ttu-id="b5b44-130">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="b5b44-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="b5b44-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b44-131">-ResourceGroupName</span></span>
<span data-ttu-id="b5b44-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b5b44-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="b5b44-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5b44-133">-ResourceId</span></span>
<span data-ttu-id="b5b44-134">Resurs-ID för namn området</span><span class="sxs-lookup"><span data-stu-id="b5b44-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="b5b44-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b5b44-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="b5b44-136">Lista över VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="b5b44-136">List of VirtualNetworkRules</span></span>

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

### <span data-ttu-id="b5b44-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5b44-137">-Confirm</span></span>
<span data-ttu-id="b5b44-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5b44-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5b44-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5b44-139">-WhatIf</span></span>
<span data-ttu-id="b5b44-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5b44-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5b44-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5b44-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5b44-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b44-142">CommonParameters</span></span>
<span data-ttu-id="b5b44-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b44-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b5b44-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b44-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b44-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5b44-145">INPUTS</span></span>

### <span data-ttu-id="b5b44-146">Microsoft. Azure. commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="b5b44-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="b5b44-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b5b44-147">System.String</span></span>

## <span data-ttu-id="b5b44-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5b44-148">OUTPUTS</span></span>

### <span data-ttu-id="b5b44-149">Microsoft. Azure. commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="b5b44-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="b5b44-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5b44-150">NOTES</span></span>

## <span data-ttu-id="b5b44-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5b44-151">RELATED LINKS</span></span>