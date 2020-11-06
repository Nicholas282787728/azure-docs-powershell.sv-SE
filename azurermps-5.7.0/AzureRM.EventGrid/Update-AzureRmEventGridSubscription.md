---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/update-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
ms.openlocfilehash: 7a6f7833a2b123a4f0235d331952b1403316df37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576530"
---
# <span data-ttu-id="ab076-101">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ab076-101">Update-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="ab076-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab076-102">SYNOPSIS</span></span>
<span data-ttu-id="ab076-103">Uppdatera egenskaperna för en händelse prenumeration för händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="ab076-103">Update the properties of an Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab076-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab076-104">SYNTAX</span></span>

### <span data-ttu-id="ab076-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ab076-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab076-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab076-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab076-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ab076-107">EventSubscriptionInputObjectSet</span></span>
```
Update-AzureRmEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab076-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab076-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab076-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab076-109">DESCRIPTION</span></span>
<span data-ttu-id="ab076-110">Uppdatera egenskaperna för en händelse prenumeration för händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="ab076-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="ab076-111">Det här kan användas för att uppdatera filter, mål eller etiketter för en befintlig händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ab076-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="ab076-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab076-112">EXAMPLES</span></span>

### <span data-ttu-id="ab076-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ab076-113">Example 1</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="ab076-114">Uppdaterar slut punkten för händelse abonnemangs \` es1 \` för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` till \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="ab076-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="ab076-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ab076-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzureRmEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="ab076-116">Uppdaterar slut punkten för händelse abonnemangs \` es1 \` för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` till \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="ab076-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="ab076-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ab076-117">Example 3</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="ab076-118">Uppdaterar egenskaperna för händelse prenumerationens \` es1 \` för EventHub-namnutrymmet ContosoNamespace med den nya slut punkten som \` https://requestb.in/1kxxoui1\ "och det nya SubjectEndsWith-filtret som \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="ab076-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="ab076-119">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="ab076-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="ab076-120">Uppdaterar egenskaperna för händelse prenumerationens \` es1 \` för resurs gruppen \` MyResourceGroupName \` med de nya etiketterna $Labels.</span><span class="sxs-lookup"><span data-stu-id="ab076-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="ab076-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab076-121">PARAMETERS</span></span>

### <span data-ttu-id="ab076-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab076-122">-DefaultProfile</span></span>
<span data-ttu-id="ab076-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab076-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab076-124">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="ab076-124">-Endpoint</span></span>
<span data-ttu-id="ab076-125">Destinations slut punkt för händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ab076-125">Event subscription destination endpoint.</span></span>
<span data-ttu-id="ab076-126">Detta kan vara en webhook-URL eller Azure-resurs-ID för en EventHub.</span><span class="sxs-lookup"><span data-stu-id="ab076-126">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab076-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="ab076-127">-EndpointType</span></span>
<span data-ttu-id="ab076-128">Typ av slut punkt.</span><span class="sxs-lookup"><span data-stu-id="ab076-128">Endpoint Type.</span></span>
<span data-ttu-id="ab076-129">Detta kan vara webhook eller eventhub</span><span class="sxs-lookup"><span data-stu-id="ab076-129">This can be webhook or eventhub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab076-130">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ab076-130">-EventSubscriptionName</span></span>
<span data-ttu-id="ab076-131">Namnet på händelse prenumerationen</span><span class="sxs-lookup"><span data-stu-id="ab076-131">The name of the event subscription</span></span>

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

### <span data-ttu-id="ab076-132">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="ab076-132">-IncludedEventType</span></span>
<span data-ttu-id="ab076-133">Filter som anger en lista över händelse typer som ska ingå. Om inget anges tas alla händelse typer med.</span><span class="sxs-lookup"><span data-stu-id="ab076-133">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab076-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab076-134">-InputObject</span></span>
<span data-ttu-id="ab076-135">EventGridSubscription-objekt.</span><span class="sxs-lookup"><span data-stu-id="ab076-135">EventGridSubscription object.</span></span>

```yaml
Type: PSEventSubscription
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab076-136">-Etikett</span><span class="sxs-lookup"><span data-stu-id="ab076-136">-Label</span></span>
<span data-ttu-id="ab076-137">Etiketter för händelse abonnemanget</span><span class="sxs-lookup"><span data-stu-id="ab076-137">Labels for the event subscription</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab076-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab076-138">-ResourceGroupName</span></span>
<span data-ttu-id="ab076-139">Ämnets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ab076-139">The resource group of the topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab076-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab076-140">-ResourceId</span></span>
<span data-ttu-id="ab076-141">ID för resursen som händelse prenumerationen skapades för.</span><span class="sxs-lookup"><span data-stu-id="ab076-141">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="ab076-142">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="ab076-142">-SubjectBeginsWith</span></span>
<span data-ttu-id="ab076-143">Filter som anger att endast händelser som matchar det angivna prefixet för subjektet kommer att ingå.</span><span class="sxs-lookup"><span data-stu-id="ab076-143">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="ab076-144">Om inget anges inkluderas händelser med alla ämnes prefix.</span><span class="sxs-lookup"><span data-stu-id="ab076-144">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab076-145">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="ab076-145">-SubjectEndsWith</span></span>
<span data-ttu-id="ab076-146">Filter som anger att endast händelser som matchar det angivna ämnes tillägget tas med.</span><span class="sxs-lookup"><span data-stu-id="ab076-146">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="ab076-147">Om inget anges inkluderas händelser med alla ämnes suffix.</span><span class="sxs-lookup"><span data-stu-id="ab076-147">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab076-148">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ab076-148">-TopicName</span></span>
<span data-ttu-id="ab076-149">Namnet på ämnet där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ab076-149">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab076-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab076-150">-Confirm</span></span>
<span data-ttu-id="ab076-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab076-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab076-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab076-152">-WhatIf</span></span>
<span data-ttu-id="ab076-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ab076-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab076-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ab076-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab076-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab076-155">CommonParameters</span></span>
<span data-ttu-id="ab076-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab076-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab076-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab076-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab076-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab076-158">INPUTS</span></span>

### <span data-ttu-id="ab076-159">System. String</span><span class="sxs-lookup"><span data-stu-id="ab076-159">System.String</span></span>
<span data-ttu-id="ab076-160">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription system. string []</span><span class="sxs-lookup"><span data-stu-id="ab076-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.String[]</span></span>

## <span data-ttu-id="ab076-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab076-161">OUTPUTS</span></span>

### <span data-ttu-id="ab076-162">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="ab076-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="ab076-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab076-163">NOTES</span></span>

## <span data-ttu-id="ab076-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab076-164">RELATED LINKS</span></span>

