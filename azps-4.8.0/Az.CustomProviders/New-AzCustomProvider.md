---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262326"
---
# <span data-ttu-id="0101c-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="0101c-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="0101c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0101c-102">SYNOPSIS</span></span>
<span data-ttu-id="0101c-103">Skapar eller uppdaterar den anpassade resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="0101c-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="0101c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0101c-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0101c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0101c-105">DESCRIPTION</span></span>
<span data-ttu-id="0101c-106">Skapar eller uppdaterar den anpassade resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="0101c-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="0101c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0101c-107">EXAMPLES</span></span>

### <span data-ttu-id="0101c-108">Exempel 1: skapa en anpassad leverantör</span><span class="sxs-lookup"><span data-stu-id="0101c-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="0101c-109">Skapa en anpassad resurs leverantör</span><span class="sxs-lookup"><span data-stu-id="0101c-109">Create a custom resource provider</span></span>

### <span data-ttu-id="0101c-110">Exempel 2: skapa en anpassad Provider med kopplingar</span><span class="sxs-lookup"><span data-stu-id="0101c-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="0101c-111">Skapa en anpassad leverantör med ett flöde för egna Provider-associationer.</span><span class="sxs-lookup"><span data-stu-id="0101c-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="0101c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0101c-112">PARAMETERS</span></span>

### <span data-ttu-id="0101c-113">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="0101c-113">-Action</span></span>
<span data-ttu-id="0101c-114">En lista med åtgärder som den anpassade resurs leverantören implementerar.</span><span class="sxs-lookup"><span data-stu-id="0101c-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="0101c-115">Om du vill skapa läser du avsnittet anteckningar för ÅTGÄRDs egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0101c-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0101c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0101c-116">-AsJob</span></span>
<span data-ttu-id="0101c-117">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="0101c-117">Run the command as a job</span></span>

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

### <span data-ttu-id="0101c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0101c-118">-DefaultProfile</span></span>
<span data-ttu-id="0101c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0101c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0101c-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="0101c-120">-Location</span></span>
<span data-ttu-id="0101c-121">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="0101c-121">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0101c-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0101c-122">-Name</span></span>
<span data-ttu-id="0101c-123">Namnet på resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="0101c-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0101c-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0101c-124">-NoWait</span></span>
<span data-ttu-id="0101c-125">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="0101c-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0101c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0101c-126">-ResourceGroupName</span></span>
<span data-ttu-id="0101c-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0101c-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0101c-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0101c-128">-ResourceType</span></span>
<span data-ttu-id="0101c-129">En lista över resurs typer som den anpassade resurs leverantören implementerar.</span><span class="sxs-lookup"><span data-stu-id="0101c-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="0101c-130">Om du vill skapa läser du avsnittet anteckningar för egenskaper för RESOURCETYPE och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0101c-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0101c-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0101c-131">-SubscriptionId</span></span>
<span data-ttu-id="0101c-132">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0101c-132">The Azure subscription ID.</span></span>
<span data-ttu-id="0101c-133">Det här är en GUID-formaterad sträng (till exempel 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="0101c-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0101c-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0101c-134">-Tag</span></span>
<span data-ttu-id="0101c-135">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="0101c-135">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0101c-136">-Verifiering</span><span class="sxs-lookup"><span data-stu-id="0101c-136">-Validation</span></span>
<span data-ttu-id="0101c-137">En lista över valideringar som ska utföras på de anpassade resurs leverantörens begär Anden.</span><span class="sxs-lookup"><span data-stu-id="0101c-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="0101c-138">Om du vill skapa läser du avsnittet anteckningar för VERIFIERINGs egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0101c-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0101c-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0101c-139">-Confirm</span></span>
<span data-ttu-id="0101c-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0101c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0101c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0101c-141">-WhatIf</span></span>
<span data-ttu-id="0101c-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0101c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0101c-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0101c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0101c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0101c-144">CommonParameters</span></span>
<span data-ttu-id="0101c-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0101c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0101c-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0101c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0101c-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0101c-147">INPUTS</span></span>

## <span data-ttu-id="0101c-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0101c-148">OUTPUTS</span></span>

### <span data-ttu-id="0101c-149">Microsoft. Azure. PowerShell. cmdletar. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="0101c-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="0101c-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0101c-150">NOTES</span></span>

<span data-ttu-id="0101c-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0101c-151">ALIASES</span></span>

<span data-ttu-id="0101c-152">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0101c-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0101c-153">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0101c-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0101c-154">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0101c-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0101c-155">ÅTGÄRD <ICustomRpActionRouteDefinition [] >: en lista med åtgärder som den anpassade resurs leverantören implementerar.</span><span class="sxs-lookup"><span data-stu-id="0101c-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="0101c-156">`Endpoint <String>`: Den URI för Dirigerings definition som den anpassade resurs leverantören kommer att begära.</span><span class="sxs-lookup"><span data-stu-id="0101c-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="0101c-157">Detta kan vara i form av en platt URI (till exempel " https://testendpoint/ ") eller ange för att dirigera via en sökväg (till exempel " https://testendpoint/{requestPath} ")</span><span class="sxs-lookup"><span data-stu-id="0101c-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="0101c-158">`Name <String>`: Namnet på flödes definitionen.</span><span class="sxs-lookup"><span data-stu-id="0101c-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="0101c-159">Detta blir namnet på ARM tillägget (till exempel "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="0101c-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="0101c-160">`[RoutingType <ActionRouting?>]`: De cirkulations typer som stöds för åtgärds förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="0101c-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="0101c-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition [] >: en lista över resurs typer som den anpassade resurs leverantören implementerar.</span><span class="sxs-lookup"><span data-stu-id="0101c-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="0101c-162">`Endpoint <String>`: Den URI för Dirigerings definition som den anpassade resurs leverantören kommer att begära.</span><span class="sxs-lookup"><span data-stu-id="0101c-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="0101c-163">Detta kan vara i form av en platt URI (till exempel " https://testendpoint/ ") eller ange för att dirigera via en sökväg (till exempel " https://testendpoint/{requestPath} ")</span><span class="sxs-lookup"><span data-stu-id="0101c-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="0101c-164">`Name <String>`: Namnet på flödes definitionen.</span><span class="sxs-lookup"><span data-stu-id="0101c-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="0101c-165">Detta blir namnet på ARM tillägget (till exempel "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="0101c-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="0101c-166">`[RoutingType <ResourceTypeRouting?>]`: De cirkulations typer som stöds för resurs förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="0101c-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="0101c-167">VERIFIERINGs <ICustomRpValidations [] >: en lista med valideringar som ska köras på de anpassade resurs leverantörens begär Anden.</span><span class="sxs-lookup"><span data-stu-id="0101c-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="0101c-168">`Specification <String>`: En länk till verifierings specifikationen.</span><span class="sxs-lookup"><span data-stu-id="0101c-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="0101c-169">Specifikationen måste finnas på raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="0101c-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="0101c-170">`[ValidationType <ValidationType?>]`: Den typ av verifiering som ska köras mot en matchande begäran.</span><span class="sxs-lookup"><span data-stu-id="0101c-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="0101c-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0101c-171">RELATED LINKS</span></span>
