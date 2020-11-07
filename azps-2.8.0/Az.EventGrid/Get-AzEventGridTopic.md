---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 2bae39bb6a3e0c08a86118ce9ed8f9c6fadf82c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744259"
---
# <span data-ttu-id="fef4e-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="fef4e-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="fef4e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fef4e-102">SYNOPSIS</span></span>
<span data-ttu-id="fef4e-103">Hämtar information om ett ämne i händelse rutnätet eller hämtar en lista över alla händelse rutnät i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fef4e-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="fef4e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fef4e-104">SYNTAX</span></span>

### <span data-ttu-id="fef4e-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fef4e-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef4e-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fef4e-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef4e-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fef4e-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef4e-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="fef4e-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fef4e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fef4e-109">DESCRIPTION</span></span>
<span data-ttu-id="fef4e-110">Get-AzEventGridTopic-cmdleten får information om ett visst ämne i händelse rutnät, eller en lista över alla händelse rutnät i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fef4e-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="fef4e-111">Om ämnets namn är angivet returneras informationen om ett avsnitt med en enskild händelse.</span><span class="sxs-lookup"><span data-stu-id="fef4e-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="fef4e-112">Om ämnets namn inte anges returneras en lista med avsnitt.</span><span class="sxs-lookup"><span data-stu-id="fef4e-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="fef4e-113">Antalet element som returneras i den här listan styrs av den översta parametern.</span><span class="sxs-lookup"><span data-stu-id="fef4e-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="fef4e-114">Om det översta värdet inte är angivet eller $null, innehåller listan alla ämnen.</span><span class="sxs-lookup"><span data-stu-id="fef4e-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="fef4e-115">Annars visas det maximala antalet element som ska returneras i listan.</span><span class="sxs-lookup"><span data-stu-id="fef4e-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="fef4e-116">Om det fortfarande finns fler ämnen kan värdet i NextLink användas i nästa samtal för att hämta nästa sida med avsnitt.</span><span class="sxs-lookup"><span data-stu-id="fef4e-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="fef4e-117">Slutligen används ODataQuery-parametern för att filtrera Sök resultatet.</span><span class="sxs-lookup"><span data-stu-id="fef4e-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="fef4e-118">Filtrerings frågan följer OData-syntax med endast namn-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="fef4e-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="fef4e-119">De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="fef4e-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="fef4e-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fef4e-120">EXAMPLES</span></span>

### <span data-ttu-id="fef4e-121">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fef4e-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="fef4e-122">Hämtar information om ämnet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="fef4e-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="fef4e-123">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fef4e-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="fef4e-124">Hämtar information om ämnet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="fef4e-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="fef4e-125">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="fef4e-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="fef4e-126">Visa en lista över alla rutnät i \` MyResourceGroupName \` utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="fef4e-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="fef4e-127">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="fef4e-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="fef4e-128">Visa en lista över de första tio händelse rutnäten i resurs grupps \` MyResourceGroupName \` som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="fef4e-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="fef4e-129">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="fef4e-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="fef4e-130">För att få nästa sida med ämnen förväntas användaren att ringa in Get-AzEventGridTopic och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="fef4e-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="fef4e-131">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="fef4e-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="fef4e-132">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="fef4e-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="fef4e-133">Visa en lista med alla händelse rutnät i prenumerationen utan sid brytning.</span><span class="sxs-lookup"><span data-stu-id="fef4e-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="fef4e-134">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="fef4e-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="fef4e-135">Visa en lista med de första 10 händelse rutnäten (om de finns) i prenumerationen som uppfyller $odataFilter-frågan.</span><span class="sxs-lookup"><span data-stu-id="fef4e-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="fef4e-136">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="fef4e-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="fef4e-137">För att få nästa sida med ämnen förväntas användaren att ringa in Get-AzEventGridTopic och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="fef4e-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="fef4e-138">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="fef4e-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="fef4e-139">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fef4e-139">PARAMETERS</span></span>

### <span data-ttu-id="fef4e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef4e-140">-DefaultProfile</span></span>
<span data-ttu-id="fef4e-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fef4e-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fef4e-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="fef4e-142">-Name</span></span>
<span data-ttu-id="fef4e-143">Namn på EventGrid-avsnitt.</span><span class="sxs-lookup"><span data-stu-id="fef4e-143">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef4e-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="fef4e-144">-NextLink</span></span>
<span data-ttu-id="fef4e-145">Länken för nästa sida med resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="fef4e-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="fef4e-146">Det här värdet hämtas med det första Get-AzEventGrid cmdlet-anropet när det fortfarande finns fler resurser att fråga efter.</span><span class="sxs-lookup"><span data-stu-id="fef4e-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="fef4e-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="fef4e-147">-ODataQuery</span></span>
<span data-ttu-id="fef4e-148">OData-frågan som används för att filtrera listans resultat.</span><span class="sxs-lookup"><span data-stu-id="fef4e-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="fef4e-149">Filtrering stöds för närvarande endast i namn-egenskapen. De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="fef4e-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef4e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fef4e-150">-ResourceGroupName</span></span>
<span data-ttu-id="fef4e-151">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fef4e-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef4e-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fef4e-152">-ResourceId</span></span>
<span data-ttu-id="fef4e-153">Resurs-ID som representerar avsnittet händelse rutnät.</span><span class="sxs-lookup"><span data-stu-id="fef4e-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="fef4e-154">-Överst</span><span class="sxs-lookup"><span data-stu-id="fef4e-154">-Top</span></span>
<span data-ttu-id="fef4e-155">Maximalt antal resurser som kan erhållas.</span><span class="sxs-lookup"><span data-stu-id="fef4e-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="fef4e-156">Giltigt värde är mellan 1 och 100.</span><span class="sxs-lookup"><span data-stu-id="fef4e-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="fef4e-157">Om högsta värde anges och fler resultat fortfarande är tillgängliga innehåller resultatet en länk till nästa sida som ska frågas i NextLink.</span><span class="sxs-lookup"><span data-stu-id="fef4e-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="fef4e-158">Om det högsta värdet inte anges returneras hela listan med resurser samtidigt.</span><span class="sxs-lookup"><span data-stu-id="fef4e-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef4e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef4e-159">CommonParameters</span></span>
<span data-ttu-id="fef4e-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fef4e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef4e-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef4e-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef4e-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fef4e-162">INPUTS</span></span>

### <span data-ttu-id="fef4e-163">System. String</span><span class="sxs-lookup"><span data-stu-id="fef4e-163">System.String</span></span>

### <span data-ttu-id="fef4e-164">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fef4e-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fef4e-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fef4e-165">OUTPUTS</span></span>

### <span data-ttu-id="fef4e-166">Microsoft. Azure. commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="fef4e-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="fef4e-167">Microsoft. Azure. commands. EventGrid. Models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="fef4e-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="fef4e-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fef4e-168">NOTES</span></span>

## <span data-ttu-id="fef4e-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fef4e-169">RELATED LINKS</span></span>
