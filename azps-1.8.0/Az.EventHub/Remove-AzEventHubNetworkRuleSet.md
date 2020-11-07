---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 597a5f0da161f7276c4945afaf026e9ee4879800
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754056"
---
# <span data-ttu-id="66a9a-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="66a9a-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="66a9a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="66a9a-103">Tar bort NetwrokRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="66a9a-103">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="66a9a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66a9a-104">SYNTAX</span></span>

### <span data-ttu-id="66a9a-105">NetworkRuleSetPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="66a9a-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66a9a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="66a9a-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66a9a-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66a9a-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a9a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66a9a-108">DESCRIPTION</span></span>
<span data-ttu-id="66a9a-109">Tar bort NetwrokRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="66a9a-109">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="66a9a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66a9a-110">EXAMPLES</span></span>

### <span data-ttu-id="66a9a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="66a9a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="66a9a-112">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="66a9a-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="66a9a-113">Tar bort NetwrokRuleSet för angiven "Eventhub-Namespace1-1375" namesapce</span><span class="sxs-lookup"><span data-stu-id="66a9a-113">Deletes the NetwrokRuleSet for the Given "Eventhub-Namespace1-1375" namesapce</span></span> 

### <span data-ttu-id="66a9a-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="66a9a-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="66a9a-115">Tar bort NetwrokRuleSet med InputObject</span><span class="sxs-lookup"><span data-stu-id="66a9a-115">Deletes the NetwrokRuleSet using InputObject</span></span> 

### <span data-ttu-id="66a9a-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="66a9a-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="66a9a-117">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="66a9a-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="66a9a-118">Tar bort NetwrokRuleSet med ResourceId för Namepsace</span><span class="sxs-lookup"><span data-stu-id="66a9a-118">Deletes the NetwrokRuleSet using ResourceId of the Namepsace</span></span>


## <span data-ttu-id="66a9a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66a9a-119">PARAMETERS</span></span>

### <span data-ttu-id="66a9a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66a9a-120">-AsJob</span></span>
<span data-ttu-id="66a9a-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="66a9a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66a9a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a9a-122">-DefaultProfile</span></span>
<span data-ttu-id="66a9a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66a9a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a9a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66a9a-124">-InputObject</span></span>
<span data-ttu-id="66a9a-125">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="66a9a-125">Namespace Object</span></span>

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

### <span data-ttu-id="66a9a-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="66a9a-126">-Name</span></span>
<span data-ttu-id="66a9a-127">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="66a9a-127">Namespace Name</span></span>

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

### <span data-ttu-id="66a9a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66a9a-128">-PassThru</span></span>
<span data-ttu-id="66a9a-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="66a9a-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="66a9a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a9a-130">-ResourceGroupName</span></span>
<span data-ttu-id="66a9a-131">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="66a9a-131">Resource Group Name</span></span>

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

### <span data-ttu-id="66a9a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66a9a-132">-ResourceId</span></span>
<span data-ttu-id="66a9a-133">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="66a9a-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="66a9a-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="66a9a-134">-Confirm</span></span>
<span data-ttu-id="66a9a-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="66a9a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66a9a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a9a-136">-WhatIf</span></span>
<span data-ttu-id="66a9a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="66a9a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a9a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="66a9a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66a9a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a9a-139">CommonParameters</span></span>
<span data-ttu-id="66a9a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a9a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="66a9a-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a9a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a9a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66a9a-142">INPUTS</span></span>

### <span data-ttu-id="66a9a-143">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="66a9a-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="66a9a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="66a9a-144">System.String</span></span>

## <span data-ttu-id="66a9a-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66a9a-145">OUTPUTS</span></span>

### <span data-ttu-id="66a9a-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66a9a-146">System.Boolean</span></span>

## <span data-ttu-id="66a9a-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66a9a-147">NOTES</span></span>

## <span data-ttu-id="66a9a-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66a9a-148">RELATED LINKS</span></span>