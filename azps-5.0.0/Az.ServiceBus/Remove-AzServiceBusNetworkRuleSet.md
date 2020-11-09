---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 6c803f399bf88c6e4887441ec9f9bd50c058361b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319835"
---
# <span data-ttu-id="483f2-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="483f2-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="483f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="483f2-102">SYNOPSIS</span></span>
<span data-ttu-id="483f2-103">Tar bort NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="483f2-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="483f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="483f2-104">SYNTAX</span></span>

### <span data-ttu-id="483f2-105">NetworkRuleSetPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="483f2-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="483f2-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="483f2-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="483f2-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="483f2-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="483f2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="483f2-108">DESCRIPTION</span></span>
<span data-ttu-id="483f2-109">Tar bort NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="483f2-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="483f2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="483f2-110">EXAMPLES</span></span>

### <span data-ttu-id="483f2-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="483f2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="483f2-112">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="483f2-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="483f2-113">Tar bort NetworkRuleSet för det givna "ServiceBus-Namespace1-1375"-namn området</span><span class="sxs-lookup"><span data-stu-id="483f2-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="483f2-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="483f2-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="483f2-115">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="483f2-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="483f2-116">Tar bort NetworkRuleSet med InputObject</span><span class="sxs-lookup"><span data-stu-id="483f2-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="483f2-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="483f2-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="483f2-118">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="483f2-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="483f2-119">Tar bort NetworkRuleSet med ResourceId för namn området</span><span class="sxs-lookup"><span data-stu-id="483f2-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="483f2-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="483f2-120">PARAMETERS</span></span>

### <span data-ttu-id="483f2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="483f2-121">-AsJob</span></span>
<span data-ttu-id="483f2-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="483f2-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="483f2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483f2-123">-DefaultProfile</span></span>
<span data-ttu-id="483f2-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="483f2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="483f2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="483f2-125">-InputObject</span></span>
<span data-ttu-id="483f2-126">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="483f2-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="483f2-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="483f2-127">-Name</span></span>
<span data-ttu-id="483f2-128">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="483f2-128">Namespace Name</span></span>

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

### <span data-ttu-id="483f2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="483f2-129">-PassThru</span></span>
<span data-ttu-id="483f2-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="483f2-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="483f2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="483f2-131">-ResourceGroupName</span></span>
<span data-ttu-id="483f2-132">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="483f2-132">Resource Group Name</span></span>

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

### <span data-ttu-id="483f2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="483f2-133">-ResourceId</span></span>
<span data-ttu-id="483f2-134">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="483f2-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="483f2-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="483f2-135">-Confirm</span></span>
<span data-ttu-id="483f2-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="483f2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="483f2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="483f2-137">-WhatIf</span></span>
<span data-ttu-id="483f2-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="483f2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="483f2-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="483f2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="483f2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483f2-140">CommonParameters</span></span>
<span data-ttu-id="483f2-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483f2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="483f2-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="483f2-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483f2-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="483f2-143">INPUTS</span></span>

### <span data-ttu-id="483f2-144">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="483f2-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="483f2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="483f2-145">System.String</span></span>

## <span data-ttu-id="483f2-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="483f2-146">OUTPUTS</span></span>

### <span data-ttu-id="483f2-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="483f2-147">System.Boolean</span></span>

## <span data-ttu-id="483f2-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="483f2-148">NOTES</span></span>

## <span data-ttu-id="483f2-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="483f2-149">RELATED LINKS</span></span>
