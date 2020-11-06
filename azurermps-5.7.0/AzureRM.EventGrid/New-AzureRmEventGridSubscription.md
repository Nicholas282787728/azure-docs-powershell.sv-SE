---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: 0c5c0f0f9739a2f9481989a69ece9aa29f0c67e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580440"
---
# <span data-ttu-id="45436-101">New-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="45436-101">New-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="45436-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45436-102">SYNOPSIS</span></span>
<span data-ttu-id="45436-103">Skapar en ny händelse prenumeration för Azure händelse rutnät till ett ämne, Azure Resource, Azure-abonnemang eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="45436-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45436-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45436-104">SYNTAX</span></span>

### <span data-ttu-id="45436-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="45436-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45436-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="45436-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45436-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="45436-107">EventSubscriptionInputObjectSet</span></span>
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45436-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="45436-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45436-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45436-109">DESCRIPTION</span></span>
<span data-ttu-id="45436-110">Skapa en ny händelse prenumeration i ett avsnitt i ett Azure-evenemang, en Azure-resurs som stöds, en Azure-prenumeration eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="45436-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="45436-111">Om du vill skapa en händelse prenumeration för det markerade Azure-abonnemanget anger du händelse prenumerationens namn och mål slut punkten.</span><span class="sxs-lookup"><span data-stu-id="45436-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="45436-112">Om du vill skapa en händelse prenumeration i en resurs grupp anger du resurs gruppens namn förutom händelse prenumerationens namn och mål slut punkten.</span><span class="sxs-lookup"><span data-stu-id="45436-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="45436-113">Om du vill skapa en händelse prenumeration i ett avsnitt i ett Azure-evenemang kan du ange ämnets namn.</span><span class="sxs-lookup"><span data-stu-id="45436-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="45436-114">Om du vill skapa en händelse prenumeration till en Azure-resurs som stöds anger du resursens fullständiga resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="45436-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="45436-115">Kör cmdleten Get-AzureRmEventGridTopicType om du vill visa listan över typer som stöds.</span><span class="sxs-lookup"><span data-stu-id="45436-115">To view the list of supported types, run the Get-AzureRmEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="45436-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45436-116">EXAMPLES</span></span>

### <span data-ttu-id="45436-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="45436-117">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="45436-118">Skapar en ny händelse prenumerations \` EventSubscription1 \` till ett ämne i en Azure- \` Ämne1 \` i resurs grupps \` MyResourceGroupName \` med webhookens destinations slut punkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="45436-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="45436-119">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="45436-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="45436-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="45436-120">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="45436-121">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till en resurs grupp \` MyResourceGroupName \` med slut punkten för webhook-destinationen https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="45436-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="45436-122">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="45436-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="45436-123">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="45436-123">Example 3</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="45436-124">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till det markerade Azure-abonnemanget med webhook-destinationens slut punkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="45436-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="45436-125">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="45436-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="45436-126">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="45436-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="45436-127">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till det markerade Azure-abonnemanget med webhook-destinationens slut punkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="45436-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="45436-128">Den här händelse prenumerationen anger ytterligare filter för händelse typer och ämne, och endast händelser som matchar dessa filter skickas till mål slut punkten.</span><span class="sxs-lookup"><span data-stu-id="45436-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="45436-129">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="45436-129">Example 5</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="45436-130">Skapar en ny händelse- \` EventSubscription1 \` till det markerade Azure-abonnemanget med den angivna händelsehubben som mål för händelser.</span><span class="sxs-lookup"><span data-stu-id="45436-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="45436-131">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="45436-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="45436-132">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="45436-132">Example 6</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="45436-133">Skapar en ny händelse prenumerations- \` EventSubscription1 \` till ett EventHub-namnområde med den angivna webhhok-destinations slut punkten https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="45436-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="45436-134">Den här händelse prenumerationen använder standard filter.</span><span class="sxs-lookup"><span data-stu-id="45436-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="45436-135">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45436-135">PARAMETERS</span></span>

### <span data-ttu-id="45436-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45436-136">-DefaultProfile</span></span>
<span data-ttu-id="45436-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="45436-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45436-138">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="45436-138">-Endpoint</span></span>
<span data-ttu-id="45436-139">Destinations slut punkt för händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="45436-139">Event subscription destination endpoint.</span></span>
<span data-ttu-id="45436-140">Detta kan vara en webhook-URL eller Azure-resurs-ID för en EventHub.</span><span class="sxs-lookup"><span data-stu-id="45436-140">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45436-141">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="45436-141">-EndpointType</span></span>
<span data-ttu-id="45436-142">Typ av slut punkt.</span><span class="sxs-lookup"><span data-stu-id="45436-142">Endpoint Type.</span></span>
<span data-ttu-id="45436-143">Detta kan vara webhook eller eventhub</span><span class="sxs-lookup"><span data-stu-id="45436-143">This can be webhook or eventhub</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45436-144">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="45436-144">-EventSubscriptionName</span></span>
<span data-ttu-id="45436-145">Namnet på händelse prenumerationen</span><span class="sxs-lookup"><span data-stu-id="45436-145">The name of the event subscription</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45436-146">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="45436-146">-IncludedEventType</span></span>
<span data-ttu-id="45436-147">Filter som anger en lista över händelse typer som ska ingå. Om inget anges tas alla händelse typer med.</span><span class="sxs-lookup"><span data-stu-id="45436-147">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45436-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45436-148">-InputObject</span></span>
<span data-ttu-id="45436-149">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="45436-149">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45436-150">-Etikett</span><span class="sxs-lookup"><span data-stu-id="45436-150">-Label</span></span>
<span data-ttu-id="45436-151">Etiketter för händelse abonnemanget</span><span class="sxs-lookup"><span data-stu-id="45436-151">Labels for the event subscription</span></span>

```yaml
Type: String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45436-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45436-152">-ResourceGroupName</span></span>
<span data-ttu-id="45436-153">Ämnets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="45436-153">The resource group of the topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45436-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45436-154">-ResourceId</span></span>
<span data-ttu-id="45436-155">ID för den resurs som händelse prenumerationen ska skapas för.</span><span class="sxs-lookup"><span data-stu-id="45436-155">The identifier of the resource to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45436-156">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="45436-156">-SubjectBeginsWith</span></span>
<span data-ttu-id="45436-157">Filter som anger att endast händelser som matchar det angivna prefixet för subjektet kommer att ingå.</span><span class="sxs-lookup"><span data-stu-id="45436-157">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="45436-158">Om inget anges inkluderas händelser med alla ämnes prefix.</span><span class="sxs-lookup"><span data-stu-id="45436-158">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45436-159">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="45436-159">-SubjectCaseSensitive</span></span>
<span data-ttu-id="45436-160">Filter som anger att ämnes fältet ska jämföras på ett skift läge.</span><span class="sxs-lookup"><span data-stu-id="45436-160">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="45436-161">Om det inte anges jämförs ämnet med ett skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="45436-161">If not specified, subject will be compared in a case insensitive manner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45436-162">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="45436-162">-SubjectEndsWith</span></span>
<span data-ttu-id="45436-163">Filter som anger att endast händelser som matchar det angivna ämnes tillägget tas med.</span><span class="sxs-lookup"><span data-stu-id="45436-163">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="45436-164">Om inget anges inkluderas händelser med alla ämnes suffix.</span><span class="sxs-lookup"><span data-stu-id="45436-164">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45436-165">-TopicName</span><span class="sxs-lookup"><span data-stu-id="45436-165">-TopicName</span></span>
<span data-ttu-id="45436-166">Namnet på ämnet där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="45436-166">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45436-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45436-167">-Confirm</span></span>
<span data-ttu-id="45436-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45436-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45436-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45436-169">-WhatIf</span></span>
<span data-ttu-id="45436-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45436-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45436-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45436-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45436-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45436-172">CommonParameters</span></span>
<span data-ttu-id="45436-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45436-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45436-174">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45436-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45436-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45436-175">INPUTS</span></span>

### <span data-ttu-id="45436-176">System. String</span><span class="sxs-lookup"><span data-stu-id="45436-176">System.String</span></span>
<span data-ttu-id="45436-177">Microsoft. Azure. commands. EventGrid. Models. PSTopic system. Management. Automation. SwitchParameter system. string []</span><span class="sxs-lookup"><span data-stu-id="45436-177">Microsoft.Azure.Commands.EventGrid.Models.PSTopic System.Management.Automation.SwitchParameter System.String[]</span></span>

## <span data-ttu-id="45436-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45436-178">OUTPUTS</span></span>

### <span data-ttu-id="45436-179">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="45436-179">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="45436-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45436-180">NOTES</span></span>

## <span data-ttu-id="45436-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45436-181">RELATED LINKS</span></span>

