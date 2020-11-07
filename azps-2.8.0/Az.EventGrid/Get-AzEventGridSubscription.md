---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 987882928ee215ed2da842e924386f5dec8b862f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744262"
---
# <span data-ttu-id="51800-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="51800-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="51800-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51800-102">SYNOPSIS</span></span>
<span data-ttu-id="51800-103">Hämtar information om en händelse prenumeration eller hämtar en lista över alla händelse prenumerationer i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="51800-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="51800-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51800-104">SYNTAX</span></span>

### <span data-ttu-id="51800-105">EventSubscriptionTopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51800-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51800-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="51800-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51800-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51800-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51800-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51800-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51800-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51800-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51800-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51800-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51800-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51800-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51800-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="51800-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51800-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51800-113">DESCRIPTION</span></span>
<span data-ttu-id="51800-114">Get-AzEventGridSubscription-cmdleten får antingen information om ett angivet abonnemang för händelse rutnät eller en lista över alla prenumerationer i det aktuella Azure-abonnemanget eller resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51800-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="51800-115">Om händelse prenumerationens namn anges returneras informationen om ett enskilt rutnäts abonnemang.</span><span class="sxs-lookup"><span data-stu-id="51800-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="51800-116">Om händelse prenumerationens namn inte anges returneras en lista över alla händelse prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="51800-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="51800-117">Antalet element som returneras i den här listan styrs av den översta parametern.</span><span class="sxs-lookup"><span data-stu-id="51800-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="51800-118">Om det översta värdet inte är angivet eller $null innehåller listan Alla händelse prenumerations objekt.</span><span class="sxs-lookup"><span data-stu-id="51800-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="51800-119">Annars visas det maximala antalet element som ska returneras i listan.</span><span class="sxs-lookup"><span data-stu-id="51800-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="51800-120">Om fler händelse abonnemang fortfarande är tillgängliga ska värdet i NextLink användas i nästa samtal för att hämta nästa sida med händelse prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="51800-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="51800-121">Slutligen används ODataQuery-parametern för att filtrera Sök resultatet.</span><span class="sxs-lookup"><span data-stu-id="51800-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="51800-122">Filtrerings frågan följer OData-syntax med endast namn-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="51800-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="51800-123">De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="51800-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="51800-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51800-124">EXAMPLES</span></span>

### <span data-ttu-id="51800-125">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51800-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="51800-126">Hämtar information om händelse abonnemangs \` EventSubscription1 \` som har skapats för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="51800-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="51800-127">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="51800-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="51800-128">Hämtar information om händelse abonnemangs \` EventSubscription1 \` som har skapats för ämne \` Ämne1 \` i resurs grupps \` MyResourceGroupName \` , inklusive fullständig slut punkts-URL om det är en webhook-baserad händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="51800-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="51800-129">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="51800-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="51800-130">Få en lista över alla händelse prenumerationer som har skapats för ämnet \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="51800-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="51800-131">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="51800-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="51800-132">Lista de första 10 händelse prenumerationerna (om sådana finns) som har skapats för ämnet \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="51800-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="51800-133">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="51800-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="51800-134">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="51800-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="51800-135">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="51800-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="51800-136">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="51800-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="51800-137">Hämtar information om händelse prenumerations \` EventSubscription1 \` som har skapats för resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="51800-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="51800-138">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="51800-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="51800-139">Hämtar information om \` EventSubscription1 som \` skapats för den valda Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="51800-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="51800-140">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="51800-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="51800-141">Hämtar listan över alla globala händelse prenumerationer som skapas under resurs gruppen \` MyResourceGroupName \` utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="51800-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="51800-142">Exempel 8</span><span class="sxs-lookup"><span data-stu-id="51800-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="51800-143">Visa en lista med de första 5 händelse prenumerationerna (om sådana finns) $odataFilter som har skapats under \` MyResourceGroupName- \` frågan.</span><span class="sxs-lookup"><span data-stu-id="51800-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="51800-144">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="51800-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="51800-145">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="51800-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="51800-146">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="51800-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="51800-147">Exempel 9</span><span class="sxs-lookup"><span data-stu-id="51800-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="51800-148">Hämtar listan över alla globala händelse prenumerationer som har skapats under den valda Azure-prenumerationen utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="51800-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="51800-149">Exempel 10</span><span class="sxs-lookup"><span data-stu-id="51800-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="51800-150">Lista de första 15 globala händelse prenumerationerna (om sådana finns) som skapats under det markerade Azure-abonnemanget som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="51800-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="51800-151">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="51800-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="51800-152">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="51800-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="51800-153">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="51800-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="51800-154">Exempel 11</span><span class="sxs-lookup"><span data-stu-id="51800-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="51800-155">Hämtar listan över alla regionala händelse prenumerationer som har skapats under \` MyResourceGroupName \` på den angivna platsen \` westus2 \` utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="51800-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="51800-156">Exempel 12</span><span class="sxs-lookup"><span data-stu-id="51800-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="51800-157">Lista de första 15 regionala händelse prenumerationerna (om sådana finns) som skapats under resurs grupp \` MyResourceGroupName \` på den angivna plats \` westus2 \` som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="51800-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="51800-158">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="51800-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="51800-159">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="51800-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="51800-160">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="51800-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="51800-161">Exempel 13</span><span class="sxs-lookup"><span data-stu-id="51800-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="51800-162">Hämtar listan över alla händelse prenumerationer som har skapats för det angivna EventHub-namnområdet utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="51800-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="51800-163">Exempel 14</span><span class="sxs-lookup"><span data-stu-id="51800-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="51800-164">Lista de första 25 händelse prenumerationerna (om sådana finns) som skapats för det angivna EventHub-namn som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="51800-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="51800-165">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="51800-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="51800-166">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="51800-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="51800-167">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="51800-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="51800-168">Exempel 15</span><span class="sxs-lookup"><span data-stu-id="51800-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="51800-169">Hämtar listan över alla händelse prenumerationer som har skapats för den angivna ämnes typen (EventHub-namnområden) på den angivna platsen utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="51800-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="51800-170">Exempel 16</span><span class="sxs-lookup"><span data-stu-id="51800-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="51800-171">Lista de första 15 händelse prenumerationerna (om sådana finns) som skapats för den angivna ämnes typen (EventHub-namnområden) på den angivna platsen som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="51800-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="51800-172">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="51800-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="51800-173">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="51800-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="51800-174">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="51800-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="51800-175">Exempel 17</span><span class="sxs-lookup"><span data-stu-id="51800-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="51800-176">Hämtar listan över alla händelse prenumerationer som har skapats för den specifika resurs gruppen utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="51800-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="51800-177">Exempel 18</span><span class="sxs-lookup"><span data-stu-id="51800-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="51800-178">Lista de första 100 händelse prenumerationerna (om sådana finns) som skapats för den specifika resurs gruppen som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="51800-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="51800-179">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="51800-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="51800-180">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="51800-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="51800-181">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="51800-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="51800-182">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51800-182">PARAMETERS</span></span>

### <span data-ttu-id="51800-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51800-183">-DefaultProfile</span></span>
<span data-ttu-id="51800-184">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="51800-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51800-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="51800-185">-DomainInputObject</span></span>
<span data-ttu-id="51800-186">EventGrid.</span><span class="sxs-lookup"><span data-stu-id="51800-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="51800-187">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="51800-187">-DomainName</span></span>
<span data-ttu-id="51800-188">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="51800-188">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51800-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="51800-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="51800-190">EventGrid Domain-objekt.</span><span class="sxs-lookup"><span data-stu-id="51800-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="51800-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="51800-191">-DomainTopicName</span></span>
<span data-ttu-id="51800-192">Namn på EventGrid-domän.</span><span class="sxs-lookup"><span data-stu-id="51800-192">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51800-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="51800-193">-EventSubscriptionName</span></span>
<span data-ttu-id="51800-194">Namnet på händelse prenumerationen</span><span class="sxs-lookup"><span data-stu-id="51800-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51800-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="51800-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="51800-196">Ange fullständig slut punkts-URL för händelse prenumerationens destination.</span><span class="sxs-lookup"><span data-stu-id="51800-196">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51800-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51800-197">-InputObject</span></span>
<span data-ttu-id="51800-198">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="51800-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="51800-199">-Plats</span><span class="sxs-lookup"><span data-stu-id="51800-199">-Location</span></span>
<span data-ttu-id="51800-200">Plats</span><span class="sxs-lookup"><span data-stu-id="51800-200">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51800-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="51800-201">-NextLink</span></span>
<span data-ttu-id="51800-202">Länken för nästa sida med resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="51800-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="51800-203">Det här värdet hämtas med det första Get-AzEventGrid cmdlet-anropet när det fortfarande finns fler resurser att fråga efter.</span><span class="sxs-lookup"><span data-stu-id="51800-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51800-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="51800-204">-ODataQuery</span></span>
<span data-ttu-id="51800-205">OData-frågan som används för att filtrera listans resultat.</span><span class="sxs-lookup"><span data-stu-id="51800-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="51800-206">Filtrering stöds för närvarande endast i namn-egenskapen. De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="51800-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51800-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51800-207">-ResourceGroupName</span></span>
<span data-ttu-id="51800-208">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="51800-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51800-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51800-209">-ResourceId</span></span>
<span data-ttu-id="51800-210">Identifierare för den resurs som händelse prenumerationer har skapats för.</span><span class="sxs-lookup"><span data-stu-id="51800-210">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51800-211">-Överst</span><span class="sxs-lookup"><span data-stu-id="51800-211">-Top</span></span>
<span data-ttu-id="51800-212">OData-frågan som används för att filtrera listans resultat.</span><span class="sxs-lookup"><span data-stu-id="51800-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="51800-213">Filtrering stöds för närvarande endast i namn-egenskapen. De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="51800-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51800-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="51800-214">-TopicName</span></span>
<span data-ttu-id="51800-215">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="51800-215">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51800-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="51800-216">-TopicTypeName</span></span>
<span data-ttu-id="51800-217">TopicType namn</span><span class="sxs-lookup"><span data-stu-id="51800-217">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51800-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51800-218">CommonParameters</span></span>
<span data-ttu-id="51800-219">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51800-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51800-220">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51800-220">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51800-221">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51800-221">INPUTS</span></span>

### <span data-ttu-id="51800-222">System. String</span><span class="sxs-lookup"><span data-stu-id="51800-222">System.String</span></span>

### <span data-ttu-id="51800-223">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="51800-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="51800-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="51800-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="51800-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="51800-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="51800-226">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="51800-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="51800-227">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51800-227">OUTPUTS</span></span>

### <span data-ttu-id="51800-228">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="51800-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="51800-229">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51800-229">NOTES</span></span>

## <span data-ttu-id="51800-230">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51800-230">RELATED LINKS</span></span>
