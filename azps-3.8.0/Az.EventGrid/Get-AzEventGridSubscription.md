---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 5adc6e203166903b0c76d906ce03cd72cb73c3d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926666"
---
# <span data-ttu-id="a90f3-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a90f3-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="a90f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a90f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a90f3-103">Hämtar information om en händelse prenumeration eller hämtar en lista över alla händelse prenumerationer i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a90f3-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="a90f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a90f3-104">SYNTAX</span></span>

### <span data-ttu-id="a90f3-105">EventSubscriptionTopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a90f3-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a90f3-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a90f3-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a90f3-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a90f3-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a90f3-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a90f3-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a90f3-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a90f3-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a90f3-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a90f3-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a90f3-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a90f3-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a90f3-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="a90f3-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a90f3-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a90f3-113">DESCRIPTION</span></span>
<span data-ttu-id="a90f3-114">Get-AzEventGridSubscription-cmdleten får antingen information om ett angivet abonnemang för händelse rutnät eller en lista över alla prenumerationer i det aktuella Azure-abonnemanget eller resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a90f3-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="a90f3-115">Om händelse prenumerationens namn anges returneras informationen om ett enskilt rutnäts abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a90f3-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="a90f3-116">Om händelse prenumerationens namn inte anges returneras en lista över alla händelse prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="a90f3-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="a90f3-117">Antalet element som returneras i den här listan styrs av den översta parametern.</span><span class="sxs-lookup"><span data-stu-id="a90f3-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="a90f3-118">Om det översta värdet inte är angivet eller $null innehåller listan Alla händelse prenumerations objekt.</span><span class="sxs-lookup"><span data-stu-id="a90f3-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="a90f3-119">Annars visas det maximala antalet element som ska returneras i listan.</span><span class="sxs-lookup"><span data-stu-id="a90f3-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="a90f3-120">Om fler händelse abonnemang fortfarande är tillgängliga ska värdet i NextLink användas i nästa samtal för att hämta nästa sida med händelse prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="a90f3-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="a90f3-121">Slutligen används ODataQuery-parametern för att filtrera Sök resultatet.</span><span class="sxs-lookup"><span data-stu-id="a90f3-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="a90f3-122">Filtrerings frågan följer OData-syntax med endast namn-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="a90f3-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="a90f3-123">De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="a90f3-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="a90f3-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a90f3-124">EXAMPLES</span></span>

### <span data-ttu-id="a90f3-125">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a90f3-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a90f3-126">Hämtar information om händelse abonnemangs \` EventSubscription1 \` som har skapats för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a90f3-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a90f3-127">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a90f3-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="a90f3-128">Hämtar information om händelse abonnemangs \` EventSubscription1 \` som har skapats för ämne \` Ämne1 \` i resurs grupps \` MyResourceGroupName \` , inklusive fullständig slut punkts-URL om det är en webhook-baserad händelse prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a90f3-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="a90f3-129">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a90f3-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="a90f3-130">Få en lista över alla händelse prenumerationer som har skapats för ämnet \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="a90f3-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="a90f3-131">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="a90f3-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a90f3-132">Lista de första 10 händelse prenumerationerna (om sådana finns) som har skapats för ämnet \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="a90f3-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a90f3-133">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a90f3-134">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="a90f3-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a90f3-135">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a90f3-136">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="a90f3-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a90f3-137">Hämtar information om händelse prenumerations \` EventSubscription1 \` som har skapats för resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a90f3-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a90f3-138">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="a90f3-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a90f3-139">Hämtar information om \` EventSubscription1 som \` skapats för den valda Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a90f3-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="a90f3-140">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="a90f3-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a90f3-141">Hämtar listan över alla globala händelse prenumerationer som skapas under resurs gruppen \` MyResourceGroupName \` utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="a90f3-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="a90f3-142">Exempel 8</span><span class="sxs-lookup"><span data-stu-id="a90f3-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a90f3-143">Visa en lista med de första 5 händelse prenumerationerna (om sådana finns) $odataFilter som har skapats under \` MyResourceGroupName- \` frågan.</span><span class="sxs-lookup"><span data-stu-id="a90f3-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a90f3-144">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a90f3-145">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="a90f3-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a90f3-146">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a90f3-147">Exempel 9</span><span class="sxs-lookup"><span data-stu-id="a90f3-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="a90f3-148">Hämtar listan över alla globala händelse prenumerationer som har skapats under den valda Azure-prenumerationen utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="a90f3-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="a90f3-149">Exempel 10</span><span class="sxs-lookup"><span data-stu-id="a90f3-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a90f3-150">Lista de första 15 globala händelse prenumerationerna (om sådana finns) som skapats under det markerade Azure-abonnemanget som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="a90f3-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a90f3-151">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a90f3-152">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="a90f3-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a90f3-153">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a90f3-154">Exempel 11</span><span class="sxs-lookup"><span data-stu-id="a90f3-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="a90f3-155">Hämtar listan över alla regionala händelse prenumerationer som har skapats under \` MyResourceGroupName \` på den angivna platsen \` westus2 \` utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="a90f3-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="a90f3-156">Exempel 12</span><span class="sxs-lookup"><span data-stu-id="a90f3-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a90f3-157">Lista de första 15 regionala händelse prenumerationerna (om sådana finns) som skapats under resurs grupp \` MyResourceGroupName \` på den angivna plats \` westus2 \` som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="a90f3-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a90f3-158">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a90f3-159">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="a90f3-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a90f3-160">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a90f3-161">Exempel 13</span><span class="sxs-lookup"><span data-stu-id="a90f3-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="a90f3-162">Hämtar listan över alla händelse prenumerationer som har skapats för det angivna EventHub-namnområdet utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="a90f3-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="a90f3-163">Exempel 14</span><span class="sxs-lookup"><span data-stu-id="a90f3-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a90f3-164">Lista de första 25 händelse prenumerationerna (om sådana finns) som skapats för det angivna EventHub-namn som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="a90f3-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a90f3-165">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a90f3-166">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="a90f3-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a90f3-167">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a90f3-168">Exempel 15</span><span class="sxs-lookup"><span data-stu-id="a90f3-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="a90f3-169">Hämtar listan över alla händelse prenumerationer som har skapats för den angivna ämnes typen (EventHub-namnområden) på den angivna platsen utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="a90f3-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="a90f3-170">Exempel 16</span><span class="sxs-lookup"><span data-stu-id="a90f3-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a90f3-171">Lista de första 15 händelse prenumerationerna (om sådana finns) som skapats för den angivna ämnes typen (EventHub-namnområden) på den angivna platsen som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="a90f3-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a90f3-172">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a90f3-173">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="a90f3-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a90f3-174">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="a90f3-175">Exempel 17</span><span class="sxs-lookup"><span data-stu-id="a90f3-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a90f3-176">Hämtar listan över alla händelse prenumerationer som har skapats för den specifika resurs gruppen utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="a90f3-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="a90f3-177">Exempel 18</span><span class="sxs-lookup"><span data-stu-id="a90f3-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="a90f3-178">Lista de första 100 händelse prenumerationerna (om sådana finns) som skapats för den specifika resurs gruppen som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="a90f3-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="a90f3-179">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="a90f3-180">För att få nästa sida (er) av händelse prenumerationer, förväntas användaren att ringa in Get-AzEventGridSubscription och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="a90f3-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="a90f3-181">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="a90f3-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="a90f3-182">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a90f3-182">PARAMETERS</span></span>

### <span data-ttu-id="a90f3-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a90f3-183">-DefaultProfile</span></span>
<span data-ttu-id="a90f3-184">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a90f3-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a90f3-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="a90f3-185">-DomainInputObject</span></span>
<span data-ttu-id="a90f3-186">EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a90f3-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="a90f3-187">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="a90f3-187">-DomainName</span></span>
<span data-ttu-id="a90f3-188">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="a90f3-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="a90f3-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="a90f3-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="a90f3-190">EventGrid Domain-objekt.</span><span class="sxs-lookup"><span data-stu-id="a90f3-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="a90f3-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="a90f3-191">-DomainTopicName</span></span>
<span data-ttu-id="a90f3-192">Namn på EventGrid-domän.</span><span class="sxs-lookup"><span data-stu-id="a90f3-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="a90f3-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a90f3-193">-EventSubscriptionName</span></span>
<span data-ttu-id="a90f3-194">Namnet på händelse prenumerationen</span><span class="sxs-lookup"><span data-stu-id="a90f3-194">The name of the event subscription</span></span>

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

### <span data-ttu-id="a90f3-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="a90f3-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="a90f3-196">Ange fullständig slut punkts-URL för händelse prenumerationens destination.</span><span class="sxs-lookup"><span data-stu-id="a90f3-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="a90f3-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a90f3-197">-InputObject</span></span>
<span data-ttu-id="a90f3-198">EventGrid ämne.</span><span class="sxs-lookup"><span data-stu-id="a90f3-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a90f3-199">-Plats</span><span class="sxs-lookup"><span data-stu-id="a90f3-199">-Location</span></span>
<span data-ttu-id="a90f3-200">Plats</span><span class="sxs-lookup"><span data-stu-id="a90f3-200">Location</span></span>

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

### <span data-ttu-id="a90f3-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="a90f3-201">-NextLink</span></span>
<span data-ttu-id="a90f3-202">Länken för nästa sida med resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="a90f3-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="a90f3-203">Det här värdet hämtas med det första Get-AzEventGrid cmdlet-anropet när det fortfarande finns fler resurser att fråga efter.</span><span class="sxs-lookup"><span data-stu-id="a90f3-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="a90f3-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a90f3-204">-ODataQuery</span></span>
<span data-ttu-id="a90f3-205">OData-frågan som används för att filtrera listans resultat.</span><span class="sxs-lookup"><span data-stu-id="a90f3-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="a90f3-206">Filtrering stöds för närvarande endast i namn-egenskapen. De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="a90f3-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="a90f3-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a90f3-207">-ResourceGroupName</span></span>
<span data-ttu-id="a90f3-208">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a90f3-208">Resource Group Name.</span></span>

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

### <span data-ttu-id="a90f3-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a90f3-209">-ResourceId</span></span>
<span data-ttu-id="a90f3-210">Identifierare för den resurs som händelse prenumerationer har skapats för.</span><span class="sxs-lookup"><span data-stu-id="a90f3-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="a90f3-211">-Överst</span><span class="sxs-lookup"><span data-stu-id="a90f3-211">-Top</span></span>
<span data-ttu-id="a90f3-212">OData-frågan som används för att filtrera listans resultat.</span><span class="sxs-lookup"><span data-stu-id="a90f3-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="a90f3-213">Filtrering stöds för närvarande endast i namn-egenskapen. De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="a90f3-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="a90f3-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a90f3-214">-TopicName</span></span>
<span data-ttu-id="a90f3-215">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="a90f3-215">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="a90f3-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="a90f3-216">-TopicTypeName</span></span>
<span data-ttu-id="a90f3-217">TopicType namn</span><span class="sxs-lookup"><span data-stu-id="a90f3-217">TopicType name</span></span>

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

### <span data-ttu-id="a90f3-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a90f3-218">CommonParameters</span></span>
<span data-ttu-id="a90f3-219">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a90f3-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a90f3-220">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a90f3-220">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a90f3-221">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a90f3-221">INPUTS</span></span>

### <span data-ttu-id="a90f3-222">System. String</span><span class="sxs-lookup"><span data-stu-id="a90f3-222">System.String</span></span>

### <span data-ttu-id="a90f3-223">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a90f3-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="a90f3-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="a90f3-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="a90f3-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a90f3-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="a90f3-226">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a90f3-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a90f3-227">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a90f3-227">OUTPUTS</span></span>

### <span data-ttu-id="a90f3-228">Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="a90f3-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a90f3-229">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a90f3-229">NOTES</span></span>

## <span data-ttu-id="a90f3-230">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a90f3-230">RELATED LINKS</span></span>