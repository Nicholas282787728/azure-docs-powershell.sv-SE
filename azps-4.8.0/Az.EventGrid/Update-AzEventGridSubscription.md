---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262703"
---
# <span data-ttu-id="c7fea-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c7fea-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="c7fea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7fea-102">SYNOPSIS</span></span>
<span data-ttu-id="c7fea-103">Uppdatera egenskaperna för en händelse prenumeration för händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="c7fea-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="c7fea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7fea-104">SYNTAX</span></span>

### <span data-ttu-id="c7fea-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c7fea-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7fea-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7fea-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7fea-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7fea-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7fea-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7fea-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7fea-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7fea-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7fea-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7fea-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7fea-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7fea-111">DESCRIPTION</span></span>
<span data-ttu-id="c7fea-112">Uppdatera egenskaperna för en händelse prenumeration för händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="c7fea-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="c7fea-113">Det här kan användas för att uppdatera filter, mål eller etiketter för en befintlig händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c7fea-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="c7fea-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7fea-114">EXAMPLES</span></span>

### <span data-ttu-id="c7fea-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c7fea-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="c7fea-116">Uppdaterar slut punkten för händelse abonnemangs \` es1 \` för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` till \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="c7fea-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="c7fea-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c7fea-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="c7fea-118">Uppdaterar slut punkten för händelse abonnemangs \` es1 \` för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` till \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="c7fea-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="c7fea-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c7fea-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="c7fea-120">Uppdaterar egenskaperna för händelse prenumerationens \` es1 \` för EventHub-namnutrymmet ContosoNamespace med den nya slut punkten som \` https://requestb.in/1kxxoui1\ "och det nya SubjectEndsWith-filtret som \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="c7fea-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="c7fea-121">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="c7fea-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="c7fea-122">Uppdaterar egenskaperna för händelse prenumerationens \` es1 \` för resurs gruppen \` MyResourceGroupName \` med de nya etiketterna $Labels.</span><span class="sxs-lookup"><span data-stu-id="c7fea-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="c7fea-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7fea-123">PARAMETERS</span></span>

### <span data-ttu-id="c7fea-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="c7fea-124">-AdvancedFilter</span></span>
<span data-ttu-id="c7fea-125">Avancerat filter som anger en matris med flera hash-värden som används för serverbaserad filtrering.</span><span class="sxs-lookup"><span data-stu-id="c7fea-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="c7fea-126">Varje hash-värde har följande nycklar-värde info: operation, nyckel och värde eller värden.</span><span class="sxs-lookup"><span data-stu-id="c7fea-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="c7fea-127">Operatorn kan vara något av följande värden: numberin, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, Stringin, StringNotIn, StringBeginsWith, StringEndsWith eller StringContains.</span><span class="sxs-lookup"><span data-stu-id="c7fea-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="c7fea-128">Nyckel representerar egenskapen nytto Last där de avancerade filtrerings principerna tillämpas.</span><span class="sxs-lookup"><span data-stu-id="c7fea-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="c7fea-129">Till sist representerar värdet eller värdena värdena som ska matchas.</span><span class="sxs-lookup"><span data-stu-id="c7fea-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="c7fea-130">Det kan vara ett enskilt värde av motsvarande typ eller en matris med värden.</span><span class="sxs-lookup"><span data-stu-id="c7fea-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="c7fea-131">Som exempel på avancerade filter parametrar: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) där $AdvFilter 1 = @ {Operator = "Nummerin"; Key = "data. KEY1"; Värden = @ (1, 2)} och $AdvFilter 2 = @ {Operator = "StringBeginsWith"; Key = "ämne"; Värden = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="c7fea-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="c7fea-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="c7fea-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="c7fea-133">ID eller URI för Azure Active Directory-programmet (AAD) för att hämta åtkomst-token som ska inkluderas som Bearer-token i leverans förfrågningar. Gäller bara webhook som mål.</span><span class="sxs-lookup"><span data-stu-id="c7fea-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7fea-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="c7fea-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="c7fea-135">Klient-ID: t för Azure Active Directory (AAD) för att få åtkomsttoken som kommer att inkluderas som Bearer-token i leverans förfrågningar. Gäller bara webhook som mål.</span><span class="sxs-lookup"><span data-stu-id="c7fea-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7fea-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7fea-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="c7fea-137">Slut punkten som används för att lagra ej levererade händelser.</span><span class="sxs-lookup"><span data-stu-id="c7fea-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="c7fea-138">Ange Azure Resource ID för en lagrings-BLOB-behållare.</span><span class="sxs-lookup"><span data-stu-id="c7fea-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="c7fea-139">Till exempel:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="c7fea-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="c7fea-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7fea-140">-DefaultProfile</span></span>
<span data-ttu-id="c7fea-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7fea-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7fea-142">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="c7fea-142">-DomainName</span></span>
<span data-ttu-id="c7fea-143">Namnet på den domän där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="c7fea-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="c7fea-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="c7fea-144">-DomainTopicName</span></span>
<span data-ttu-id="c7fea-145">Namnet på den domän där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="c7fea-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="c7fea-146">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="c7fea-146">-Endpoint</span></span>
<span data-ttu-id="c7fea-147">Destinations slut punkt för händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c7fea-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="c7fea-148">Detta kan vara en webhook-URL eller Azure-resurs-ID för en EventHub, lagringsprovider, hybridconnection eller servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="c7fea-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="c7fea-149">Resurs-ID för en hybrid anslutning har till exempel följande form:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="c7fea-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="c7fea-150">Det förväntas att mål slut punkten skapas och är tillgänglig för användning innan ett händelse rutnät körs.</span><span class="sxs-lookup"><span data-stu-id="c7fea-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="c7fea-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="c7fea-151">-EndpointType</span></span>
<span data-ttu-id="c7fea-152">Typ av slut punkt.</span><span class="sxs-lookup"><span data-stu-id="c7fea-152">Endpoint Type.</span></span>
<span data-ttu-id="c7fea-153">Det här kan vara webhook, eventhub, storagequeue, hybridconnection eller servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="c7fea-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="c7fea-154">Standardvärdet är webhook.</span><span class="sxs-lookup"><span data-stu-id="c7fea-154">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7fea-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c7fea-155">-EventSubscriptionName</span></span>
<span data-ttu-id="c7fea-156">Namnet på händelse prenumerationen</span><span class="sxs-lookup"><span data-stu-id="c7fea-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="c7fea-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="c7fea-157">-EventTtl</span></span>
<span data-ttu-id="c7fea-158">Tid i minuter för händelse leverans.</span><span class="sxs-lookup"><span data-stu-id="c7fea-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="c7fea-159">Värdet måste vara mellan 1 och 1440</span><span class="sxs-lookup"><span data-stu-id="c7fea-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="c7fea-160">-Förfallo</span><span class="sxs-lookup"><span data-stu-id="c7fea-160">-ExpirationDate</span></span>
<span data-ttu-id="c7fea-161">Avgör förfallo dag/tid för händelse prenumerationen efter vilken händelse prenumerationen dras tillbaka.</span><span class="sxs-lookup"><span data-stu-id="c7fea-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="c7fea-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="c7fea-162">-IncludedEventType</span></span>
<span data-ttu-id="c7fea-163">Filter som anger en lista över händelse typer som ska ingå. Om inget anges tas alla händelse typer med.</span><span class="sxs-lookup"><span data-stu-id="c7fea-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="c7fea-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7fea-164">-InputObject</span></span>
<span data-ttu-id="c7fea-165">EventGridSubscription-objekt.</span><span class="sxs-lookup"><span data-stu-id="c7fea-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="c7fea-166">-Etikett</span><span class="sxs-lookup"><span data-stu-id="c7fea-166">-Label</span></span>
<span data-ttu-id="c7fea-167">Etiketter för händelse abonnemanget</span><span class="sxs-lookup"><span data-stu-id="c7fea-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="c7fea-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="c7fea-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="c7fea-169">Maximalt antal försök att leverera händelsen.</span><span class="sxs-lookup"><span data-stu-id="c7fea-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="c7fea-170">Värdet måste vara mellan 1 och 30</span><span class="sxs-lookup"><span data-stu-id="c7fea-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="c7fea-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="c7fea-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="c7fea-172">Maximalt antal händelser i en grupp.</span><span class="sxs-lookup"><span data-stu-id="c7fea-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="c7fea-173">Värdet måste vara mellan 1 och 5000.</span><span class="sxs-lookup"><span data-stu-id="c7fea-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="c7fea-174">Den här parametern är giltig när Endpint-typen endast är webhook.</span><span class="sxs-lookup"><span data-stu-id="c7fea-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="c7fea-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="c7fea-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="c7fea-176">Önskad batchstorlek i kilobyte.</span><span class="sxs-lookup"><span data-stu-id="c7fea-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="c7fea-177">Värdet måste vara mellan 1 och 1024.</span><span class="sxs-lookup"><span data-stu-id="c7fea-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="c7fea-178">Den här parametern är giltig när Endpint-typen endast är webhook.</span><span class="sxs-lookup"><span data-stu-id="c7fea-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="c7fea-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7fea-179">-ResourceGroupName</span></span>
<span data-ttu-id="c7fea-180">Ämnets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c7fea-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="c7fea-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7fea-181">-ResourceId</span></span>
<span data-ttu-id="c7fea-182">ID för resursen som händelse prenumerationen skapades för.</span><span class="sxs-lookup"><span data-stu-id="c7fea-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="c7fea-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="c7fea-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="c7fea-184">Filter som anger att endast händelser som matchar det angivna prefixet för subjektet kommer att ingå.</span><span class="sxs-lookup"><span data-stu-id="c7fea-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="c7fea-185">Om inget anges inkluderas händelser med alla ämnes prefix.</span><span class="sxs-lookup"><span data-stu-id="c7fea-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="c7fea-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="c7fea-186">-SubjectEndsWith</span></span>
<span data-ttu-id="c7fea-187">Filter som anger att endast händelser som matchar det angivna ämnes tillägget tas med.</span><span class="sxs-lookup"><span data-stu-id="c7fea-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="c7fea-188">Om inget anges inkluderas händelser med alla ämnes suffix.</span><span class="sxs-lookup"><span data-stu-id="c7fea-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="c7fea-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="c7fea-189">-TopicName</span></span>
<span data-ttu-id="c7fea-190">Namnet på ämnet där händelse prenumerationen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="c7fea-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="c7fea-191">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7fea-191">-Confirm</span></span>
<span data-ttu-id="c7fea-192">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7fea-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7fea-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7fea-193">-WhatIf</span></span>
<span data-ttu-id="c7fea-194">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7fea-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7fea-195">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7fea-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7fea-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7fea-196">CommonParameters</span></span>
<span data-ttu-id="c7fea-197">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7fea-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7fea-198">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7fea-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7fea-199">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7fea-199">INPUTS</span></span>

### <span data-ttu-id="c7fea-200">System. String</span><span class="sxs-lookup"><span data-stu-id="c7fea-200">System.String</span></span>

### <span data-ttu-id="c7fea-201">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="c7fea-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="c7fea-202">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7fea-202">OUTPUTS</span></span>

### <span data-ttu-id="c7fea-203">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="c7fea-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="c7fea-204">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7fea-204">NOTES</span></span>

## <span data-ttu-id="c7fea-205">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7fea-205">RELATED LINKS</span></span>
