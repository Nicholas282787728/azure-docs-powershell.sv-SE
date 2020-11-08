---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsoffer
schema: 2.0.0
ms.openlocfilehash: 82be26ae402278d8cdc24195fd62ed09b67bdc14
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099894"
---
# <span data-ttu-id="f986d-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="f986d-101">Set-AzsOffer</span></span>

## <span data-ttu-id="f986d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f986d-102">SYNOPSIS</span></span>
<span data-ttu-id="f986d-103">Skapa eller uppdatera ett bud.</span><span class="sxs-lookup"><span data-stu-id="f986d-103">Create or update the offer.</span></span>

## <span data-ttu-id="f986d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f986d-104">SYNTAX</span></span>

### <span data-ttu-id="f986d-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="f986d-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-BasePlanIds <String[]>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-MaxSubscriptionsPerAccount <Int32>] [-PropertiesName <String>] [-State <AccessibilityState>]
 [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f986d-106">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="f986d-106">Update</span></span>
```
Set-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f986d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f986d-107">DESCRIPTION</span></span>
<span data-ttu-id="f986d-108">Skapa eller uppdatera ett bud.</span><span class="sxs-lookup"><span data-stu-id="f986d-108">Create or update the offer.</span></span>

## <span data-ttu-id="f986d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f986d-109">EXAMPLES</span></span>

### <span data-ttu-id="f986d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f986d-110">Example 1</span></span>
```powershell
PS C:\> $Offer = Get-AzsAdminManagedOffer | Select-Object -First 1
$Offer.MaxSubscriptionsPerAccount = 18
$Offer | Set-AzsOffer

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056}
Description                : 
DisplayName                : DRPTestOffer5056
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Location                   : redmond
MaxSubscriptionsPerAccount : 18
Name                       : DRPTestOffer5056
PropertiesName             : DRPTestOffer5056
State                      : Private
SubscriptionCount          : 5
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="f986d-111">Uppdatera ett bud.</span><span class="sxs-lookup"><span data-stu-id="f986d-111">Update an offer.</span></span>

## <span data-ttu-id="f986d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f986d-112">PARAMETERS</span></span>

### <span data-ttu-id="f986d-113">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="f986d-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="f986d-114">Referenser till tilläggs planer som en klient organisation kan erhålla för att bli en del av det.</span><span class="sxs-lookup"><span data-stu-id="f986d-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="f986d-115">För att konstruera kan du läsa avsnittet anteckningar för ADDONPLANDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f986d-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="f986d-116">-BasePlanIds</span></span>
<span data-ttu-id="f986d-117">Identifierare för de grundläggande abonnemang som blir tillgängliga för klient organisationen omedelbart när en klient organisation abonnerar på ett bud.</span><span class="sxs-lookup"><span data-stu-id="f986d-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f986d-118">-DefaultProfile</span></span>
<span data-ttu-id="f986d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f986d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f986d-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="f986d-120">-Description</span></span>
<span data-ttu-id="f986d-121">Beskrivning av bud.</span><span class="sxs-lookup"><span data-stu-id="f986d-121">Description of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f986d-122">-DisplayName</span></span>
<span data-ttu-id="f986d-123">Visnings namn för bud.</span><span class="sxs-lookup"><span data-stu-id="f986d-123">Display name of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-124">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="f986d-124">-ExternalReferenceId</span></span>
<span data-ttu-id="f986d-125">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="f986d-125">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="f986d-126">-Location</span></span>
<span data-ttu-id="f986d-127">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="f986d-127">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="f986d-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="f986d-129">Maximalt antal prenumerationer per konto.</span><span class="sxs-lookup"><span data-stu-id="f986d-129">Maximum subscriptions per account.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="f986d-130">-Name</span></span>
<span data-ttu-id="f986d-131">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="f986d-131">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="f986d-132">-OfferDefinition</span></span>
<span data-ttu-id="f986d-133">Representerar ett utbud av tjänster som ett abonnemang kan skapas för.</span><span class="sxs-lookup"><span data-stu-id="f986d-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="f986d-134">För att konstruera kan du läsa avsnittet anteckningar för OFFERDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f986d-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-135">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="f986d-135">-PropertiesName</span></span>
<span data-ttu-id="f986d-136">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="f986d-136">Name of the Offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f986d-137">-ResourceGroupName</span></span>
<span data-ttu-id="f986d-138">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="f986d-138">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-139">-State</span><span class="sxs-lookup"><span data-stu-id="f986d-139">-State</span></span>
<span data-ttu-id="f986d-140">Ge hjälpmedels status.</span><span class="sxs-lookup"><span data-stu-id="f986d-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-141">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="f986d-141">-SubscriptionCount</span></span>
<span data-ttu-id="f986d-142">Aktuellt antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="f986d-142">Current subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f986d-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f986d-143">-SubscriptionId</span></span>
<span data-ttu-id="f986d-144">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f986d-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f986d-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f986d-145">-Confirm</span></span>
<span data-ttu-id="f986d-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f986d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f986d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f986d-147">-WhatIf</span></span>
<span data-ttu-id="f986d-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f986d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f986d-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f986d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f986d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f986d-150">CommonParameters</span></span>
<span data-ttu-id="f986d-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f986d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f986d-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f986d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f986d-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f986d-153">INPUTS</span></span>

### <span data-ttu-id="f986d-154">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="f986d-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="f986d-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f986d-155">OUTPUTS</span></span>

### <span data-ttu-id="f986d-156">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="f986d-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="f986d-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f986d-157">ALIASES</span></span>

## <span data-ttu-id="f986d-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f986d-158">NOTES</span></span>

<span data-ttu-id="f986d-159">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="f986d-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f986d-160">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f986d-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f986d-161">ADDONPLANDEFINITION <IAddonPlanDefinition [] >: referenser till tilläggs planer som en klient organisation kan skaffa som en del av ett bud.</span><span class="sxs-lookup"><span data-stu-id="f986d-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="f986d-162">`[MaxAcquisitionCount <Int32?>]`: Maximalt antal instanser som kan erhållas av en enda prenumeration.</span><span class="sxs-lookup"><span data-stu-id="f986d-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="f986d-163">Om det inte anges är det förmodade värdet 1.</span><span class="sxs-lookup"><span data-stu-id="f986d-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="f986d-164">`[PlanId <String>]`: Plan-ID.</span><span class="sxs-lookup"><span data-stu-id="f986d-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="f986d-165">OFFERDEFINITION <IOffer> : representerar ett utbud av tjänster som ett abonnemang kan skapas för.</span><span class="sxs-lookup"><span data-stu-id="f986d-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="f986d-166">`[Location <String>]`: Resursens plats</span><span class="sxs-lookup"><span data-stu-id="f986d-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="f986d-167">`[AddonPlans <IAddonPlanDefinition[]>]`: Referenser till tilläggs planer som en innehavare kan skaffa som en del av ett utbud.</span><span class="sxs-lookup"><span data-stu-id="f986d-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="f986d-168">`[MaxAcquisitionCount <Int32?>]`: Maximalt antal instanser som kan erhållas av en enda prenumeration.</span><span class="sxs-lookup"><span data-stu-id="f986d-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="f986d-169">Om det inte anges är det förmodade värdet 1.</span><span class="sxs-lookup"><span data-stu-id="f986d-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="f986d-170">`[PlanId <String>]`: Plan-ID.</span><span class="sxs-lookup"><span data-stu-id="f986d-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="f986d-171">`[BasePlanIds <String[]>]`: Identifierare för de grundläggande abonnemang som blir tillgängliga för klient organisationen omedelbart när en klient organisation abonnerar på ett bud.</span><span class="sxs-lookup"><span data-stu-id="f986d-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="f986d-172">`[Description <String>]`: Beskrivning av bud.</span><span class="sxs-lookup"><span data-stu-id="f986d-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="f986d-173">`[DisplayName <String>]`: Visnings namn för bud.</span><span class="sxs-lookup"><span data-stu-id="f986d-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="f986d-174">`[ExternalReferenceId <String>]`: Identifierare för extern referens.</span><span class="sxs-lookup"><span data-stu-id="f986d-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="f986d-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Högsta antal prenumerationer per konto.</span><span class="sxs-lookup"><span data-stu-id="f986d-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="f986d-176">`[PropertiesName <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="f986d-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="f986d-177">`[State <AccessibilityState?>]`: Ge hjälpmedels status.</span><span class="sxs-lookup"><span data-stu-id="f986d-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="f986d-178">`[SubscriptionCount <Int32?>]`: Aktuellt antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="f986d-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="f986d-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f986d-179">RELATED LINKS</span></span>

