---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 1c0391fa266e498c717bc4eb43bd92ab93be508f
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395194"
---
# <span data-ttu-id="0d986-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0d986-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="0d986-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d986-102">SYNOPSIS</span></span>
<span data-ttu-id="0d986-103">Skapar en ny händelse prenumeration för Azure händelse rutnät till ett ämne, Azure Resource, Azure-abonnemang eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0d986-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="0d986-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d986-104">SYNTAX</span></span>

### <span data-ttu-id="0d986-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0d986-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d986-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d986-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d986-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d986-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d986-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d986-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d986-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d986-109">DESCRIPTION</span></span>
<span data-ttu-id="0d986-110">Skapa en ny händelse prenumeration i ett avsnitt i ett Azure-evenemang, en Azure-resurs som stöds, en Azure-prenumeration eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0d986-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="0d986-111">Om du vill skapa en händelse prenumeration för det markerade Azure-abonnemanget anger du händelse prenumerationens namn och mål slut punkten.</span><span class="sxs-lookup"><span data-stu-id="0d986-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="0d986-112">Om du vill skapa en händelse prenumeration i en resurs grupp anger du resurs gruppens namn förutom händelse prenumerationens namn och mål slut punkten.</span><span class="sxs-lookup"><span data-stu-id="0d986-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="0d986-113">Om du vill skapa en händelse prenumeration i ett avsnitt i ett Azure-evenemang kan du ange ämnets namn.</span><span class="sxs-lookup"><span data-stu-id="0d986-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="0d986-114">Om du vill skapa en händelse prenumeration till en Azure-resurs som stöds anger du resursens fullständiga resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="0d986-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="0d986-115">Kör cmdleten Get-AzEventGridTopicType om du vill visa listan över typer som stöds.</span><span class="sxs-lookup"><span data-stu-id="0d986-115">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="0d986-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d986-116">EXAMPLES</span></span>

### <span data-ttu-id="0d986-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0d986-117">Example 1</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0d986-118">Skapar en ny händelse prenumerations \` EventSubscription1 \` till ett ämne i en Azure- \` Ämne1 \` i resurs grupps \` MyResourceGroupName \` med webhookens destinations slut punkt `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="0d986-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="0d986-119">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="0d986-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0d986-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0d986-120">Example 2</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0d986-121">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till en resurs grupp \` MyResourceGroupName \` med slut punkten för webhook-destinationen `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="0d986-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="0d986-122">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="0d986-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0d986-123">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="0d986-123">Example 3</span></span>
```
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0d986-124">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till det markerade Azure-abonnemanget med webhook-destinationens slut punkt `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="0d986-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="0d986-125">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="0d986-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0d986-126">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="0d986-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="0d986-127">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till det markerade Azure-abonnemanget med webhook-destinationens slut punkt `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="0d986-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="0d986-128">Den här händelse prenumerationen anger ytterligare filter för händelse typer och ämne, och endast händelser som matchar dessa filter skickas till mål slut punkten.</span><span class="sxs-lookup"><span data-stu-id="0d986-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="0d986-129">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="0d986-129">Example 5</span></span>
```
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="0d986-130">Skapar en ny händelse- \` EventSubscription1 \` till det markerade Azure-abonnemanget med den angivna händelsehubben som mål för händelser.</span><span class="sxs-lookup"><span data-stu-id="0d986-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="0d986-131">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="0d986-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="0d986-132">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="0d986-132">Example 6</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0d986-133">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till ett EventHub-namnområde med den angivna webhook-destinationens slut punkt `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="0d986-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="0d986-134">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="0d986-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="0d986-135">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d986-135">PARAMETERS</span></span>

### <span data-ttu-id="0d986-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d986-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="0d986-137">Slut punkten som används för att lagra ej levererade händelser.</span><span class="sxs-lookup"><span data-stu-id="0d986-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="0d986-138">Ange Azure Resource ID för en lagrings-BLOB-behållare.</span><span class="sxs-lookup"><span data-stu-id="0d986-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="0d986-139">Till exempel:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="0d986-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d986-140">-DefaultProfile</span></span>
<span data-ttu-id="0d986-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0d986-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d986-142">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="0d986-142">-Endpoint</span></span>
<span data-ttu-id="0d986-143">Destinations slut punkt för händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0d986-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="0d986-144">Detta kan vara en webhook-URL eller Azure-resurs-ID för en EventHub-, lagringsprovider-eller hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="0d986-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="0d986-145">Resurs-ID för en hybrid anslutning har till exempel följande form:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="0d986-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="0d986-146">Det förväntas att mål slut punkten skapas och är tillgänglig för användning innan ett händelse rutnät körs.</span><span class="sxs-lookup"><span data-stu-id="0d986-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="0d986-147">-EndpointType</span></span>
<span data-ttu-id="0d986-148">Typ av slut punkt.</span><span class="sxs-lookup"><span data-stu-id="0d986-148">Endpoint Type.</span></span>
<span data-ttu-id="0d986-149">Detta kan vara webhook, eventhub, storagequeue eller hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="0d986-149">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="0d986-150">Standardvärdet är webhook.</span><span class="sxs-lookup"><span data-stu-id="0d986-150">Default value is webhook.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0d986-151">-EventSubscriptionName</span></span>
<span data-ttu-id="0d986-152">Namnet på händelse prenumerationen</span><span class="sxs-lookup"><span data-stu-id="0d986-152">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="0d986-153">-EventTtl</span></span>
<span data-ttu-id="0d986-154">Tid i minuter för händelse leverans.</span><span class="sxs-lookup"><span data-stu-id="0d986-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="0d986-155">Värdet måste vara mellan 1 och 1440</span><span class="sxs-lookup"><span data-stu-id="0d986-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-156">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="0d986-156">-IncludedEventType</span></span>
<span data-ttu-id="0d986-157">Filter som anger en lista över händelse typer som ska ingå. Om inget anges tas alla händelse typer med.</span><span class="sxs-lookup"><span data-stu-id="0d986-157">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d986-158">-InputObject</span></span>
<span data-ttu-id="0d986-159">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="0d986-159">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-160">-Etikett</span><span class="sxs-lookup"><span data-stu-id="0d986-160">-Label</span></span>
<span data-ttu-id="0d986-161">Etiketter för händelse abonnemanget</span><span class="sxs-lookup"><span data-stu-id="0d986-161">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-162">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="0d986-162">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="0d986-163">Maximalt antal försök att leverera händelsen.</span><span class="sxs-lookup"><span data-stu-id="0d986-163">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="0d986-164">Värdet måste vara mellan 1 och 30</span><span class="sxs-lookup"><span data-stu-id="0d986-164">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d986-165">-ResourceGroupName</span></span>
<span data-ttu-id="0d986-166">Ämnets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0d986-166">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d986-167">-ResourceId</span></span>
<span data-ttu-id="0d986-168">ID för den resurs som händelse prenumerationen ska skapas för.</span><span class="sxs-lookup"><span data-stu-id="0d986-168">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="0d986-169">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="0d986-169">-SubjectBeginsWith</span></span>
<span data-ttu-id="0d986-170">Filter som anger att endast händelser som matchar det angivna prefixet för subjektet kommer att ingå.</span><span class="sxs-lookup"><span data-stu-id="0d986-170">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="0d986-171">Om inget anges inkluderas händelser med alla ämnes prefix.</span><span class="sxs-lookup"><span data-stu-id="0d986-171">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-172">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="0d986-172">-SubjectCaseSensitive</span></span>
<span data-ttu-id="0d986-173">Filter som anger att ämnes fältet ska jämföras på ett skift läge.</span><span class="sxs-lookup"><span data-stu-id="0d986-173">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="0d986-174">Om det inte anges jämförs ämnet med ett skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="0d986-174">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="0d986-175">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="0d986-175">-SubjectEndsWith</span></span>
<span data-ttu-id="0d986-176">Filter som anger att endast händelser som matchar det angivna ämnes tillägget tas med.</span><span class="sxs-lookup"><span data-stu-id="0d986-176">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="0d986-177">Om inget anges inkluderas händelser med alla ämnes suffix.</span><span class="sxs-lookup"><span data-stu-id="0d986-177">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-178">-TopicName</span><span class="sxs-lookup"><span data-stu-id="0d986-178">-TopicName</span></span>
<span data-ttu-id="0d986-179">Namnet på ämnet där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0d986-179">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d986-180">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d986-180">-Confirm</span></span>
<span data-ttu-id="0d986-181">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d986-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d986-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d986-182">-WhatIf</span></span>
<span data-ttu-id="0d986-183">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d986-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d986-184">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d986-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d986-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d986-185">CommonParameters</span></span>
<span data-ttu-id="0d986-186">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d986-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d986-187">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d986-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d986-188">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d986-188">INPUTS</span></span>

### <span data-ttu-id="0d986-189">System. String</span><span class="sxs-lookup"><span data-stu-id="0d986-189">System.String</span></span>

### <span data-ttu-id="0d986-190">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="0d986-190">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="0d986-191">System. string []</span><span class="sxs-lookup"><span data-stu-id="0d986-191">System.String[]</span></span>

## <span data-ttu-id="0d986-192">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d986-192">OUTPUTS</span></span>

### <span data-ttu-id="0d986-193">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="0d986-193">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="0d986-194">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d986-194">NOTES</span></span>

## <span data-ttu-id="0d986-195">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d986-195">RELATED LINKS</span></span>
