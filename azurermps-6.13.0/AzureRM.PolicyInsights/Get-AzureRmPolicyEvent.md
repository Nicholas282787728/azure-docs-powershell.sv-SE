---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
ms.openlocfilehash: 0c4e4f531dac3f75f0eff69ba1dcfc644473ea06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578784"
---
# <span data-ttu-id="e02f9-101">Get-AzureRmPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="e02f9-101">Get-AzureRmPolicyEvent</span></span>

## <span data-ttu-id="e02f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e02f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e02f9-103">Hämtar princip utvärderings händelser som uppstår när resurser skapas eller uppdateras.</span><span class="sxs-lookup"><span data-stu-id="e02f9-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e02f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e02f9-104">SYNTAX</span></span>

### <span data-ttu-id="e02f9-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="e02f9-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02f9-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="e02f9-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02f9-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="e02f9-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02f9-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="e02f9-108">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02f9-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="e02f9-109">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02f9-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="e02f9-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02f9-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="e02f9-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02f9-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="e02f9-112">ResourceScope</span></span>
```
Get-AzureRmPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e02f9-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e02f9-113">DESCRIPTION</span></span>
<span data-ttu-id="e02f9-114">Hämtar princip utvärderings händelser som uppstår när resurser skapas eller uppdateras.</span><span class="sxs-lookup"><span data-stu-id="e02f9-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="e02f9-115">Poster i princip händelser kan frågas efter olika omfattningar baserat på det tidsintervall du angett (standard).</span><span class="sxs-lookup"><span data-stu-id="e02f9-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="e02f9-116">Resultaten kan filtreras, grupperas och grupp agg regeringar beräknas.</span><span class="sxs-lookup"><span data-stu-id="e02f9-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="e02f9-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e02f9-117">EXAMPLES</span></span>

### <span data-ttu-id="e02f9-118">Exempel 1: Hämta princip händelser i aktuell prenumerations omfattning</span><span class="sxs-lookup"><span data-stu-id="e02f9-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent
```

<span data-ttu-id="e02f9-119">Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="e02f9-120">Exempel 2: Hämta princip händelser i den angivna abonnemangs omfattningen</span><span class="sxs-lookup"><span data-stu-id="e02f9-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="e02f9-121">Hämtar princip händelse poster genererade under den sista dagen för alla resurser inom det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e02f9-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="e02f9-122">Exempel 3: Hämta princip händelser i omfattning för hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="e02f9-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="e02f9-123">Hämtar princip händelser genererade den sista dagen för alla resurser i den angivna hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="e02f9-124">Exempel 4: Hämta princip händelser i resurs gruppens omfattning i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="e02f9-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="e02f9-125">Hämtar princip händelse poster genererade under den sista dagen för alla resurser i den angivna resurs gruppen (i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="e02f9-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="e02f9-126">Exempel 5: Hämta princip händelser i resurs gruppens omfattning i det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="e02f9-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="e02f9-127">Hämtar princip händelse poster genererade under den sista dagen för alla resurser i den angivna resurs gruppen (i det angivna abonnemanget).</span><span class="sxs-lookup"><span data-stu-id="e02f9-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="e02f9-128">Exempel 6: Hämta princip händelser för en resurs</span><span class="sxs-lookup"><span data-stu-id="e02f9-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="e02f9-129">Hämtar princip händelser genererade den sista dagen för den angivna resursen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="e02f9-130">Exempel 7: Hämta princip händelser för en definition av en princip uppsättning i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="e02f9-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e02f9-131">Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättning (som finns i prenumerationen i den aktuella session-kontexten).</span><span class="sxs-lookup"><span data-stu-id="e02f9-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e02f9-132">Exempel 8: Hämta princip händelser för en definition av en princip uppsättning i det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="e02f9-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e02f9-133">Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättningar (som finns i den angivna prenumerationen).</span><span class="sxs-lookup"><span data-stu-id="e02f9-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e02f9-134">Exempel 9: Hämta princip händelser för en princip definition i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="e02f9-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e02f9-135">Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="e02f9-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e02f9-136">Exempel 10: Hämta princip händelser för en princip definition i det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="e02f9-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="e02f9-137">Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i det angivna abonnemanget).</span><span class="sxs-lookup"><span data-stu-id="e02f9-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e02f9-138">Exempel 11: Hämta princip händelser för en princip tilldelning i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="e02f9-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e02f9-139">Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="e02f9-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="e02f9-140">Exempel 12: Hämta princip händelser för en princip tilldelning i det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="e02f9-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e02f9-141">Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i den angivna prenumerationen).</span><span class="sxs-lookup"><span data-stu-id="e02f9-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="e02f9-142">Exempel 13: Hämta princip händelser för en princip tilldelning i den angivna resurs gruppen i den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="e02f9-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="e02f9-143">Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionskatalogen) som tillämpas av den angivna princip tilldelningen (som finns i resurs gruppen i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="e02f9-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="e02f9-144">Exempel 14: Hämta princip händelser i aktuell prenumerations omfattning med OrderBy, Top och Select Query-alternativ</span><span class="sxs-lookup"><span data-stu-id="e02f9-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="e02f9-145">Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e02f9-146">Kommandot beställer resultaten efter tidsstämpel-och princip tilldelnings namn och tar bara upp 5 av de som listas i den ordningen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="e02f9-147">Den väljer också att lista ut en delmängd av kolumnerna för varje post.</span><span class="sxs-lookup"><span data-stu-id="e02f9-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="e02f9-148">Exempel 15: Hämta princip händelser i aktuell prenumerations omfattning med alternativen från och till fråga</span><span class="sxs-lookup"><span data-stu-id="e02f9-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="e02f9-149">Hämtar princip händelse poster som genereras inom det datum intervall som anges för alla resurser i prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="e02f9-150">Exempel 16: Hämta princip händelser i aktuell prenumerations omfattning med alternativet filtrera fråga</span><span class="sxs-lookup"><span data-stu-id="e02f9-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="e02f9-151">Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="e02f9-152">Kommandot begränsar resultaten som returneras genom filtrering baserat på princip definitions åtgärden (inklusive neka-eller gransknings åtgärder) och resurs plats (exklusive östasiatiska platser).</span><span class="sxs-lookup"><span data-stu-id="e02f9-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="e02f9-153">Exempel 17: Hämta princip händelser i aktuell prenumerations omfattning med tillämpa ange radantal agg regering</span><span class="sxs-lookup"><span data-stu-id="e02f9-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="e02f9-154">Hämtar antalet princip händelse poster som genererats under den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="e02f9-155">Kommandot returnerar antalet princip poster, som returneras i egenskapen AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="e02f9-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="e02f9-156">Exempel 18: Hämta princip händelser i aktuell prenumerations omfattning med tillämpa ange gruppering med agg regering</span><span class="sxs-lookup"><span data-stu-id="e02f9-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="e02f9-157">Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e02f9-158">Kommandot begränsar resultaten som returneras genom filtrering baserat på princip definitions åtgärden (inkluderar endast gransknings-och avvisa händelser).</span><span class="sxs-lookup"><span data-stu-id="e02f9-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="e02f9-159">Det grupperar resultaten baserat på princip tilldelning, princip definiering, princip definierings åtgärd och resurs-ID, och beräknar antalet poster i varje grupp, som returneras i egenskapen AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="e02f9-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="e02f9-160">Den bevarar resultaten utifrån mängd agg regering i fallande ordning och tar bara upp 5 av de som anges i den ordningen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="e02f9-161">Exempel 19: Hämta princip händelser i aktuell prenumerations omfattning med tillämpa ange gruppering utan agg regering</span><span class="sxs-lookup"><span data-stu-id="e02f9-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="e02f9-162">Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e02f9-163">Kommandot begränsar resultaten som returneras genom filtrering baserat på princip definitions åtgärden (inkluderar endast gransknings-och avvisa händelser).</span><span class="sxs-lookup"><span data-stu-id="e02f9-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="e02f9-164">Resultatet grupperas utifrån resurs-ID. Då skapas en lista över alla resurser i prenumerationen som genererade en princip händelse för minst en gransknings-eller nekande policy.</span><span class="sxs-lookup"><span data-stu-id="e02f9-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="e02f9-165">Exempel 20: Hämta princip händelser i aktuell prenumerations omfattning med tillämpa flera grupperingar</span><span class="sxs-lookup"><span data-stu-id="e02f9-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="e02f9-166">Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="e02f9-167">Kommandot begränsar resultatet som returneras genom filtrering baserat på princip definitions åtgärden (inkluderar endast neka-händelser).</span><span class="sxs-lookup"><span data-stu-id="e02f9-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="e02f9-168">Resultatet grupperas först baserat på princip tilldelning, princip definiering och resurs-ID. Sedan grupperas resultaten av den här grupperingen med samma egenskaper förutom för resurs-ID och det beräknade antalet poster i var och en av de här grupperna, som returneras i egenskapen AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="e02f9-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="e02f9-169">Den bevarar resultaten utifrån mängd agg regering i fallande ordning och tar bara upp 5 av de som anges i den ordningen.</span><span class="sxs-lookup"><span data-stu-id="e02f9-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="e02f9-170">Då skapas de 5 högsta neka-principerna med flest nekade resurser.</span><span class="sxs-lookup"><span data-stu-id="e02f9-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="e02f9-171">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e02f9-171">PARAMETERS</span></span>

### <span data-ttu-id="e02f9-172">-Koppla</span><span class="sxs-lookup"><span data-stu-id="e02f9-172">-Apply</span></span>
<span data-ttu-id="e02f9-173">Använd uttryck för agg regeringar med OData-notation.</span><span class="sxs-lookup"><span data-stu-id="e02f9-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="e02f9-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02f9-174">-DefaultProfile</span></span>
<span data-ttu-id="e02f9-175">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e02f9-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-176">-Filter</span><span class="sxs-lookup"><span data-stu-id="e02f9-176">-Filter</span></span>
<span data-ttu-id="e02f9-177">Filter uttryck med hjälp av OData-notation.</span><span class="sxs-lookup"><span data-stu-id="e02f9-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="e02f9-178">-Från</span><span class="sxs-lookup"><span data-stu-id="e02f9-178">-From</span></span>
<span data-ttu-id="e02f9-179">ISO 8601 formaterad tidsstämpel anger start tiden för det intervall som ska frågas.</span><span class="sxs-lookup"><span data-stu-id="e02f9-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="e02f9-180">Om du inte anger något värde används värdet "till" minus 1 dag.</span><span class="sxs-lookup"><span data-stu-id="e02f9-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="e02f9-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e02f9-181">-ManagementGroupName</span></span>
<span data-ttu-id="e02f9-182">Namn på hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="e02f9-182">Management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="e02f9-183">-OrderBy</span></span>
<span data-ttu-id="e02f9-184">Beställnings uttryck med hjälp av OData-notation.</span><span class="sxs-lookup"><span data-stu-id="e02f9-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="e02f9-185">Ett eller flera kommaseparerade kolumn namn med "DESC" (standard) eller "ASC".</span><span class="sxs-lookup"><span data-stu-id="e02f9-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="e02f9-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e02f9-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="e02f9-187">Namn på princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="e02f9-187">Policy assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e02f9-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="e02f9-189">Princip definitions namn.</span><span class="sxs-lookup"><span data-stu-id="e02f9-189">Policy definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e02f9-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="e02f9-191">Definitions namn för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e02f9-191">Policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02f9-192">-ResourceGroupName</span></span>
<span data-ttu-id="e02f9-193">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e02f9-193">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e02f9-194">-ResourceId</span></span>
<span data-ttu-id="e02f9-195">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e02f9-195">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-196">-Välj</span><span class="sxs-lookup"><span data-stu-id="e02f9-196">-Select</span></span>
<span data-ttu-id="e02f9-197">Välj uttryck med hjälp av OData-notation.</span><span class="sxs-lookup"><span data-stu-id="e02f9-197">Select expression using OData notation.</span></span>
<span data-ttu-id="e02f9-198">Ett eller flera kommaseparerade kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="e02f9-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="e02f9-199">Begränsar kolumnerna för varje post till de begärda.</span><span class="sxs-lookup"><span data-stu-id="e02f9-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="e02f9-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e02f9-200">-SubscriptionId</span></span>
<span data-ttu-id="e02f9-201">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="e02f9-201">Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-202">-För att</span><span class="sxs-lookup"><span data-stu-id="e02f9-202">-To</span></span>
<span data-ttu-id="e02f9-203">ISO 8601 formaterad tidsstämpel som anger slut tiden för intervallet att fråga.</span><span class="sxs-lookup"><span data-stu-id="e02f9-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="e02f9-204">Om du inte anger det här är standardvärdet för tid.</span><span class="sxs-lookup"><span data-stu-id="e02f9-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="e02f9-205">-Överst</span><span class="sxs-lookup"><span data-stu-id="e02f9-205">-Top</span></span>
<span data-ttu-id="e02f9-206">Maximalt antal poster att returnera.</span><span class="sxs-lookup"><span data-stu-id="e02f9-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="e02f9-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02f9-207">CommonParameters</span></span>
<span data-ttu-id="e02f9-208">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02f9-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02f9-209">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e02f9-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02f9-210">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e02f9-210">INPUTS</span></span>

### <span data-ttu-id="e02f9-211">System. String</span><span class="sxs-lookup"><span data-stu-id="e02f9-211">System.String</span></span>

## <span data-ttu-id="e02f9-212">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e02f9-212">OUTPUTS</span></span>

### <span data-ttu-id="e02f9-213">Microsoft. Azure. commands. PolicyInsights. Models. PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="e02f9-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="e02f9-214">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e02f9-214">NOTES</span></span>

## <span data-ttu-id="e02f9-215">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e02f9-215">RELATED LINKS</span></span>