---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 467b7141735cdce31bbdcf964e058f892238ec1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263205"
---
# <span data-ttu-id="ce737-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ce737-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="ce737-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce737-102">SYNOPSIS</span></span>
<span data-ttu-id="ce737-103">Hämtar information om en händelse i en rutnäts domän eller hämtar en lista över alla domäner i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ce737-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="ce737-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce737-104">SYNTAX</span></span>

### <span data-ttu-id="ce737-105">ResourceGroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ce737-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce737-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce737-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce737-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce737-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce737-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce737-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce737-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce737-109">DESCRIPTION</span></span>
<span data-ttu-id="ce737-110">Get-AzEventGridDomain-cmdleten får antingen information om en angiven domän för händelse rutnät eller en lista över alla domäner i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ce737-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="ce737-111">Om domän namnet är angivet returneras informationen om en enkel rutnäts domän.</span><span class="sxs-lookup"><span data-stu-id="ce737-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="ce737-112">Om domän namnet inte anges returneras en lista över domäner.</span><span class="sxs-lookup"><span data-stu-id="ce737-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="ce737-113">Antalet element som returneras i den här listan styrs av den översta parametern.</span><span class="sxs-lookup"><span data-stu-id="ce737-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="ce737-114">Om det översta värdet inte är angivet eller $null innehåller listan alla domän objekt som returneras samtidigt.</span><span class="sxs-lookup"><span data-stu-id="ce737-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="ce737-115">Annars visas det maximala antalet element som ska returneras i listan.</span><span class="sxs-lookup"><span data-stu-id="ce737-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="ce737-116">Om fler domäner fortfarande är tillgängliga ska värdet i NextLink användas i nästa samtal för att hämta nästa sida med domäner.</span><span class="sxs-lookup"><span data-stu-id="ce737-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="ce737-117">Slutligen används ODataQuery-parametern för att filtrera Sök resultatet.</span><span class="sxs-lookup"><span data-stu-id="ce737-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="ce737-118">Filtrerings frågan följer OData-syntax med endast namn-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="ce737-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="ce737-119">De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="ce737-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="ce737-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce737-120">EXAMPLES</span></span>

### <span data-ttu-id="ce737-121">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ce737-121">Example 1</span></span>

<span data-ttu-id="ce737-122">Hämtar information om domain1 för händelse rutnät \` \` i resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ce737-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="ce737-123">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ce737-123">Example 2</span></span>

<span data-ttu-id="ce737-124">Hämtar information om \` domain1 \` i resurs gruppen \` MyResourceGroupName \` med alternativet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="ce737-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="ce737-125">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ce737-125">Example 3</span></span>

<span data-ttu-id="ce737-126">Visa en lista över alla MyResourceGroupName-domäner i resurs gruppen \` \` utan sid brytning (alla domäner returneras i en bild)</span><span class="sxs-lookup"><span data-stu-id="ce737-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain -ResourceGroup MyResourceGroupName
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="ce737-127">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="ce737-127">Example 4</span></span>

<span data-ttu-id="ce737-128">Visa en lista över de olika händelse rutnäts domänerna (om de finns) i resurs gruppens \` MyResourceGroupName \` som uppfyller $odataFilter fråga 10-domäner åt gången.</span><span class="sxs-lookup"><span data-stu-id="ce737-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="ce737-129">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="ce737-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ce737-130">För att få till gång till följande sidor med domäner förväntas användaren att ringa upp Get-AzEventGridDomain och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="ce737-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ce737-131">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="ce737-131">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domains is $Total"
```

### <span data-ttu-id="ce737-132">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="ce737-132">Example 5</span></span>

<span data-ttu-id="ce737-133">Lista alla domän rutnäts domäner i Azure-prenumerationen utan sid brytning (alla domäner returneras i en bild)</span><span class="sxs-lookup"><span data-stu-id="ce737-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname2/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname3/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="ce737-134">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="ce737-134">Example 6</span></span>

<span data-ttu-id="ce737-135">Lista de domäner i händelse rutnät (om de finns) i Azure-prenumerationen som uppfyller $odataFilter frågaens 20 domäner åt gången.</span><span class="sxs-lookup"><span data-stu-id="ce737-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="ce737-136">Om det finns fler resultat kan $result. NextLink kommer inte att $null.</span><span class="sxs-lookup"><span data-stu-id="ce737-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ce737-137">För att få till gång till följande sidor med domäner förväntas användaren att ringa upp Get-AzEventGridDomain och använder resultat. NextLink hämtat från det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="ce737-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ce737-138">Anroparen bör sluta när resultatet är. NextLink blir $null.</span><span class="sxs-lookup"><span data-stu-id="ce737-138">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Contains(Name, 'ABCD')"
PS C:\> $result = Get-AzEventGridDomain -Top 20 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }
PS C:\> echo "Total number of domains is $Total"
```

## <span data-ttu-id="ce737-139">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce737-139">PARAMETERS</span></span>

### <span data-ttu-id="ce737-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce737-140">-DefaultProfile</span></span>
<span data-ttu-id="ce737-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce737-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce737-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce737-142">-Name</span></span>
<span data-ttu-id="ce737-143">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="ce737-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce737-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="ce737-144">-NextLink</span></span>
<span data-ttu-id="ce737-145">Länken för nästa sida med resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="ce737-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="ce737-146">Det här värdet hämtas med det första Get-AzEventGrid cmdlet-anropet när det fortfarande finns fler resurser att fråga efter.</span><span class="sxs-lookup"><span data-stu-id="ce737-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="ce737-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ce737-147">-ODataQuery</span></span>
<span data-ttu-id="ce737-148">OData-frågan som används för att filtrera listans resultat.</span><span class="sxs-lookup"><span data-stu-id="ce737-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="ce737-149">Filtrering stöds för närvarande endast i namn-egenskapen. De funktioner som stöds är: innehåller, EQ (för lika), Ne (för inte lika med) och, eller och inte.</span><span class="sxs-lookup"><span data-stu-id="ce737-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce737-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce737-150">-ResourceGroupName</span></span>
<span data-ttu-id="ce737-151">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ce737-151">The name of the resource group.</span></span>

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
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce737-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce737-152">-ResourceId</span></span>
<span data-ttu-id="ce737-153">Resurs-ID som representerar händelse rutnäts domänen.</span><span class="sxs-lookup"><span data-stu-id="ce737-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="ce737-154">-Överst</span><span class="sxs-lookup"><span data-stu-id="ce737-154">-Top</span></span>
<span data-ttu-id="ce737-155">Maximalt antal resurser som kan erhållas.</span><span class="sxs-lookup"><span data-stu-id="ce737-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="ce737-156">Giltigt värde är mellan 1 och 100.</span><span class="sxs-lookup"><span data-stu-id="ce737-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="ce737-157">Om högsta värde anges och fler resultat fortfarande är tillgängliga innehåller resultatet en länk till nästa sida som ska frågas i NextLink.</span><span class="sxs-lookup"><span data-stu-id="ce737-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="ce737-158">Om det högsta värdet inte anges returneras hela listan med resurser samtidigt.</span><span class="sxs-lookup"><span data-stu-id="ce737-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce737-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce737-159">CommonParameters</span></span>
<span data-ttu-id="ce737-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce737-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce737-161">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce737-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce737-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce737-162">INPUTS</span></span>

### <span data-ttu-id="ce737-163">System. String</span><span class="sxs-lookup"><span data-stu-id="ce737-163">System.String</span></span>

## <span data-ttu-id="ce737-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce737-164">OUTPUTS</span></span>

### <span data-ttu-id="ce737-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="ce737-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="ce737-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="ce737-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="ce737-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce737-167">NOTES</span></span>

## <span data-ttu-id="ce737-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce737-168">RELATED LINKS</span></span>
