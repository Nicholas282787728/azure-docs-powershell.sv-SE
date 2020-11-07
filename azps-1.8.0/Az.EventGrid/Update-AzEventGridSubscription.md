---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: a5aee2c8df132a4218ece171453e04d1224f7adc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754092"
---
# <span data-ttu-id="968dd-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="968dd-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="968dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="968dd-102">SYNOPSIS</span></span>
<span data-ttu-id="968dd-103">Uppdatera egenskaperna för en händelse prenumeration för händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="968dd-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="968dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="968dd-104">SYNTAX</span></span>

### <span data-ttu-id="968dd-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="968dd-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="968dd-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="968dd-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="968dd-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="968dd-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="968dd-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="968dd-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="968dd-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="968dd-109">DESCRIPTION</span></span>
<span data-ttu-id="968dd-110">Uppdatera egenskaperna för en händelse prenumeration för händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="968dd-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="968dd-111">Det här kan användas för att uppdatera filter, mål eller etiketter för en befintlig händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="968dd-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="968dd-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="968dd-112">EXAMPLES</span></span>

### <span data-ttu-id="968dd-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="968dd-113">Example 1</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="968dd-114">Uppdaterar slut punkten för händelse abonnemangs \` es1 \` för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` till \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="968dd-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="968dd-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="968dd-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="968dd-116">Uppdaterar slut punkten för händelse abonnemangs \` es1 \` för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` till \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="968dd-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="968dd-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="968dd-117">Example 3</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="968dd-118">Uppdaterar egenskaperna för händelse prenumerationens \` es1 \` för EventHub-namnutrymmet ContosoNamespace med den nya slut punkten som \` https://requestb.in/1kxxoui1\ "och det nya SubjectEndsWith-filtret som \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="968dd-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="968dd-119">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="968dd-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="968dd-120">Uppdaterar egenskaperna för händelse prenumerationens \` es1 \` för resurs gruppen \` MyResourceGroupName \` med de nya etiketterna $Labels.</span><span class="sxs-lookup"><span data-stu-id="968dd-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="968dd-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="968dd-121">PARAMETERS</span></span>

### <span data-ttu-id="968dd-122">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="968dd-122">-DeadLetterEndpoint</span></span>
<span data-ttu-id="968dd-123">Slut punkten som används för att lagra ej levererade händelser.</span><span class="sxs-lookup"><span data-stu-id="968dd-123">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="968dd-124">Ange Azure Resource ID för en lagrings-BLOB-behållare.</span><span class="sxs-lookup"><span data-stu-id="968dd-124">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="968dd-125">Till exempel:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="968dd-125">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="968dd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968dd-126">-DefaultProfile</span></span>
<span data-ttu-id="968dd-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="968dd-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="968dd-128">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="968dd-128">-Endpoint</span></span>
<span data-ttu-id="968dd-129">Destinations slut punkt för händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="968dd-129">Event subscription destination endpoint.</span></span>
<span data-ttu-id="968dd-130">Detta kan vara en webhook-URL eller Azure-resurs-ID för en EventHub-, lagringsprovider-eller hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="968dd-130">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="968dd-131">Resurs-ID för en hybrid anslutning har till exempel följande form:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="968dd-131">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="968dd-132">Det förväntas att mål slut punkten skapas och är tillgänglig för användning innan ett händelse rutnät körs.</span><span class="sxs-lookup"><span data-stu-id="968dd-132">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="968dd-133">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="968dd-133">-EndpointType</span></span>
<span data-ttu-id="968dd-134">Typ av slut punkt.</span><span class="sxs-lookup"><span data-stu-id="968dd-134">Endpoint Type.</span></span>
<span data-ttu-id="968dd-135">Detta kan vara webhook, eventhub, storagequeue eller hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="968dd-135">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="968dd-136">Standardvärdet är webhook.</span><span class="sxs-lookup"><span data-stu-id="968dd-136">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="968dd-137">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="968dd-137">-EventSubscriptionName</span></span>
<span data-ttu-id="968dd-138">Namnet på händelse prenumerationen</span><span class="sxs-lookup"><span data-stu-id="968dd-138">The name of the event subscription</span></span>

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

### <span data-ttu-id="968dd-139">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="968dd-139">-EventTtl</span></span>
<span data-ttu-id="968dd-140">Tid i minuter för händelse leverans.</span><span class="sxs-lookup"><span data-stu-id="968dd-140">The time in minutes for the event delivery.</span></span> <span data-ttu-id="968dd-141">Värdet måste vara mellan 1 och 1440</span><span class="sxs-lookup"><span data-stu-id="968dd-141">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="968dd-142">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="968dd-142">-IncludedEventType</span></span>
<span data-ttu-id="968dd-143">Filter som anger en lista över händelse typer som ska ingå. Om inget anges tas alla händelse typer med.</span><span class="sxs-lookup"><span data-stu-id="968dd-143">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="968dd-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="968dd-144">-InputObject</span></span>
<span data-ttu-id="968dd-145">EventGridSubscription-objekt.</span><span class="sxs-lookup"><span data-stu-id="968dd-145">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="968dd-146">-Etikett</span><span class="sxs-lookup"><span data-stu-id="968dd-146">-Label</span></span>
<span data-ttu-id="968dd-147">Etiketter för händelse abonnemanget</span><span class="sxs-lookup"><span data-stu-id="968dd-147">Labels for the event subscription</span></span>

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

### <span data-ttu-id="968dd-148">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="968dd-148">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="968dd-149">Maximalt antal försök att leverera händelsen.</span><span class="sxs-lookup"><span data-stu-id="968dd-149">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="968dd-150">Värdet måste vara mellan 1 och 30</span><span class="sxs-lookup"><span data-stu-id="968dd-150">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="968dd-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="968dd-151">-ResourceGroupName</span></span>
<span data-ttu-id="968dd-152">Ämnets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="968dd-152">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="968dd-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="968dd-153">-ResourceId</span></span>
<span data-ttu-id="968dd-154">ID för resursen som händelse prenumerationen skapades för.</span><span class="sxs-lookup"><span data-stu-id="968dd-154">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="968dd-155">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="968dd-155">-SubjectBeginsWith</span></span>
<span data-ttu-id="968dd-156">Filter som anger att endast händelser som matchar det angivna prefixet för subjektet kommer att ingå.</span><span class="sxs-lookup"><span data-stu-id="968dd-156">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="968dd-157">Om inget anges inkluderas händelser med alla ämnes prefix.</span><span class="sxs-lookup"><span data-stu-id="968dd-157">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="968dd-158">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="968dd-158">-SubjectEndsWith</span></span>
<span data-ttu-id="968dd-159">Filter som anger att endast händelser som matchar det angivna ämnes tillägget tas med.</span><span class="sxs-lookup"><span data-stu-id="968dd-159">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="968dd-160">Om inget anges inkluderas händelser med alla ämnes suffix.</span><span class="sxs-lookup"><span data-stu-id="968dd-160">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="968dd-161">-TopicName</span><span class="sxs-lookup"><span data-stu-id="968dd-161">-TopicName</span></span>
<span data-ttu-id="968dd-162">Namnet på ämnet där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="968dd-162">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="968dd-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="968dd-163">-Confirm</span></span>
<span data-ttu-id="968dd-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="968dd-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="968dd-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="968dd-165">-WhatIf</span></span>
<span data-ttu-id="968dd-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="968dd-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="968dd-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="968dd-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="968dd-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968dd-168">CommonParameters</span></span>
<span data-ttu-id="968dd-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="968dd-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968dd-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="968dd-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968dd-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="968dd-171">INPUTS</span></span>

### <span data-ttu-id="968dd-172">System. String</span><span class="sxs-lookup"><span data-stu-id="968dd-172">System.String</span></span>

### <span data-ttu-id="968dd-173">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="968dd-173">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="968dd-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="968dd-174">OUTPUTS</span></span>

### <span data-ttu-id="968dd-175">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="968dd-175">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="968dd-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="968dd-176">NOTES</span></span>

## <span data-ttu-id="968dd-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="968dd-177">RELATED LINKS</span></span>
