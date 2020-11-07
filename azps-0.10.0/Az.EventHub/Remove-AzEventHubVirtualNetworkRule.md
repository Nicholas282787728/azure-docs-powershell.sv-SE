---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 9385d8ca958eab28f485e56fbcd6c926f5422ca0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922861"
---
# <span data-ttu-id="8b105-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8b105-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="8b105-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b105-102">SYNOPSIS</span></span>
<span data-ttu-id="8b105-103">Tar bort den enskilda VirtualNetworkRule för NetworkRuleSet i namn området</span><span class="sxs-lookup"><span data-stu-id="8b105-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="8b105-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b105-104">SYNTAX</span></span>

### <span data-ttu-id="8b105-105">VirtualNetworkRulePropertiesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8b105-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b105-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b105-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b105-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b105-107">DESCRIPTION</span></span>
<span data-ttu-id="8b105-108">Tar bort den enskilda VirtualNetworkRule för NetworkRuleSet i namn området</span><span class="sxs-lookup"><span data-stu-id="8b105-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="8b105-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b105-109">EXAMPLES</span></span>

### <span data-ttu-id="8b105-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8b105-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="8b105-111">Tar bort den enskilda VirtualNetworkRule för NetworkRuleSet i namn området</span><span class="sxs-lookup"><span data-stu-id="8b105-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="8b105-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8b105-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="8b105-113">Ta bort $virtualruleset 1 för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="8b105-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="8b105-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b105-114">PARAMETERS</span></span>

### <span data-ttu-id="8b105-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b105-115">-AsJob</span></span>
<span data-ttu-id="8b105-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8b105-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b105-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b105-117">-DefaultProfile</span></span>
<span data-ttu-id="8b105-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b105-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b105-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b105-119">-Name</span></span>
<span data-ttu-id="8b105-120">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="8b105-120">Namespace Name</span></span>

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

### <span data-ttu-id="8b105-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b105-121">-PassThru</span></span>
<span data-ttu-id="8b105-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8b105-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8b105-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b105-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b105-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8b105-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8b105-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8b105-125">-SubnetId</span></span>
<span data-ttu-id="8b105-126">ID för under nätet</span><span class="sxs-lookup"><span data-stu-id="8b105-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="8b105-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="8b105-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="8b105-128">IPRule-konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="8b105-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b105-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b105-129">-Confirm</span></span>
<span data-ttu-id="8b105-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b105-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b105-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b105-131">-WhatIf</span></span>
<span data-ttu-id="8b105-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b105-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b105-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b105-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b105-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b105-134">CommonParameters</span></span>
<span data-ttu-id="8b105-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b105-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8b105-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b105-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b105-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b105-137">INPUTS</span></span>

### <span data-ttu-id="8b105-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8b105-138">System.String</span></span>

### <span data-ttu-id="8b105-139">Microsoft. Azure. commands. EventHub. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="8b105-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="8b105-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b105-140">OUTPUTS</span></span>

### <span data-ttu-id="8b105-141">Microsoft. Azure. commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="8b105-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="8b105-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b105-142">NOTES</span></span>

## <span data-ttu-id="8b105-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b105-143">RELATED LINKS</span></span>