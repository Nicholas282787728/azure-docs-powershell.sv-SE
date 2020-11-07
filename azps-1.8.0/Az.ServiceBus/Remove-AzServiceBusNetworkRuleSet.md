---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: df8e85505a7aa62b883ecdc0536f9b3cd1352109
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746888"
---
# <span data-ttu-id="82eef-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="82eef-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="82eef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82eef-102">SYNOPSIS</span></span>
<span data-ttu-id="82eef-103">Tar bort NetwrokRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="82eef-103">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="82eef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82eef-104">SYNTAX</span></span>

### <span data-ttu-id="82eef-105">NetworkRuleSetPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="82eef-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82eef-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="82eef-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82eef-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82eef-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82eef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82eef-108">DESCRIPTION</span></span>
<span data-ttu-id="82eef-109">Tar bort NetwrokRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="82eef-109">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="82eef-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82eef-110">EXAMPLES</span></span>

### <span data-ttu-id="82eef-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82eef-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="82eef-112">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="82eef-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="82eef-113">Tar bort NetwrokRuleSet för angiven "ServiceBus-Namespace1-1375" namesapce</span><span class="sxs-lookup"><span data-stu-id="82eef-113">Deletes the NetwrokRuleSet for the Given "ServiceBus-Namespace1-1375" namesapce</span></span> 

### <span data-ttu-id="82eef-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="82eef-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="82eef-115">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="82eef-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="82eef-116">Tar bort NetwrokRuleSet med InputObject</span><span class="sxs-lookup"><span data-stu-id="82eef-116">Deletes the NetwrokRuleSet using InputObject</span></span> 

### <span data-ttu-id="82eef-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="82eef-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="82eef-118">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="82eef-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="82eef-119">Tar bort NetwrokRuleSet med ResourceId för Namepsace</span><span class="sxs-lookup"><span data-stu-id="82eef-119">Deletes the NetwrokRuleSet using ResourceId of the Namepsace</span></span>


## <span data-ttu-id="82eef-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82eef-120">PARAMETERS</span></span>

### <span data-ttu-id="82eef-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82eef-121">-AsJob</span></span>
<span data-ttu-id="82eef-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="82eef-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82eef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82eef-123">-DefaultProfile</span></span>
<span data-ttu-id="82eef-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82eef-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82eef-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82eef-125">-InputObject</span></span>
<span data-ttu-id="82eef-126">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="82eef-126">Namespace Object</span></span>

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

### <span data-ttu-id="82eef-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="82eef-127">-Name</span></span>
<span data-ttu-id="82eef-128">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="82eef-128">Namespace Name</span></span>

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

### <span data-ttu-id="82eef-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82eef-129">-PassThru</span></span>
<span data-ttu-id="82eef-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="82eef-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="82eef-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82eef-131">-ResourceGroupName</span></span>
<span data-ttu-id="82eef-132">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="82eef-132">Resource Group Name</span></span>

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

### <span data-ttu-id="82eef-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82eef-133">-ResourceId</span></span>
<span data-ttu-id="82eef-134">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="82eef-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="82eef-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82eef-135">-Confirm</span></span>
<span data-ttu-id="82eef-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82eef-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82eef-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82eef-137">-WhatIf</span></span>
<span data-ttu-id="82eef-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82eef-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82eef-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82eef-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82eef-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82eef-140">CommonParameters</span></span>
<span data-ttu-id="82eef-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82eef-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="82eef-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82eef-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82eef-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82eef-143">INPUTS</span></span>

### <span data-ttu-id="82eef-144">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="82eef-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="82eef-145">System. String</span><span class="sxs-lookup"><span data-stu-id="82eef-145">System.String</span></span>

## <span data-ttu-id="82eef-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82eef-146">OUTPUTS</span></span>

### <span data-ttu-id="82eef-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82eef-147">System.Boolean</span></span>

## <span data-ttu-id="82eef-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82eef-148">NOTES</span></span>

## <span data-ttu-id="82eef-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82eef-149">RELATED LINKS</span></span>
