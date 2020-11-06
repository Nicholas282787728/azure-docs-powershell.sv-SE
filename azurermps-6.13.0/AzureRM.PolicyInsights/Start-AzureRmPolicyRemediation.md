---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/start-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
ms.openlocfilehash: d5a0d4cd14f86c782defd7b70a1edee209982d2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575154"
---
# <span data-ttu-id="2df7d-101">Start-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="2df7d-101">Start-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="2df7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2df7d-102">SYNOPSIS</span></span>
<span data-ttu-id="2df7d-103">Skapar och startar en princip åtgärd för en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="2df7d-103">Creates and starts a policy remediation for a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2df7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2df7d-104">SYNTAX</span></span>

### <span data-ttu-id="2df7d-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="2df7d-105">ByName (Default)</span></span>
```
Start-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2df7d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2df7d-106">ByResourceId</span></span>
```
Start-AzureRmPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2df7d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2df7d-107">DESCRIPTION</span></span>
<span data-ttu-id="2df7d-108">Cmdleten **Start-AzureRmPolicyRemediation** skapar en princip åtgärd för en viss princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="2df7d-108">The **Start-AzureRmPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="2df7d-109">Alla icke-kompatibla resurser på eller under reparations omfattningen åtgärdas.</span><span class="sxs-lookup"><span data-stu-id="2df7d-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="2df7d-110">Åtgärd stöds endast för principer med "deployIfNotExists"-effekten.</span><span class="sxs-lookup"><span data-stu-id="2df7d-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="2df7d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2df7d-111">EXAMPLES</span></span>

### <span data-ttu-id="2df7d-112">Exempel 1: starta en reparation av abonnemangs omfattningen</span><span class="sxs-lookup"><span data-stu-id="2df7d-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="2df7d-113">Det här kommandot skapar en ny princip reparation i prenumerationens "min prenumeration" för den angivna princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="2df7d-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="2df7d-114">Exempel 2: påbörja en reparation av grupp omfattningen med valfria filter</span><span class="sxs-lookup"><span data-stu-id="2df7d-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzureRmPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="2df7d-115">Det här kommandot skapar en ny princip reparation i hanterings gruppen ' MG1 ' för den angivna princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="2df7d-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="2df7d-116">Endast resurser i platserna "västkusten" eller "öster" kommer att åtgärdas.</span><span class="sxs-lookup"><span data-stu-id="2df7d-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="2df7d-117">Exempel 3: starta en reparations åtgärd i resurs gruppens omfattning för en princip uppsättning med definitions tilldelning</span><span class="sxs-lookup"><span data-stu-id="2df7d-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzureRmPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="2df7d-118">Det här kommandot skapar en ny princip åtgärd i resurs gruppen ' myRG ' för den angivna princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="2df7d-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="2df7d-119">Princip tilldelningen tilldelar en definition för princip uppsättning (kallas även för ett initiativ).</span><span class="sxs-lookup"><span data-stu-id="2df7d-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="2df7d-120">Referens-ID för princip definition anger vilken princip som ska åtgärdas i initiativet.</span><span class="sxs-lookup"><span data-stu-id="2df7d-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="2df7d-121">Exempel 4: starta en reparation och vänta tills den är klar i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2df7d-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="2df7d-122">Det här kommandot startar en ny princip reparation i prenumerationens "min prenumeration" för den angivna princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="2df7d-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="2df7d-123">Reparationen kan slutföras innan den sista reparations statusen returneras.</span><span class="sxs-lookup"><span data-stu-id="2df7d-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

## <span data-ttu-id="2df7d-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2df7d-124">PARAMETERS</span></span>

### <span data-ttu-id="2df7d-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2df7d-125">-AsJob</span></span>
<span data-ttu-id="2df7d-126">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="2df7d-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2df7d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df7d-127">-DefaultProfile</span></span>
<span data-ttu-id="2df7d-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2df7d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2df7d-129">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="2df7d-129">-LocationFilter</span></span>
<span data-ttu-id="2df7d-130">Resurs platserna som ska ingå i reparationen.</span><span class="sxs-lookup"><span data-stu-id="2df7d-130">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="2df7d-131">Resurser som inte finns på dessa platser kommer inte att åtgärdas.</span><span class="sxs-lookup"><span data-stu-id="2df7d-131">Resources that don't reside in these locations will not be remediated.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df7d-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="2df7d-132">-ManagementGroupName</span></span>
<span data-ttu-id="2df7d-133">Hanterings grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="2df7d-133">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df7d-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="2df7d-134">-Name</span></span>
<span data-ttu-id="2df7d-135">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="2df7d-135">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df7d-136">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="2df7d-136">-PolicyAssignmentId</span></span>
<span data-ttu-id="2df7d-137">ID för tilldelning av policy.</span><span class="sxs-lookup"><span data-stu-id="2df7d-137">Policy assignment ID.</span></span>
<span data-ttu-id="2df7d-138">Namn@example.com.</span><span class="sxs-lookup"><span data-stu-id="2df7d-138">E.g.</span></span>
<span data-ttu-id="2df7d-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="2df7d-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df7d-140">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="2df7d-140">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="2df7d-141">Hämtar policy definition Reference ID för den enskilda definitionen som repare ras.</span><span class="sxs-lookup"><span data-stu-id="2df7d-141">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="2df7d-142">Krävs när princip tilldelnings definitionen tilldelas.</span><span class="sxs-lookup"><span data-stu-id="2df7d-142">Required when the policy assignment assigns a policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df7d-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df7d-143">-ResourceGroupName</span></span>
<span data-ttu-id="2df7d-144">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2df7d-144">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df7d-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2df7d-145">-ResourceId</span></span>
<span data-ttu-id="2df7d-146">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2df7d-146">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df7d-147">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="2df7d-147">-Scope</span></span>
<span data-ttu-id="2df7d-148">Omfattning av resursen.</span><span class="sxs-lookup"><span data-stu-id="2df7d-148">Scope of the resource.</span></span>
<span data-ttu-id="2df7d-149">Namn@example.com.</span><span class="sxs-lookup"><span data-stu-id="2df7d-149">E.g.</span></span>
<span data-ttu-id="2df7d-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="2df7d-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df7d-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2df7d-151">-Confirm</span></span>
<span data-ttu-id="2df7d-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2df7d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df7d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df7d-153">-WhatIf</span></span>
<span data-ttu-id="2df7d-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2df7d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2df7d-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2df7d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2df7d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df7d-156">CommonParameters</span></span>
<span data-ttu-id="2df7d-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df7d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df7d-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df7d-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df7d-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2df7d-159">INPUTS</span></span>

### <span data-ttu-id="2df7d-160">System. String</span><span class="sxs-lookup"><span data-stu-id="2df7d-160">System.String</span></span>

### <span data-ttu-id="2df7d-161">System. string []</span><span class="sxs-lookup"><span data-stu-id="2df7d-161">System.String[]</span></span>

## <span data-ttu-id="2df7d-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2df7d-162">OUTPUTS</span></span>

### <span data-ttu-id="2df7d-163">Microsoft. Azure. commands. PolicyInsights. Models. remedling. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="2df7d-163">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="2df7d-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2df7d-164">NOTES</span></span>

## <span data-ttu-id="2df7d-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2df7d-165">RELATED LINKS</span></span>
