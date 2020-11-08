---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: d72c7e1ebfdd7543740ea8fafeb62861f4394093
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088819"
---
# <span data-ttu-id="9d8b4-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9d8b4-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="9d8b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="9d8b4-103">Tar bort den enskilda VirtualNetworkRule för NetworkRuleSet i namn området</span><span class="sxs-lookup"><span data-stu-id="9d8b4-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="9d8b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d8b4-104">SYNTAX</span></span>

### <span data-ttu-id="9d8b4-105">VirtualNetworkRulePropertiesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9d8b4-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d8b4-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d8b4-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d8b4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d8b4-107">DESCRIPTION</span></span>
<span data-ttu-id="9d8b4-108">Tar bort den enskilda VirtualNetworkRule för NetworkRuleSet i namn området</span><span class="sxs-lookup"><span data-stu-id="9d8b4-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="9d8b4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d8b4-109">EXAMPLES</span></span>

### <span data-ttu-id="9d8b4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9d8b4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="9d8b4-111">Tar bort den enskilda VirtualNetworkRule för NetworkRuleSet i namn området</span><span class="sxs-lookup"><span data-stu-id="9d8b4-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="9d8b4-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9d8b4-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="9d8b4-113">Ta bort $virtualruleset 1 för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="9d8b4-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="9d8b4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d8b4-114">PARAMETERS</span></span>

### <span data-ttu-id="9d8b4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d8b4-115">-AsJob</span></span>
<span data-ttu-id="9d8b4-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9d8b4-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d8b4-117">-DefaultProfile</span></span>
<span data-ttu-id="9d8b4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d8b4-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d8b4-119">-Name</span></span>
<span data-ttu-id="9d8b4-120">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="9d8b4-120">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d8b4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d8b4-121">-PassThru</span></span>
<span data-ttu-id="9d8b4-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9d8b4-122">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8b4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d8b4-123">-ResourceGroupName</span></span>
<span data-ttu-id="9d8b4-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9d8b4-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d8b4-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9d8b4-125">-SubnetId</span></span>
<span data-ttu-id="9d8b4-126">ID för under nätet</span><span class="sxs-lookup"><span data-stu-id="9d8b4-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d8b4-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="9d8b4-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="9d8b4-128">IPRule-konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="9d8b4-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d8b4-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9d8b4-129">-Confirm</span></span>
<span data-ttu-id="9d8b4-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d8b4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d8b4-131">-WhatIf</span></span>
<span data-ttu-id="9d8b4-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d8b4-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d8b4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d8b4-134">CommonParameters</span></span>
<span data-ttu-id="9d8b4-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d8b4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9d8b4-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d8b4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d8b4-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d8b4-137">INPUTS</span></span>

### <span data-ttu-id="9d8b4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9d8b4-138">System.String</span></span>

### <span data-ttu-id="9d8b4-139">Microsoft. Azure. commands. ServiceBus. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="9d8b4-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="9d8b4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d8b4-140">OUTPUTS</span></span>

### <span data-ttu-id="9d8b4-141">Microsoft. Azure. commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="9d8b4-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="9d8b4-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d8b4-142">NOTES</span></span>

## <span data-ttu-id="9d8b4-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d8b4-143">RELATED LINKS</span></span>
