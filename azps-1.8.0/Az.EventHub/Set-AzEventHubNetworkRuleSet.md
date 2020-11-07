---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 72be362d513f447e32db0fe13b5e4b7b076ab947
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754038"
---
# <span data-ttu-id="434d0-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="434d0-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="434d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="434d0-102">SYNOPSIS</span></span>
<span data-ttu-id="434d0-103">Uppdatera NetwrokruleSet för angiven Namepsace i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="434d0-103">Update the NetwrokruleSet of the given Namepsace in the current Azure subscription.</span></span>

## <span data-ttu-id="434d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="434d0-104">SYNTAX</span></span>

### <span data-ttu-id="434d0-105">NetworkRuleSetPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="434d0-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNteworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="434d0-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="434d0-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="434d0-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="434d0-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="434d0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="434d0-108">DESCRIPTION</span></span>
<span data-ttu-id="434d0-109">Uppdatera NetwrokruleSet för angiven Namepsace i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="434d0-109">Update the NetwrokruleSet of the given Namepsace in the current Azure subscription.</span></span>

## <span data-ttu-id="434d0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="434d0-110">EXAMPLES</span></span>

### <span data-ttu-id="434d0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="434d0-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNteworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="434d0-112">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="434d0-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="434d0-113">Uppdatera NetworkRuleSet med-IPRule och-VirtualNteworkRule-parametrar</span><span class="sxs-lookup"><span data-stu-id="434d0-113">Update the NetworkRuleSet using -IPRule and -VirtualNteworkRule parameters</span></span>

### <span data-ttu-id="434d0-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="434d0-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="434d0-115">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="434d0-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="434d0-116">Uppdatera NetworkRuleSet med-InputObject</span><span class="sxs-lookup"><span data-stu-id="434d0-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="434d0-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="434d0-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="434d0-118">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="434d0-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="434d0-119">Uppdatera NetworkRuleSet med-ResourceId för det andra namn området.</span><span class="sxs-lookup"><span data-stu-id="434d0-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="434d0-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="434d0-120">PARAMETERS</span></span>

### <span data-ttu-id="434d0-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="434d0-121">-DefaultAction</span></span>
<span data-ttu-id="434d0-122">Standard åtgärd för NetwrokeuleSet</span><span class="sxs-lookup"><span data-stu-id="434d0-122">Default Action for NetwrokeuleSet</span></span>

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

### <span data-ttu-id="434d0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434d0-123">-DefaultProfile</span></span>
<span data-ttu-id="434d0-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="434d0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="434d0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="434d0-125">-InputObject</span></span>
<span data-ttu-id="434d0-126">NetworkruleSet-konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="434d0-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="434d0-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="434d0-127">-IPRule</span></span>
<span data-ttu-id="434d0-128">Lista över IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="434d0-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434d0-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="434d0-129">-Name</span></span>
<span data-ttu-id="434d0-130">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="434d0-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="434d0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434d0-131">-ResourceGroupName</span></span>
<span data-ttu-id="434d0-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="434d0-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="434d0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="434d0-133">-ResourceId</span></span>
<span data-ttu-id="434d0-134">Resurs-ID för namn området</span><span class="sxs-lookup"><span data-stu-id="434d0-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="434d0-135">-VirtualNteworkRule</span><span class="sxs-lookup"><span data-stu-id="434d0-135">-VirtualNteworkRule</span></span>
<span data-ttu-id="434d0-136">Lista över VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="434d0-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434d0-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="434d0-137">-Confirm</span></span>
<span data-ttu-id="434d0-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="434d0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="434d0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="434d0-139">-WhatIf</span></span>
<span data-ttu-id="434d0-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="434d0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="434d0-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="434d0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="434d0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434d0-142">CommonParameters</span></span>
<span data-ttu-id="434d0-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="434d0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="434d0-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="434d0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434d0-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="434d0-145">INPUTS</span></span>

### <span data-ttu-id="434d0-146">Microsoft. Azure. commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="434d0-146">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="434d0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="434d0-147">System.String</span></span>

## <span data-ttu-id="434d0-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="434d0-148">OUTPUTS</span></span>

### <span data-ttu-id="434d0-149">Microsoft. Azure. commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="434d0-149">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="434d0-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="434d0-150">NOTES</span></span>

## <span data-ttu-id="434d0-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="434d0-151">RELATED LINKS</span></span>