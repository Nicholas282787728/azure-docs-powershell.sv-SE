---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44f7d3331d32092636c53850b0315f34b7df7808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919561"
---
# <span data-ttu-id="32560-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="32560-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="32560-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32560-102">SYNOPSIS</span></span>
<span data-ttu-id="32560-103">Hämtar princip åtgärder.</span><span class="sxs-lookup"><span data-stu-id="32560-103">Gets policy remediations.</span></span>

## <span data-ttu-id="32560-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32560-104">SYNTAX</span></span>

### <span data-ttu-id="32560-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="32560-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32560-106">ByName</span><span class="sxs-lookup"><span data-stu-id="32560-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32560-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="32560-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32560-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="32560-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32560-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="32560-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32560-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="32560-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32560-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32560-111">DESCRIPTION</span></span>
<span data-ttu-id="32560-112">Cmdleten **Get-AzPolicyRemediation** hämtar alla princip åtgärder i ett scope eller en viss åtgärd.</span><span class="sxs-lookup"><span data-stu-id="32560-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="32560-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32560-113">EXAMPLES</span></span>

### <span data-ttu-id="32560-114">Exempel 1: Hämta alla princip åtgärder i det aktuella abonnemanget</span><span class="sxs-lookup"><span data-stu-id="32560-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="32560-115">Det här kommandot får alla de åtgärder som skapas på eller under ett abonnemang med namnet "min prenumeration".</span><span class="sxs-lookup"><span data-stu-id="32560-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="32560-116">Exempel 2: skaffa en specifik policy och distributions uppgifter</span><span class="sxs-lookup"><span data-stu-id="32560-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="32560-117">Med det här kommandot hämtas reparations funktionen ' remediation1 ' från resurs gruppen ' myResourceGroup '.</span><span class="sxs-lookup"><span data-stu-id="32560-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="32560-118">Detaljerna för de resurser som repare ras kommer att ingå.</span><span class="sxs-lookup"><span data-stu-id="32560-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="32560-119">Exempel 3: få tio policyer för principer i en hanterings grupp med valfria filter</span><span class="sxs-lookup"><span data-stu-id="32560-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="32560-120">Det här kommandot får högst tio princips par från en hanterings grupp som heter ' MG1 '.</span><span class="sxs-lookup"><span data-stu-id="32560-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="32560-121">Endast princip reparation för den angivna princip tilldelningen kommer att hämtas.</span><span class="sxs-lookup"><span data-stu-id="32560-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="32560-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32560-122">PARAMETERS</span></span>

### <span data-ttu-id="32560-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32560-123">-DefaultProfile</span></span>
<span data-ttu-id="32560-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="32560-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32560-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="32560-125">-Filter</span></span>
<span data-ttu-id="32560-126">Filter uttryck med hjälp av OData-notation.</span><span class="sxs-lookup"><span data-stu-id="32560-126">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, GenericScope, ManagementGroupScope, ResourceGroupScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32560-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="32560-127">-IncludeDetail</span></span>
<span data-ttu-id="32560-128">Inkludera information om de distributioner som har skapats av reparationen.</span><span class="sxs-lookup"><span data-stu-id="32560-128">Include details of the deployments created by the remediation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32560-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="32560-129">-ManagementGroupName</span></span>
<span data-ttu-id="32560-130">Hanterings grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="32560-130">Management group ID.</span></span>

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

### <span data-ttu-id="32560-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="32560-131">-Name</span></span>
<span data-ttu-id="32560-132">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="32560-132">Resource name.</span></span>

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

### <span data-ttu-id="32560-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32560-133">-ResourceGroupName</span></span>
<span data-ttu-id="32560-134">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="32560-134">Resource group name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32560-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32560-135">-ResourceId</span></span>
<span data-ttu-id="32560-136">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="32560-136">Resource ID.</span></span>

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

### <span data-ttu-id="32560-137">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="32560-137">-Scope</span></span>
<span data-ttu-id="32560-138">Omfattning av resursen.</span><span class="sxs-lookup"><span data-stu-id="32560-138">Scope of the resource.</span></span> <span data-ttu-id="32560-139">Till exempel "/subscriptions/{subscriptionId}/resourceGroups/{rgName}".</span><span class="sxs-lookup"><span data-stu-id="32560-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

```yaml
Type: System.String
Parameter Sets: GenericScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32560-140">-Överst</span><span class="sxs-lookup"><span data-stu-id="32560-140">-Top</span></span>
<span data-ttu-id="32560-141">Maximalt antal poster att returnera.</span><span class="sxs-lookup"><span data-stu-id="32560-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="32560-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32560-142">CommonParameters</span></span>
<span data-ttu-id="32560-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32560-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32560-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32560-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32560-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32560-145">INPUTS</span></span>

### <span data-ttu-id="32560-146">System. String</span><span class="sxs-lookup"><span data-stu-id="32560-146">System.String</span></span>

## <span data-ttu-id="32560-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32560-147">OUTPUTS</span></span>

### <span data-ttu-id="32560-148">Microsoft. Azure. commands. PolicyInsights. Models. remedling. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="32560-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="32560-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32560-149">NOTES</span></span>

## <span data-ttu-id="32560-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32560-150">RELATED LINKS</span></span>
