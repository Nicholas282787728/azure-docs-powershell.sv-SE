---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: c1eff968bf72c77e6b4e1c2aedfe50459ec3faef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271934"
---
# <span data-ttu-id="8ed0e-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8ed0e-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="8ed0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ed0e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed0e-103">Skapar en ny händelse prenumeration för Azure händelse rutnät till ett ämne, Azure Resource, Azure-abonnemang eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="8ed0e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ed0e-104">SYNTAX</span></span>

### <span data-ttu-id="8ed0e-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8ed0e-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed0e-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ed0e-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed0e-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ed0e-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed0e-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ed0e-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed0e-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ed0e-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed0e-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ed0e-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed0e-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ed0e-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed0e-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ed0e-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [-EndpointType <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ed0e-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ed0e-113">DESCRIPTION</span></span>
<span data-ttu-id="8ed0e-114">Skapa en ny händelse prenumeration i ett avsnitt i ett Azure-evenemang, en Azure-resurs som stöds, en Azure-prenumeration eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="8ed0e-115">Om du vill skapa en händelse prenumeration för det markerade Azure-abonnemanget anger du händelse prenumerationens namn och mål slut punkten.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="8ed0e-116">Om du vill skapa en händelse prenumeration i en resurs grupp anger du resurs gruppens namn förutom händelse prenumerationens namn och mål slut punkten.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="8ed0e-117">Om du vill skapa en händelse prenumeration i ett avsnitt i ett Azure-evenemang kan du ange ämnets namn.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="8ed0e-118">Om du vill skapa en händelse prenumeration till en Azure-resurs som stöds anger du resursens fullständiga resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="8ed0e-119">Kör cmdleten Get-AzEventGridTopicType om du vill visa listan över typer som stöds.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="8ed0e-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ed0e-120">EXAMPLES</span></span>

### <span data-ttu-id="8ed0e-121">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8ed0e-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8ed0e-122">Skapar en ny händelse prenumerations \` EventSubscription1 \` till ett ämne i en Azure- \` Ämne1 \` i resurs grupps \` MyResourceGroupName \` med webhookens destinations slut punkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="8ed0e-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="8ed0e-123">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="8ed0e-124">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8ed0e-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8ed0e-125">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till en resurs grupp \` MyResourceGroupName \` med slut punkten för webhook-destinationen https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="8ed0e-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="8ed0e-126">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="8ed0e-127">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8ed0e-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8ed0e-128">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till det markerade Azure-abonnemanget med webhook-destinationens slut punkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="8ed0e-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="8ed0e-129">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="8ed0e-130">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="8ed0e-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="8ed0e-131">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till det markerade Azure-abonnemanget med webhook-destinationens slut punkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="8ed0e-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="8ed0e-132">Den här händelse prenumerationen anger ytterligare filter för händelse typer och ämne, och endast händelser som matchar dessa filter skickas till mål slut punkten.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="8ed0e-133">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="8ed0e-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="8ed0e-134">Skapar en ny händelse- \` EventSubscription1 \` till det markerade Azure-abonnemanget med den angivna händelsehubben som mål för händelser.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="8ed0e-135">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="8ed0e-136">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="8ed0e-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8ed0e-137">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till ett EventHub-namnområde med den angivna webhook-destinationens slut punkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="8ed0e-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="8ed0e-138">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="8ed0e-139">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ed0e-139">PARAMETERS</span></span>

### <span data-ttu-id="8ed0e-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="8ed0e-140">-AdvancedFilter</span></span>
<span data-ttu-id="8ed0e-141">Avancerat filter som anger en matris med flera hash-värden som används för serverbaserad filtrering.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="8ed0e-142">Varje hash-värde har följande nycklar-värde info: operation, nyckel och värde eller värden.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="8ed0e-143">Operatorn kan vara något av följande värden: numberin, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, Stringin, StringNotIn, StringBeginsWith, StringEndsWith eller StringContains.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="8ed0e-144">Nyckel representerar egenskapen nytto Last där de avancerade filtrerings principerna tillämpas.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="8ed0e-145">Till sist representerar värdet eller värdena värdena som ska matchas.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="8ed0e-146">Det kan vara ett enskilt värde av motsvarande typ eller en matris med värden.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="8ed0e-147">Som exempel på avancerade filter parametrar: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) där $AdvFilter 1 = @ {Operator = "Nummerin"; Key = "data. KEY1"; Värden = @ (1, 2)} och $AdvFilter 2 = @ {Operator = "StringBringsWith"; Key = "ämne"; Värden = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="8ed0e-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="8ed0e-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="8ed0e-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="8ed0e-149">ID eller URI för Azure Active Directory-programmet (AAD) för att hämta åtkomst-token som ska inkluderas som Bearer-token i leverans förfrågningar. Gäller bara webhook som mål.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="8ed0e-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="8ed0e-151">Klient-ID: t för Azure Active Directory (AAD) för att få åtkomsttoken som kommer att inkluderas som Bearer-token i leverans förfrågningar. Gäller bara webhook som mål.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ed0e-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="8ed0e-153">Slut punkten som används för att lagra ej levererade händelser.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="8ed0e-154">Ange Azure Resource ID för en lagrings-BLOB-behållare.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="8ed0e-155">Till exempel:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="8ed0e-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed0e-156">-DefaultProfile</span></span>
<span data-ttu-id="8ed0e-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8ed0e-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ed0e-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="8ed0e-158">-DeliverySchema</span></span>
<span data-ttu-id="8ed0e-159">Schemat som ska användas när du levererar händelser till målet.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="8ed0e-160">Möjliga värden är: eventgridschema, CustomInputSchema eller cloudeventv01schema.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="8ed0e-161">Standardvärdet är CustomInputSchema.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-161">Default value is CustomInputSchema.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="8ed0e-162">-DomainInputObject</span></span>
<span data-ttu-id="8ed0e-163">EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-163">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-164">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="8ed0e-164">-DomainName</span></span>
<span data-ttu-id="8ed0e-165">Namnet på den domän i händelse rutnätet där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="8ed0e-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="8ed0e-167">EventGrid Domain-objekt.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-167">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="8ed0e-168">-DomainTopicName</span></span>
<span data-ttu-id="8ed0e-169">Namnet på den domän där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-169">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-170">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="8ed0e-170">-Endpoint</span></span>
<span data-ttu-id="8ed0e-171">Destinations slut punkt för händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="8ed0e-172">Detta kan vara en webhook-URL eller Azure-resurs-ID för en EventHub, lagringsprovider, hybridconnection eller servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="8ed0e-173">Resurs-ID för en hybrid anslutning har till exempel följande form:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="8ed0e-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="8ed0e-174">Det förväntas att mål slut punkten skapas och är tillgänglig för användning innan ett händelse rutnät körs.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="8ed0e-175">-EndpointType</span></span>
<span data-ttu-id="8ed0e-176">Typ av slut punkt.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-176">Endpoint Type.</span></span>
<span data-ttu-id="8ed0e-177">Det här kan vara webhook, eventhub, storagequeue, hybridconnection eller servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="8ed0e-178">Standardvärdet är webhook.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-178">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8ed0e-179">-EventSubscriptionName</span></span>
<span data-ttu-id="8ed0e-180">Namnet på händelse prenumerationen</span><span class="sxs-lookup"><span data-stu-id="8ed0e-180">The name of the event subscription</span></span>

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

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="8ed0e-181">-EventTtl</span></span>
<span data-ttu-id="8ed0e-182">Tid i minuter för händelse leverans.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="8ed0e-183">Värdet måste vara mellan 1 och 1440</span><span class="sxs-lookup"><span data-stu-id="8ed0e-183">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-184">-Förfallo</span><span class="sxs-lookup"><span data-stu-id="8ed0e-184">-ExpirationDate</span></span>
<span data-ttu-id="8ed0e-185">Avgör förfallo dag/tid för händelse prenumerationen efter vilken händelse prenumerationen dras tillbaka.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="8ed0e-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="8ed0e-186">-IncludedEventType</span></span>
<span data-ttu-id="8ed0e-187">Filter som anger en lista över händelse typer som ska ingå. Om inget anges tas alla händelse typer med.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-188">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ed0e-188">-InputObject</span></span>
<span data-ttu-id="8ed0e-189">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="8ed0e-190">-Etikett</span><span class="sxs-lookup"><span data-stu-id="8ed0e-190">-Label</span></span>
<span data-ttu-id="8ed0e-191">Etiketter för händelse abonnemanget</span><span class="sxs-lookup"><span data-stu-id="8ed0e-191">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="8ed0e-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="8ed0e-193">Maximalt antal försök att leverera händelsen.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="8ed0e-194">Värdet måste vara mellan 1 och 30</span><span class="sxs-lookup"><span data-stu-id="8ed0e-194">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="8ed0e-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="8ed0e-196">Maximalt antal händelser i en grupp.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="8ed0e-197">Värdet måste vara mellan 1 och 5000.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="8ed0e-198">Den här parametern är giltig när Endpint-typen endast är webhook.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-198">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="8ed0e-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="8ed0e-200">Önskad batchstorlek i kilobyte.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="8ed0e-201">Värdet måste vara mellan 1 och 1024.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="8ed0e-202">Den här parametern är giltig när Endpint-typen endast är webhook.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-202">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ed0e-203">-ResourceGroupName</span></span>
<span data-ttu-id="8ed0e-204">Ämnets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-204">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ed0e-205">-ResourceId</span></span>
<span data-ttu-id="8ed0e-206">ID för den resurs som händelse prenumerationen ska skapas för.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="8ed0e-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="8ed0e-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="8ed0e-208">Filter som anger att endast händelser som matchar det angivna prefixet för subjektet kommer att ingå.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="8ed0e-209">Om inget anges inkluderas händelser med alla ämnes prefix.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-209">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="8ed0e-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="8ed0e-211">Filter som anger att ämnes fältet ska jämföras på ett skift läge.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="8ed0e-212">Om det inte anges jämförs ämnet med ett skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="8ed0e-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="8ed0e-213">-SubjectEndsWith</span></span>
<span data-ttu-id="8ed0e-214">Filter som anger att endast händelser som matchar det angivna ämnes tillägget tas med.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="8ed0e-215">Om inget anges inkluderas händelser med alla ämnes suffix.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-215">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0e-216">-TopicName</span><span class="sxs-lookup"><span data-stu-id="8ed0e-216">-TopicName</span></span>
<span data-ttu-id="8ed0e-217">Namnet på ämnet där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="8ed0e-218">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8ed0e-218">-Confirm</span></span>
<span data-ttu-id="8ed0e-219">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ed0e-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ed0e-220">-WhatIf</span></span>
<span data-ttu-id="8ed0e-221">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ed0e-222">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ed0e-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed0e-223">CommonParameters</span></span>
<span data-ttu-id="8ed0e-224">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed0e-225">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ed0e-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed0e-226">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ed0e-226">INPUTS</span></span>

### <span data-ttu-id="8ed0e-227">System. String</span><span class="sxs-lookup"><span data-stu-id="8ed0e-227">System.String</span></span>

### <span data-ttu-id="8ed0e-228">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="8ed0e-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="8ed0e-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="8ed0e-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="8ed0e-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8ed0e-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="8ed0e-231">System. string []</span><span class="sxs-lookup"><span data-stu-id="8ed0e-231">System.String[]</span></span>

### <span data-ttu-id="8ed0e-232">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8ed0e-232">System.Int32</span></span>

## <span data-ttu-id="8ed0e-233">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ed0e-233">OUTPUTS</span></span>

### <span data-ttu-id="8ed0e-234">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="8ed0e-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="8ed0e-235">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ed0e-235">NOTES</span></span>

## <span data-ttu-id="8ed0e-236">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ed0e-236">RELATED LINKS</span></span>
