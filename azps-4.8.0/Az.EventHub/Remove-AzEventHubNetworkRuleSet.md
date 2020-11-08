---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262688"
---
# <span data-ttu-id="25265-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="25265-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="25265-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25265-102">SYNOPSIS</span></span>
<span data-ttu-id="25265-103">Tar bort NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="25265-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="25265-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25265-104">SYNTAX</span></span>

### <span data-ttu-id="25265-105">NetworkRuleSetPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="25265-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25265-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="25265-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25265-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25265-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25265-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25265-108">DESCRIPTION</span></span>
<span data-ttu-id="25265-109">Tar bort NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="25265-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="25265-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25265-110">EXAMPLES</span></span>

### <span data-ttu-id="25265-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25265-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="25265-112">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="25265-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="25265-113">Tar bort NetworkRuleSet för angivet "Eventhub-Namespace1-1375"-namn område</span><span class="sxs-lookup"><span data-stu-id="25265-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="25265-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="25265-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="25265-115">Tar bort NetworkRuleSet med InputObject</span><span class="sxs-lookup"><span data-stu-id="25265-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="25265-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="25265-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="25265-117">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="25265-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="25265-118">Tar bort NetworkRuleSet med ResourceId för namn området</span><span class="sxs-lookup"><span data-stu-id="25265-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="25265-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25265-119">PARAMETERS</span></span>

### <span data-ttu-id="25265-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25265-120">-AsJob</span></span>
<span data-ttu-id="25265-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="25265-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25265-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25265-122">-DefaultProfile</span></span>
<span data-ttu-id="25265-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25265-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25265-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25265-124">-InputObject</span></span>
<span data-ttu-id="25265-125">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="25265-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25265-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="25265-126">-Name</span></span>
<span data-ttu-id="25265-127">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="25265-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25265-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25265-128">-PassThru</span></span>
<span data-ttu-id="25265-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="25265-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="25265-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25265-130">-ResourceGroupName</span></span>
<span data-ttu-id="25265-131">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="25265-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25265-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25265-132">-ResourceId</span></span>
<span data-ttu-id="25265-133">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="25265-133">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25265-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="25265-134">-Confirm</span></span>
<span data-ttu-id="25265-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="25265-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25265-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25265-136">-WhatIf</span></span>
<span data-ttu-id="25265-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="25265-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25265-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="25265-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25265-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25265-139">CommonParameters</span></span>
<span data-ttu-id="25265-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25265-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="25265-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25265-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25265-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25265-142">INPUTS</span></span>

### <span data-ttu-id="25265-143">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="25265-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="25265-144">System. String</span><span class="sxs-lookup"><span data-stu-id="25265-144">System.String</span></span>

## <span data-ttu-id="25265-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25265-145">OUTPUTS</span></span>

### <span data-ttu-id="25265-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25265-146">System.Boolean</span></span>

## <span data-ttu-id="25265-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25265-147">NOTES</span></span>

## <span data-ttu-id="25265-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25265-148">RELATED LINKS</span></span>