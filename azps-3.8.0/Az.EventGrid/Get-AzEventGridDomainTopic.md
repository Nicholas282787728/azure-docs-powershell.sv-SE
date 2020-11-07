---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 10ea1dca3ef550bcbd38082a8b27a19dd2ffb46a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926201"
---
# <span data-ttu-id="1b57b-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1b57b-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="1b57b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b57b-102">SYNOPSIS</span></span>
<span data-ttu-id="1b57b-103">Hämtar information om ett ämne i händelse rutnät eller en lista över alla ämnen för händelse rutnät i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1b57b-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="1b57b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b57b-104">SYNTAX</span></span>

### <span data-ttu-id="1b57b-105">DomainTopicNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1b57b-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b57b-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b57b-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b57b-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b57b-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b57b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b57b-108">DESCRIPTION</span></span>
<span data-ttu-id="1b57b-109">Get-AzEventGridDomainTopic-cmdleten får information om ett ämne i avsnittet händelse rutnät eller en lista över alla ämnen under en viss domän i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1b57b-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="1b57b-110">Om domänens avsnitts namn är angivet returneras information om ett avsnitt med en enskild händelse med rutnät.</span><span class="sxs-lookup"><span data-stu-id="1b57b-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="1b57b-111">Om domänens avsnitts namn inte anges returneras en lista med domän ämnen under det angivna domän namnet.</span><span class="sxs-lookup"><span data-stu-id="1b57b-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="1b57b-112">Antalet element som returneras i den här listan styrs av den översta parametern.</span><span class="sxs-lookup"><span data-stu-id="1b57b-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="1b57b-113">Om det översta värdet inte är angivet eller $null innehåller listan alla objekt avsnitt.</span><span class="sxs-lookup"><span data-stu-id="1b57b-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="1b57b-114">Annars visas det maximala antalet element som ska returneras i listan.</span><span class="sxs-lookup"><span data-stu-id="1b57b-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="1b57b-115">Om det fortfarande finns fler avsnitt i domänen ska värdet i NextLink användas i nästa samtal för att hämta nästa sida med domän avsnitt.</span><span class="sxs-lookup"><span data-stu-id="1b57b-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="1b57b-116">Slutligen används ODataQuery-parametern för att filtrera Sök resultatet.</span><span class="sxs-lookup"><span data-stu-id="1b57b-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="1b57b-117">Filtrerings frågan följer OData-syntax med endast namn-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="1b57b-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="1b57b-118">De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="1b57b-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="1b57b-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b57b-119">EXAMPLES</span></span>

### <span data-ttu-id="1b57b-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1b57b-120">Example 1</span></span>

<span data-ttu-id="1b57b-121">Hämtar information om avsnittet händelse rutnät Domain \` DomainTopic1 \` under händelse rutnätets domän- \` domain1 \` i resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="1b57b-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="1b57b-122">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1b57b-122">Example 2</span></span>

<span data-ttu-id="1b57b-123">Hämtar information om avsnittet händelse rutnäts domän \` \` i DomainTopic1 under händelse rutnät Domain \` domain1 \` i resurs grupps \` MyResourceGroupName \` med alternativet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="1b57b-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="1b57b-124">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="1b57b-124">Example 3</span></span>

<span data-ttu-id="1b57b-125">Lista alla ämnen för händelse rutnät i domän \` domain1 \` i resurs gruppen \` MyResourceGroupName \` utan sid brytning (alla resultat returneras i en bild).</span><span class="sxs-lookup"><span data-stu-id="1b57b-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="1b57b-126">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="1b57b-126">Example 4</span></span>

<span data-ttu-id="1b57b-127">Lista alla ämnen för händelse rutnät i domänen \` domain1 \` i resurs gruppen \` MyResourceGroupName \` utan sid brytning (alla resultat returneras samtidigt) med alternativet ResourceID</span><span class="sxs-lookup"><span data-stu-id="1b57b-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="1b57b-128">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="1b57b-128">Example 5</span></span>

<span data-ttu-id="1b57b-129">Lista med ämnen för händelse rutnät i domänen (om det finns några) under domän \` domain1 \` i resurs grupp \` MyResourceGroupName \` som uppfyller de $odataFilter de olika ämnena för domän i taget.</span><span class="sxs-lookup"><span data-stu-id="1b57b-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="1b57b-130">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="1b57b-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="1b57b-131">För att få nästa sida (er) av domän ämnen förväntas användaren att ringa in Get-AzEventGridDomainTopic och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="1b57b-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="1b57b-132">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="1b57b-132">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## <span data-ttu-id="1b57b-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b57b-133">PARAMETERS</span></span>

### <span data-ttu-id="1b57b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b57b-134">-DefaultProfile</span></span>
<span data-ttu-id="1b57b-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b57b-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b57b-136">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="1b57b-136">-DomainName</span></span>
<span data-ttu-id="1b57b-137">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="1b57b-137">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b57b-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b57b-138">-Name</span></span>
<span data-ttu-id="1b57b-139">Namn på EventGrid-domän.</span><span class="sxs-lookup"><span data-stu-id="1b57b-139">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b57b-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="1b57b-140">-NextLink</span></span>
<span data-ttu-id="1b57b-141">Länken för nästa sida med resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1b57b-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="1b57b-142">Det här värdet hämtas med det första Get-AzEventGrid cmdlet-anropet när det fortfarande finns fler resurser att fråga efter.</span><span class="sxs-lookup"><span data-stu-id="1b57b-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b57b-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="1b57b-143">-ODataQuery</span></span>
<span data-ttu-id="1b57b-144">OData-frågan som används för att filtrera listans resultat.</span><span class="sxs-lookup"><span data-stu-id="1b57b-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="1b57b-145">Filtrering stöds för närvarande endast i namn-egenskapen. De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="1b57b-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b57b-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b57b-146">-ResourceGroupName</span></span>
<span data-ttu-id="1b57b-147">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1b57b-147">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b57b-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b57b-148">-ResourceId</span></span>
<span data-ttu-id="1b57b-149">Resurs-ID som representerar domän-eller rutnäts domän ämnets avsnitt.</span><span class="sxs-lookup"><span data-stu-id="1b57b-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b57b-150">-Överst</span><span class="sxs-lookup"><span data-stu-id="1b57b-150">-Top</span></span>
<span data-ttu-id="1b57b-151">OData-frågan som används för att filtrera listans resultat.</span><span class="sxs-lookup"><span data-stu-id="1b57b-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="1b57b-152">Filtrering stöds för närvarande endast i namn-egenskapen. De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="1b57b-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b57b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b57b-153">CommonParameters</span></span>
<span data-ttu-id="1b57b-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b57b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b57b-155">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b57b-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b57b-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b57b-156">INPUTS</span></span>

### <span data-ttu-id="1b57b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="1b57b-157">System.String</span></span>

### <span data-ttu-id="1b57b-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1b57b-158">System.Int32</span></span>

## <span data-ttu-id="1b57b-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b57b-159">OUTPUTS</span></span>

### <span data-ttu-id="1b57b-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1b57b-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="1b57b-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="1b57b-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="1b57b-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b57b-162">NOTES</span></span>

## <span data-ttu-id="1b57b-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b57b-163">RELATED LINKS</span></span>
