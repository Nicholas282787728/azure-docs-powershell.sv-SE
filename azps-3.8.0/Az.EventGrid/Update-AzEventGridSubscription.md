---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: d4967dd45cc420035a4be60736389729d019fd45
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088656"
---
# <span data-ttu-id="880f5-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="880f5-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="880f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="880f5-102">SYNOPSIS</span></span>
<span data-ttu-id="880f5-103">Uppdatera egenskaperna för en händelse prenumeration för händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="880f5-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="880f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="880f5-104">SYNTAX</span></span>

### <span data-ttu-id="880f5-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="880f5-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="880f5-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="880f5-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="880f5-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="880f5-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="880f5-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="880f5-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="880f5-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="880f5-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="880f5-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="880f5-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="880f5-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="880f5-111">DESCRIPTION</span></span>
<span data-ttu-id="880f5-112">Uppdatera egenskaperna för en händelse prenumeration för händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="880f5-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="880f5-113">Det här kan användas för att uppdatera filter, mål eller etiketter för en befintlig händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="880f5-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="880f5-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="880f5-114">EXAMPLES</span></span>

### <span data-ttu-id="880f5-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="880f5-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="880f5-116">Uppdaterar slut punkten för händelse abonnemangs \` es1 \` för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` till \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="880f5-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="880f5-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="880f5-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="880f5-118">Uppdaterar slut punkten för händelse abonnemangs \` es1 \` för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` till \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="880f5-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="880f5-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="880f5-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="880f5-120">Uppdaterar egenskaperna för händelse prenumerationens \` es1 \` för EventHub-namnutrymmet ContosoNamespace med den nya slut punkten som \` https://requestb.in/1kxxoui1\ "och det nya SubjectEndsWith-filtret som \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="880f5-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="880f5-121">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="880f5-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="880f5-122">Uppdaterar egenskaperna för händelse prenumerationens \` es1 \` för resurs gruppen \` MyResourceGroupName \` med de nya etiketterna $Labels.</span><span class="sxs-lookup"><span data-stu-id="880f5-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="880f5-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="880f5-123">PARAMETERS</span></span>

### <span data-ttu-id="880f5-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="880f5-124">-AdvancedFilter</span></span>
<span data-ttu-id="880f5-125">Avancerat filter som anger en matris med flera hash-värden som används för serverbaserad filtrering.</span><span class="sxs-lookup"><span data-stu-id="880f5-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="880f5-126">Varje hash-värde har följande nycklar-värde info: operation, nyckel och värde eller värden.</span><span class="sxs-lookup"><span data-stu-id="880f5-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="880f5-127">Operatorn kan vara något av följande värden: numberin, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, Stringin, StringNotIn, StringBeginsWith, StringEndsWith eller StringContains.</span><span class="sxs-lookup"><span data-stu-id="880f5-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="880f5-128">Nyckel representerar egenskapen nytto Last där de avancerade filtrerings principerna tillämpas.</span><span class="sxs-lookup"><span data-stu-id="880f5-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="880f5-129">Till sist representerar värdet eller värdena värdena som ska matchas.</span><span class="sxs-lookup"><span data-stu-id="880f5-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="880f5-130">Det kan vara ett enskilt värde av motsvarande typ eller en matris med värden.</span><span class="sxs-lookup"><span data-stu-id="880f5-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="880f5-131">Som exempel på avancerade filter parametrar: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) där $AdvFilter 1 = @ {Operator = "Nummerin"; Key = "data. KEY1"; Värden = @ (1, 2)} och $AdvFilter 2 = @ {Operator = "StringBringsWith"; Key = "ämne"; Värden = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="880f5-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-132">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="880f5-132">-DeadLetterEndpoint</span></span>
<span data-ttu-id="880f5-133">Slut punkten som används för att lagra ej levererade händelser.</span><span class="sxs-lookup"><span data-stu-id="880f5-133">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="880f5-134">Ange Azure Resource ID för en lagrings-BLOB-behållare.</span><span class="sxs-lookup"><span data-stu-id="880f5-134">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="880f5-135">Till exempel:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="880f5-135">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="880f5-136">-DefaultProfile</span></span>
<span data-ttu-id="880f5-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="880f5-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="880f5-138">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="880f5-138">-DomainName</span></span>
<span data-ttu-id="880f5-139">Namnet på den domän där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="880f5-139">The name of the domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-140">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="880f5-140">-DomainTopicName</span></span>
<span data-ttu-id="880f5-141">Namnet på den domän där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="880f5-141">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-142">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="880f5-142">-Endpoint</span></span>
<span data-ttu-id="880f5-143">Destinations slut punkt för händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="880f5-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="880f5-144">Detta kan vara en webhook-URL eller Azure-resurs-ID för en EventHub, lagringsprovider, hybridconnection eller servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="880f5-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="880f5-145">Resurs-ID för en hybrid anslutning har till exempel följande form:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="880f5-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="880f5-146">Det förväntas att mål slut punkten skapas och är tillgänglig för användning innan ett händelse rutnät körs.</span><span class="sxs-lookup"><span data-stu-id="880f5-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="880f5-147">-EndpointType</span></span>
<span data-ttu-id="880f5-148">Typ av slut punkt.</span><span class="sxs-lookup"><span data-stu-id="880f5-148">Endpoint Type.</span></span>
<span data-ttu-id="880f5-149">Det här kan vara webhook, eventhub, storagequeue, hybridconnection eller servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="880f5-149">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="880f5-150">Standardvärdet är webhook.</span><span class="sxs-lookup"><span data-stu-id="880f5-150">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="880f5-151">-EventSubscriptionName</span></span>
<span data-ttu-id="880f5-152">Namnet på händelse prenumerationen</span><span class="sxs-lookup"><span data-stu-id="880f5-152">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="880f5-153">-EventTtl</span></span>
<span data-ttu-id="880f5-154">Tid i minuter för händelse leverans.</span><span class="sxs-lookup"><span data-stu-id="880f5-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="880f5-155">Värdet måste vara mellan 1 och 1440</span><span class="sxs-lookup"><span data-stu-id="880f5-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-156">-Förfallo</span><span class="sxs-lookup"><span data-stu-id="880f5-156">-ExpirationDate</span></span>
<span data-ttu-id="880f5-157">Avgör förfallo dag/tid för händelse prenumerationen efter vilken händelse prenumerationen dras tillbaka.</span><span class="sxs-lookup"><span data-stu-id="880f5-157">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-158">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="880f5-158">-IncludedEventType</span></span>
<span data-ttu-id="880f5-159">Filter som anger en lista över händelse typer som ska ingå. Om inget anges tas alla händelse typer med.</span><span class="sxs-lookup"><span data-stu-id="880f5-159">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-160">-InputObject</span><span class="sxs-lookup"><span data-stu-id="880f5-160">-InputObject</span></span>
<span data-ttu-id="880f5-161">EventGridSubscription-objekt.</span><span class="sxs-lookup"><span data-stu-id="880f5-161">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-162">-Etikett</span><span class="sxs-lookup"><span data-stu-id="880f5-162">-Label</span></span>
<span data-ttu-id="880f5-163">Etiketter för händelse abonnemanget</span><span class="sxs-lookup"><span data-stu-id="880f5-163">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-164">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="880f5-164">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="880f5-165">Maximalt antal försök att leverera händelsen.</span><span class="sxs-lookup"><span data-stu-id="880f5-165">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="880f5-166">Värdet måste vara mellan 1 och 30</span><span class="sxs-lookup"><span data-stu-id="880f5-166">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880f5-167">-ResourceGroupName</span></span>
<span data-ttu-id="880f5-168">Ämnets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="880f5-168">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="880f5-169">-ResourceId</span></span>
<span data-ttu-id="880f5-170">ID för resursen som händelse prenumerationen skapades för.</span><span class="sxs-lookup"><span data-stu-id="880f5-170">The identifier of the resource to which the event subscription was created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-171">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="880f5-171">-SubjectBeginsWith</span></span>
<span data-ttu-id="880f5-172">Filter som anger att endast händelser som matchar det angivna prefixet för subjektet kommer att ingå.</span><span class="sxs-lookup"><span data-stu-id="880f5-172">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="880f5-173">Om inget anges inkluderas händelser med alla ämnes prefix.</span><span class="sxs-lookup"><span data-stu-id="880f5-173">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-174">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="880f5-174">-SubjectEndsWith</span></span>
<span data-ttu-id="880f5-175">Filter som anger att endast händelser som matchar det angivna ämnes tillägget tas med.</span><span class="sxs-lookup"><span data-stu-id="880f5-175">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="880f5-176">Om inget anges inkluderas händelser med alla ämnes suffix.</span><span class="sxs-lookup"><span data-stu-id="880f5-176">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-177">-TopicName</span><span class="sxs-lookup"><span data-stu-id="880f5-177">-TopicName</span></span>
<span data-ttu-id="880f5-178">Namnet på ämnet där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="880f5-178">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880f5-179">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="880f5-179">-Confirm</span></span>
<span data-ttu-id="880f5-180">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="880f5-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="880f5-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="880f5-181">-WhatIf</span></span>
<span data-ttu-id="880f5-182">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="880f5-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="880f5-183">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="880f5-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="880f5-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880f5-184">CommonParameters</span></span>
<span data-ttu-id="880f5-185">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="880f5-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880f5-186">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="880f5-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880f5-187">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="880f5-187">INPUTS</span></span>

### <span data-ttu-id="880f5-188">System. String</span><span class="sxs-lookup"><span data-stu-id="880f5-188">System.String</span></span>

### <span data-ttu-id="880f5-189">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="880f5-189">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="880f5-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="880f5-190">OUTPUTS</span></span>

### <span data-ttu-id="880f5-191">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="880f5-191">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="880f5-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="880f5-192">NOTES</span></span>

## <span data-ttu-id="880f5-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="880f5-193">RELATED LINKS</span></span>
