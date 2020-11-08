---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271299"
---
# <span data-ttu-id="aba04-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="aba04-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="aba04-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aba04-102">SYNOPSIS</span></span>
<span data-ttu-id="aba04-103">Hämtar den senaste översikten över efterlevnad för principer för resurser.</span><span class="sxs-lookup"><span data-stu-id="aba04-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="aba04-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aba04-104">SYNTAX</span></span>

### <span data-ttu-id="aba04-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="aba04-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aba04-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="aba04-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aba04-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="aba04-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aba04-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="aba04-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aba04-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="aba04-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aba04-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="aba04-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aba04-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="aba04-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aba04-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="aba04-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aba04-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aba04-113">DESCRIPTION</span></span>
<span data-ttu-id="aba04-114">Får en sammanfattningsvy över de senaste tillstånds numren för policy efterlevnad för olika scope, nedbrutna till princip tilldelningar och princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="aba04-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="aba04-115">Den innehåller endast icke-kompatibla princip tillstånd.</span><span class="sxs-lookup"><span data-stu-id="aba04-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="aba04-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aba04-116">EXAMPLES</span></span>

### <span data-ttu-id="aba04-117">Exempel 1: Hämta senaste icke-kompatibla princip status sammanfattning för aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="aba04-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="aba04-118">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser inom prenumerationen i den aktuella sessionskatalogen.</span><span class="sxs-lookup"><span data-stu-id="aba04-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="aba04-119">Exempel 2: Hämta senaste icke-kompatibla princip status sammanfattning för det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="aba04-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="aba04-120">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser inom det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="aba04-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="aba04-121">Exempel 3: Hämta senaste icke-kompatibla princip status sammanfattning i hanterings gruppens omfattning</span><span class="sxs-lookup"><span data-stu-id="aba04-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="aba04-122">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser i den angivna hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="aba04-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="aba04-123">Exempel 4: Hämta senaste icke-kompatibla princip status sammanfattning i resurs gruppens omfattning i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="aba04-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="aba04-124">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser i den angivna resurs gruppen (i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="aba04-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="aba04-125">Exempel 5: Hämta senaste icke-kompatibla princip status sammanfattning i resurs gruppens omfattning i det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="aba04-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="aba04-126">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser i den angivna resurs gruppen (i den angivna prenumerationen).</span><span class="sxs-lookup"><span data-stu-id="aba04-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="aba04-127">Exempel 6: Hämta senaste icke-kompatibla princip status sammanfattning för en resurs</span><span class="sxs-lookup"><span data-stu-id="aba04-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="aba04-128">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för den angivna resursen.</span><span class="sxs-lookup"><span data-stu-id="aba04-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="aba04-129">Exempel 7: Hämta senaste icke-kompatibla princip status sammanfattning för en princip uppsättnings definition i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="aba04-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="aba04-130">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (i klient organisationen i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättning (som finns i prenumerationen i den aktuella session-kontexten).</span><span class="sxs-lookup"><span data-stu-id="aba04-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="aba04-131">Exempel 8: Hämta senaste icke-kompatibla princip status sammanfattning för en princip uppsättnings definition i det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="aba04-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="aba04-132">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättning (som finns i den angivna prenumerationen).</span><span class="sxs-lookup"><span data-stu-id="aba04-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="aba04-133">Exempel 9: Hämta senaste icke-kompatibla princip status sammanfattning för en princip definition i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="aba04-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="aba04-134">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="aba04-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="aba04-135">Exempel 10: Hämta senaste icke-kompatibla princip status sammanfattning för en princip definition i det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="aba04-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="aba04-136">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (i klient organisationen i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i den angivna prenumerationen).</span><span class="sxs-lookup"><span data-stu-id="aba04-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="aba04-137">Exempel 11: Hämta senaste icke-kompatibla princip status översikt för en princip tilldelning i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="aba04-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="aba04-138">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i prenumerationen i aktuell session-kontext).</span><span class="sxs-lookup"><span data-stu-id="aba04-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="aba04-139">Exempel 12: Hämta senaste icke-kompatibla princip tillstånds Sammanfattning för en princip tilldelning i den angivna prenumerationen</span><span class="sxs-lookup"><span data-stu-id="aba04-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="aba04-140">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (i klient organisationen i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i den angivna prenumerationen).</span><span class="sxs-lookup"><span data-stu-id="aba04-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="aba04-141">Exempel 13: Hämta senaste icke-kompatibla princip status sammanfattning för en princip tilldelning i den angivna resurs gruppen i den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="aba04-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="aba04-142">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i resurs gruppen i prenumerationen i den aktuella sessionen).</span><span class="sxs-lookup"><span data-stu-id="aba04-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="aba04-143">Exempel 14: Hämta senaste icke-kompatibla princip status sammanfattning i den aktuella prenumerations omfattningen, med alternativet Top Query</span><span class="sxs-lookup"><span data-stu-id="aba04-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="aba04-144">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser inom prenumerationen i den aktuella sessionskatalogen.</span><span class="sxs-lookup"><span data-stu-id="aba04-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="aba04-145">Kommandot beställer sammanfattningar av princip tilldelningar i resultaten efter icke-kompatibla resurs räkningar i fallande ordning och endast de 5 högsta av dessa princip tilldelnings sammanfattningar används.</span><span class="sxs-lookup"><span data-stu-id="aba04-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="aba04-146">Exempel 15: Hämta senaste icke-kompatibla princip status sammanfattning i den aktuella prenumerations omfattningen med alternativen från och till fråga</span><span class="sxs-lookup"><span data-stu-id="aba04-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="aba04-147">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats inom det datum intervall som anges för alla resurser i prenumerationen i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="aba04-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="aba04-148">Exempel 16: Hämta senaste icke-kompatibla princip status sammanfattning i aktuell prenumerations omfattning med alternativet filtrera fråga</span><span class="sxs-lookup"><span data-stu-id="aba04-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="aba04-149">Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser inom prenumerationen i den aktuella sessionskatalogen.</span><span class="sxs-lookup"><span data-stu-id="aba04-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="aba04-150">Kommandot begränsar resultaten som returneras genom filtrering baserat på princip definitions åtgärden (inklusive neka-eller gransknings åtgärder) och resurs plats (utesluter östasiatiska platser).</span><span class="sxs-lookup"><span data-stu-id="aba04-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="aba04-151">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aba04-151">PARAMETERS</span></span>

### <span data-ttu-id="aba04-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba04-152">-DefaultProfile</span></span>
<span data-ttu-id="aba04-153">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aba04-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aba04-154">-Filter</span><span class="sxs-lookup"><span data-stu-id="aba04-154">-Filter</span></span>
<span data-ttu-id="aba04-155">Filter uttryck med hjälp av OData-notation.</span><span class="sxs-lookup"><span data-stu-id="aba04-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="aba04-156">-Från</span><span class="sxs-lookup"><span data-stu-id="aba04-156">-From</span></span>
<span data-ttu-id="aba04-157">ISO 8601 formaterad tidsstämpel anger start tiden för det intervall som ska frågas.</span><span class="sxs-lookup"><span data-stu-id="aba04-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="aba04-158">Om du inte anger något värde används värdet "till" minus 1 dag.</span><span class="sxs-lookup"><span data-stu-id="aba04-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="aba04-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="aba04-159">-ManagementGroupName</span></span>
<span data-ttu-id="aba04-160">Namn på hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="aba04-160">Management group name.</span></span>

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

### <span data-ttu-id="aba04-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="aba04-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="aba04-162">Namn på princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="aba04-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="aba04-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="aba04-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="aba04-164">Princip definitions namn.</span><span class="sxs-lookup"><span data-stu-id="aba04-164">Policy definition name.</span></span>

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

### <span data-ttu-id="aba04-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="aba04-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="aba04-166">Definitions namn för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="aba04-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="aba04-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba04-167">-ResourceGroupName</span></span>
<span data-ttu-id="aba04-168">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="aba04-168">Resource group name.</span></span>

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

### <span data-ttu-id="aba04-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aba04-169">-ResourceId</span></span>
<span data-ttu-id="aba04-170">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="aba04-170">Resource ID.</span></span>

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

### <span data-ttu-id="aba04-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aba04-171">-SubscriptionId</span></span>
<span data-ttu-id="aba04-172">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="aba04-172">Subscription ID.</span></span>

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

### <span data-ttu-id="aba04-173">-För att</span><span class="sxs-lookup"><span data-stu-id="aba04-173">-To</span></span>
<span data-ttu-id="aba04-174">ISO 8601 formaterad tidsstämpel som anger slut tiden för intervallet att fråga.</span><span class="sxs-lookup"><span data-stu-id="aba04-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="aba04-175">Om du inte anger det här är standardvärdet för tid.</span><span class="sxs-lookup"><span data-stu-id="aba04-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="aba04-176">-Överst</span><span class="sxs-lookup"><span data-stu-id="aba04-176">-Top</span></span>
<span data-ttu-id="aba04-177">Maximalt antal poster att returnera.</span><span class="sxs-lookup"><span data-stu-id="aba04-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="aba04-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba04-178">CommonParameters</span></span>
<span data-ttu-id="aba04-179">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aba04-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba04-180">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aba04-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba04-181">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aba04-181">INPUTS</span></span>

### <span data-ttu-id="aba04-182">System. String</span><span class="sxs-lookup"><span data-stu-id="aba04-182">System.String</span></span>

## <span data-ttu-id="aba04-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aba04-183">OUTPUTS</span></span>

### <span data-ttu-id="aba04-184">Microsoft. Azure. commands. PolicyInsights. Models. PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="aba04-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="aba04-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aba04-185">NOTES</span></span>

## <span data-ttu-id="aba04-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aba04-186">RELATED LINKS</span></span>

[<span data-ttu-id="aba04-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="aba04-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
