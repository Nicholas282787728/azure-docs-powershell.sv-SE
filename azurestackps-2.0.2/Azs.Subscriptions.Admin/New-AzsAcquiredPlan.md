---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 0db0f7ae4358e49ff62f94132701be1f4bd4d0b7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100052"
---
# <span data-ttu-id="8d459-101">New-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="8d459-101">New-AzsAcquiredPlan</span></span>

## <span data-ttu-id="8d459-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d459-102">SYNOPSIS</span></span>


## <span data-ttu-id="8d459-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d459-103">SYNTAX</span></span>

### <span data-ttu-id="8d459-104">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="8d459-104">CreateExpanded (Default)</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> [-PlanAcquisitionId <String>] [-SubscriptionId <String>]
 [-AcquisitionTime <DateTime>] [-ExternalReferenceId <String>] [-Id <String>] [-PlanId <String>]
 [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8d459-105">Göra</span><span class="sxs-lookup"><span data-stu-id="8d459-105">Create</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> -AcquiredPlanDefinition <IPlanAcquisition>
 [-PlanAcquisitionId <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8d459-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d459-106">DESCRIPTION</span></span>


## <span data-ttu-id="8d459-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d459-107">EXAMPLES</span></span>

### <span data-ttu-id="8d459-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8d459-108">Example 1</span></span>
```powershell
PS C:\> New-AzsAcquiredPlan -PlanAcquisitionId $([Guid]::NewGuid()) -PlanId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="8d459-109">Skapa en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="8d459-109">Create a subscription plan.</span></span>

## <span data-ttu-id="8d459-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d459-110">PARAMETERS</span></span>

### <span data-ttu-id="8d459-111">-AcquiredPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="8d459-111">-AcquiredPlanDefinition</span></span>
<span data-ttu-id="8d459-112">För att konstruera kan du läsa avsnittet anteckningar för ACQUIREDPLANDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8d459-112">To construct, see NOTES section for ACQUIREDPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8d459-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="8d459-113">-AcquisitionTime</span></span>


```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d459-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d459-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="8d459-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="8d459-115">-ExternalReferenceId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d459-116">-ID</span><span class="sxs-lookup"><span data-stu-id="8d459-116">-Id</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d459-117">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="8d459-117">-PlanAcquisitionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d459-118">-PlanId</span><span class="sxs-lookup"><span data-stu-id="8d459-118">-PlanId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d459-119">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="8d459-119">-ProvisioningState</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d459-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d459-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="8d459-121">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d459-121">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="8d459-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d459-122">-Confirm</span></span>
<span data-ttu-id="8d459-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d459-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d459-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d459-124">-WhatIf</span></span>
<span data-ttu-id="8d459-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d459-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d459-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d459-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d459-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d459-127">CommonParameters</span></span>
<span data-ttu-id="8d459-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d459-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d459-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d459-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d459-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d459-130">INPUTS</span></span>

### <span data-ttu-id="8d459-131">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="8d459-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

## <span data-ttu-id="8d459-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d459-132">OUTPUTS</span></span>

### <span data-ttu-id="8d459-133">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="8d459-133">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="8d459-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8d459-134">ALIASES</span></span>

<span data-ttu-id="8d459-135">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="8d459-135">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="8d459-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d459-136">NOTES</span></span>

<span data-ttu-id="8d459-137">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8d459-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d459-138">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d459-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8d459-139">ACQUIREDPLANDEFINITION <IPlanAcquisition> :</span><span class="sxs-lookup"><span data-stu-id="8d459-139">ACQUIREDPLANDEFINITION <IPlanAcquisition>:</span></span> 
  - <span data-ttu-id="8d459-140">`[AcquisitionId <String>]`: Anskaffnings-ID.</span><span class="sxs-lookup"><span data-stu-id="8d459-140">`[AcquisitionId <String>]`: Acquisition identifier.</span></span>
  - <span data-ttu-id="8d459-141">`[AcquisitionTime <DateTime?>]`: Anskaffnings tid.</span><span class="sxs-lookup"><span data-stu-id="8d459-141">`[AcquisitionTime <DateTime?>]`: Acquisition time.</span></span>
  - <span data-ttu-id="8d459-142">`[ExternalReferenceId <String>]`: Identifierare för extern referens.</span><span class="sxs-lookup"><span data-stu-id="8d459-142">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="8d459-143">`[Id <String>]`: ID i kontext för klient organisationens prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8d459-143">`[Id <String>]`: Identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="8d459-144">`[PlanId <String>]`: Planera identifierare i kontexten för klient organisations prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8d459-144">`[PlanId <String>]`: Plan identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="8d459-145">`[ProvisioningState <ProvisioningState?>]`: Etablerings status.</span><span class="sxs-lookup"><span data-stu-id="8d459-145">`[ProvisioningState <ProvisioningState?>]`: State of the provisioning.</span></span>

## <span data-ttu-id="8d459-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d459-146">RELATED LINKS</span></span>

