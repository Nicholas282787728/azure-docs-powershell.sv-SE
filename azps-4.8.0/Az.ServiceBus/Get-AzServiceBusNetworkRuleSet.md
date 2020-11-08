---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: c9c5d3f9c8900ebfa1e11202f6105549c2180481
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100854"
---
# <span data-ttu-id="2a141-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2a141-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="2a141-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a141-102">SYNOPSIS</span></span>
<span data-ttu-id="2a141-103">Hämtar information om en händelse hubbar NetworkruleSet i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2a141-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="2a141-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a141-104">SYNTAX</span></span>

### <span data-ttu-id="2a141-105">NetworkRuleSetPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2a141-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a141-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2a141-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a141-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a141-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a141-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a141-108">DESCRIPTION</span></span>
<span data-ttu-id="2a141-109">Hämtar information om en händelse hubbar NetworkruleSet i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2a141-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="2a141-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a141-110">EXAMPLES</span></span>

### <span data-ttu-id="2a141-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a141-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="2a141-112">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1; Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="2a141-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="2a141-113">Få information om NetworkruleSet med hjälp av ResourceGroup och namespace parametrar.</span><span class="sxs-lookup"><span data-stu-id="2a141-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="2a141-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2a141-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="2a141-115">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1; Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="2a141-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="2a141-116">Få information om NetworkruleSet med namn områden som finns i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2a141-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="2a141-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="2a141-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="2a141-118">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1; Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="2a141-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="2a141-119">Få information om NetworkruleSet med resurs-ID för andra namn områden</span><span class="sxs-lookup"><span data-stu-id="2a141-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="2a141-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a141-120">PARAMETERS</span></span>

### <span data-ttu-id="2a141-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a141-121">-DefaultProfile</span></span>
<span data-ttu-id="2a141-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a141-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a141-123">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="2a141-123">-Namespace</span></span>
<span data-ttu-id="2a141-124">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="2a141-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a141-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a141-125">-ResourceGroupName</span></span>
<span data-ttu-id="2a141-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2a141-126">Resource Group Name</span></span>

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

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a141-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a141-127">-ResourceId</span></span>
<span data-ttu-id="2a141-128">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="2a141-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2a141-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a141-129">CommonParameters</span></span>
<span data-ttu-id="2a141-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a141-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2a141-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a141-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a141-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a141-132">INPUTS</span></span>

### <span data-ttu-id="2a141-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2a141-133">System.String</span></span>

## <span data-ttu-id="2a141-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a141-134">OUTPUTS</span></span>

### <span data-ttu-id="2a141-135">Microsoft. Azure. commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="2a141-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="2a141-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a141-136">NOTES</span></span>

## <span data-ttu-id="2a141-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a141-137">RELATED LINKS</span></span>