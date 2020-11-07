---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 8ac0be356aa1f10df2543e65e03eae302e1d6454
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747552"
---
# <span data-ttu-id="013f5-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="013f5-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="013f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="013f5-102">SYNOPSIS</span></span>
<span data-ttu-id="013f5-103">Hämtar efterlevnadsprinciper för principer för resurser.</span><span class="sxs-lookup"><span data-stu-id="013f5-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="013f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="013f5-104">SYNTAX</span></span>

### <span data-ttu-id="013f5-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="013f5-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="013f5-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="013f5-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="013f5-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="013f5-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="013f5-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="013f5-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="013f5-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="013f5-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="013f5-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="013f5-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="013f5-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="013f5-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="013f5-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="013f5-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="013f5-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="013f5-113">DESCRIPTION</span></span>
<span data-ttu-id="013f5-114">Hämtar efterlevnadsprinciper för principer för resurser.</span><span class="sxs-lookup"><span data-stu-id="013f5-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="013f5-115">Poster för princip tillstånd kan frågas efter olika omfattningar.</span><span class="sxs-lookup"><span data-stu-id="013f5-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="013f5-116">Baserat på det tidsintervall som anges (standard för förra dagen), kan antingen de senaste princip tillstånden eller alla över gångar för princip status ställas till.</span><span class="sxs-lookup"><span data-stu-id="013f5-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="013f5-117">Resultaten kan filtreras, grupperas och grupp agg regeringar beräknas.</span><span class="sxs-lookup"><span data-stu-id="013f5-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="013f5-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="013f5-118">EXAMPLES</span></span>

### <span data-ttu-id="013f5-119">Exempel 1: Hämta de senaste princip tillstånden till aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="013f5-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="013f5-120">Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="013f5-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="013f5-121">Exempel 2: Hämta de senaste princip tillstånden i den angivna abonnemangs omfattningen</span><span class="sxs-lookup"><span data-stu-id="013f5-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="013f5-122">Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="013f5-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="013f5-123">Exempel 3: Hämta alla princip lägen i nuvarande prenumerations omfattning</span><span class="sxs-lookup"><span data-stu-id="013f5-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="013f5-124">Hämtar alla historiska princip tillstånds poster (inklusive senaste) som genererats av den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="013f5-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="013f5-125">Exempel 4: Hämta de senaste princip tillstånden i området hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="013f5-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="013f5-126">Hämtar de senaste princip tillstånds posterna som genererats för alla resurser i den angivna hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="013f5-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="013f5-127">Exempel 5: Hämta de senaste princip tillstånden i resurs gruppens omfattning i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="013f5-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="013f5-128">Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser i den angivna resurs gruppen (i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="013f5-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="013f5-129">Exempel 6: Hämta de senaste princip tillstånden i resurs gruppens omfattning i det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="013f5-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="013f5-130">Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser i den angivna resurs gruppen (i det angivna abonnemanget).</span><span class="sxs-lookup"><span data-stu-id="013f5-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="013f5-131">Exempel 7: Hämta de senaste princip tillstånden för en resurs</span><span class="sxs-lookup"><span data-stu-id="013f5-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="013f5-132">Hämtar de senaste princip tillstånds posterna skapade den sista dagen för den angivna resursen.</span><span class="sxs-lookup"><span data-stu-id="013f5-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="013f5-133">Exempel 8: Hämta de senaste princip tillstånden för en definition av en princip uppsättning i aktuellt abonnemang</span><span class="sxs-lookup"><span data-stu-id="013f5-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="013f5-134">Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättningar (som finns i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="013f5-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="013f5-135">Exempel 9: Hämta de senaste princip tillstånden för en definition av en princip uppsättning i det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="013f5-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="013f5-136">Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättningar (som finns i den angivna prenumerationen).</span><span class="sxs-lookup"><span data-stu-id="013f5-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="013f5-137">Exempel 10: Hämta de senaste princip tillstånden för en princip definition i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="013f5-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="013f5-138">Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="013f5-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="013f5-139">Exempel 11: Hämta de senaste princip tillstånden för en princip definition i det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="013f5-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="013f5-140">Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i den angivna prenumerationen).</span><span class="sxs-lookup"><span data-stu-id="013f5-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="013f5-141">Exempel 12: Hämta senaste policy tillstånd för en princip tilldelning i nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="013f5-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="013f5-142">Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="013f5-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="013f5-143">Exempel 13: Hämta de senaste princip tillstånden för en princip tilldelning i det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="013f5-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="013f5-144">Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i den angivna prenumerationen).</span><span class="sxs-lookup"><span data-stu-id="013f5-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="013f5-145">Exempel 14: Hämta de senaste princip tillstånden för en princip tilldelning i den angivna resurs gruppen i den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="013f5-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="013f5-146">Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i resurs gruppen i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="013f5-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="013f5-147">Exempel 15: Hämta de senaste princip lägena i aktuell prenumerations omfattning med OrderBy, Top och Select Query-alternativ</span><span class="sxs-lookup"><span data-stu-id="013f5-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="013f5-148">Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="013f5-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="013f5-149">Kommandot beställer resultaten efter tidsstämpel-och princip tilldelnings namn och tar bara upp 5 av de som listas i den ordningen.</span><span class="sxs-lookup"><span data-stu-id="013f5-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="013f5-150">Den väljer också att lista ut en delmängd av kolumnerna för varje post.</span><span class="sxs-lookup"><span data-stu-id="013f5-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="013f5-151">Exempel 16: Hämta de senaste princip lägena i aktuell prenumerations omfattning med alternativen från och till fråga</span><span class="sxs-lookup"><span data-stu-id="013f5-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="013f5-152">Hämtar de senaste princip tillstånds posterna som genererats inom det angivna datum intervallet för alla resurser i prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="013f5-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="013f5-153">Exempel 17: Hämta de senaste princip stegen i aktuellt prenumerations omfång med alternativet filtrera fråga</span><span class="sxs-lookup"><span data-stu-id="013f5-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and IsCompliant eq false and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="013f5-154">Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="013f5-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="013f5-155">Kommandot begränsar resultaten som returneras genom filtrering baserat på princip definitions åtgärden (inklusive neka-eller gransknings åtgärder), kompatibilitetsstatus (inkluderar endast icke-kompatibel status) och resurs plats (utesluter östasiatiska platser).</span><span class="sxs-lookup"><span data-stu-id="013f5-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="013f5-156">Exempel 18: Hämta de senaste princip tillstånden i aktuell prenumerations omfattning med tillämpa ange radantal agg regering</span><span class="sxs-lookup"><span data-stu-id="013f5-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="013f5-157">Hämtar antalet senaste princip status posterna som genererats den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="013f5-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="013f5-158">Kommandot returnerar antalet poster för princip tillstånd som returneras i egenskapen AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="013f5-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="013f5-159">Exempel 19: Hämta de senaste princip tillstånden i nuvarande prenumerations omfattning, med tillämpa ange gruppering med agg regering</span><span class="sxs-lookup"><span data-stu-id="013f5-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="013f5-160">Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="013f5-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="013f5-161">Kommandot begränsar resultaten som returneras genom filtrering baserat på kompatibilitetsstatus (inkluderar endast icke-kompatibel status).</span><span class="sxs-lookup"><span data-stu-id="013f5-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="013f5-162">Det grupperar resultaten baserat på princip tilldelning, princip uppsättnings definition och princip definition och beräknar antalet poster i varje grupp, som returneras i egenskapen AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="013f5-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="013f5-163">Den bevarar resultaten utifrån mängd agg regering i fallande ordning och tar bara upp 5 av de som anges i den ordningen.</span><span class="sxs-lookup"><span data-stu-id="013f5-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="013f5-164">Exempel 20: Hämta de senaste princip tillstånden i nuvarande prenumerations omfattning, med tillämpa ange gruppering utan agg regering</span><span class="sxs-lookup"><span data-stu-id="013f5-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="013f5-165">Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="013f5-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="013f5-166">Kommandot begränsar resultaten som returneras genom filtrering baserat på kompatibilitetsstatus (inkluderar endast icke-kompatibel status).</span><span class="sxs-lookup"><span data-stu-id="013f5-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="013f5-167">Resultatet grupperas utifrån resurs-ID. Då skapas en lista över alla resurser i prenumerationen som inte är kompatibla för minst en princip.</span><span class="sxs-lookup"><span data-stu-id="013f5-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="013f5-168">Exempel 21: Hämta de senaste princip tillstånden i aktuell prenumerations omfattning, med tillämpa flera grupperingar</span><span class="sxs-lookup"><span data-stu-id="013f5-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

<span data-ttu-id="013f5-169">Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="013f5-169">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="013f5-170">Kommandot begränsar resultaten som returneras genom filtrering baserat på kompatibilitetsstatus (inkluderar endast icke-kompatibel status).</span><span class="sxs-lookup"><span data-stu-id="013f5-170">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="013f5-171">Det grupperar resultaten först baserat på princip tilldelning, princip uppsättnings definition, princip definiering och resurs-ID. Sedan grupperas resultaten av den här grupperingen med samma egenskaper förutom för resurs-ID och det beräknade antalet poster i var och en av de här grupperna, som returneras i egenskapen AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="013f5-171">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="013f5-172">Den bevarar resultaten utifrån mängd agg regering i fallande ordning och tar bara upp 5 av de som anges i den ordningen.</span><span class="sxs-lookup"><span data-stu-id="013f5-172">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="013f5-173">Då skapas de 5 främsta principerna med flest antal icke-kompatibla resurser.</span><span class="sxs-lookup"><span data-stu-id="013f5-173">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="013f5-174">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="013f5-174">PARAMETERS</span></span>

### <span data-ttu-id="013f5-175">-Alla</span><span class="sxs-lookup"><span data-stu-id="013f5-175">-All</span></span>
<span data-ttu-id="013f5-176">I det angivna tidsintervallet får du alla princip lägen i stället för de senaste.</span><span class="sxs-lookup"><span data-stu-id="013f5-176">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="013f5-177">-Koppla</span><span class="sxs-lookup"><span data-stu-id="013f5-177">-Apply</span></span>
<span data-ttu-id="013f5-178">Använd uttryck för agg regeringar med OData-notation.</span><span class="sxs-lookup"><span data-stu-id="013f5-178">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="013f5-179">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="013f5-179">-DefaultProfile</span></span>
<span data-ttu-id="013f5-180">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="013f5-180">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="013f5-181">-Filter</span><span class="sxs-lookup"><span data-stu-id="013f5-181">-Filter</span></span>
<span data-ttu-id="013f5-182">Filter uttryck med hjälp av OData-notation.</span><span class="sxs-lookup"><span data-stu-id="013f5-182">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="013f5-183">-Från</span><span class="sxs-lookup"><span data-stu-id="013f5-183">-From</span></span>
<span data-ttu-id="013f5-184">ISO 8601 formaterad tidsstämpel anger start tiden för det intervall som ska frågas.</span><span class="sxs-lookup"><span data-stu-id="013f5-184">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="013f5-185">Om du inte anger något värde används värdet "till" minus 1 dag.</span><span class="sxs-lookup"><span data-stu-id="013f5-185">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="013f5-186">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="013f5-186">-ManagementGroupName</span></span>
<span data-ttu-id="013f5-187">Namn på hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="013f5-187">Management group name.</span></span>

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

### <span data-ttu-id="013f5-188">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="013f5-188">-OrderBy</span></span>
<span data-ttu-id="013f5-189">Beställnings uttryck med hjälp av OData-notation.</span><span class="sxs-lookup"><span data-stu-id="013f5-189">Ordering expression using OData notation.</span></span>
<span data-ttu-id="013f5-190">Ett eller flera kommaseparerade kolumn namn med "DESC" (standard) eller "ASC".</span><span class="sxs-lookup"><span data-stu-id="013f5-190">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="013f5-191">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="013f5-191">-PolicyAssignmentName</span></span>
<span data-ttu-id="013f5-192">Namn på princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="013f5-192">Policy assignment name.</span></span>

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

### <span data-ttu-id="013f5-193">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="013f5-193">-PolicyDefinitionName</span></span>
<span data-ttu-id="013f5-194">Princip definitions namn.</span><span class="sxs-lookup"><span data-stu-id="013f5-194">Policy definition name.</span></span>

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

### <span data-ttu-id="013f5-195">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="013f5-195">-PolicySetDefinitionName</span></span>
<span data-ttu-id="013f5-196">Definitions namn för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="013f5-196">Policy set definition name.</span></span>

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

### <span data-ttu-id="013f5-197">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="013f5-197">-ResourceGroupName</span></span>
<span data-ttu-id="013f5-198">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="013f5-198">Resource group name.</span></span>

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

### <span data-ttu-id="013f5-199">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="013f5-199">-ResourceId</span></span>
<span data-ttu-id="013f5-200">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="013f5-200">Resource ID.</span></span>

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

### <span data-ttu-id="013f5-201">-Välj</span><span class="sxs-lookup"><span data-stu-id="013f5-201">-Select</span></span>
<span data-ttu-id="013f5-202">Välj uttryck med hjälp av OData-notation.</span><span class="sxs-lookup"><span data-stu-id="013f5-202">Select expression using OData notation.</span></span>
<span data-ttu-id="013f5-203">Ett eller flera kommaseparerade kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="013f5-203">One or more comma-separated column names.</span></span>
<span data-ttu-id="013f5-204">Begränsar kolumnerna för varje post till de begärda.</span><span class="sxs-lookup"><span data-stu-id="013f5-204">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="013f5-205">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="013f5-205">-SubscriptionId</span></span>
<span data-ttu-id="013f5-206">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="013f5-206">Subscription ID.</span></span>

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

### <span data-ttu-id="013f5-207">-För att</span><span class="sxs-lookup"><span data-stu-id="013f5-207">-To</span></span>
<span data-ttu-id="013f5-208">ISO 8601 formaterad tidsstämpel som anger slut tiden för intervallet att fråga.</span><span class="sxs-lookup"><span data-stu-id="013f5-208">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="013f5-209">Om du inte anger det här är standardvärdet för tid.</span><span class="sxs-lookup"><span data-stu-id="013f5-209">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="013f5-210">-Överst</span><span class="sxs-lookup"><span data-stu-id="013f5-210">-Top</span></span>
<span data-ttu-id="013f5-211">Maximalt antal poster att returnera.</span><span class="sxs-lookup"><span data-stu-id="013f5-211">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="013f5-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="013f5-212">CommonParameters</span></span>
<span data-ttu-id="013f5-213">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="013f5-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="013f5-214">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="013f5-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="013f5-215">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="013f5-215">INPUTS</span></span>

### <span data-ttu-id="013f5-216">System. String</span><span class="sxs-lookup"><span data-stu-id="013f5-216">System.String</span></span>

## <span data-ttu-id="013f5-217">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="013f5-217">OUTPUTS</span></span>

### <span data-ttu-id="013f5-218">Microsoft. Azure. commands. PolicyInsights. Models. PolicyState</span><span class="sxs-lookup"><span data-stu-id="013f5-218">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="013f5-219">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="013f5-219">NOTES</span></span>

## <span data-ttu-id="013f5-220">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="013f5-220">RELATED LINKS</span></span>

[<span data-ttu-id="013f5-221">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="013f5-221">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)