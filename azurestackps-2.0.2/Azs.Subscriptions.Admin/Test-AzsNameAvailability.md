---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsnameavailability
schema: 2.0.0
ms.openlocfilehash: d92c2558375a180c96ff20260977bdb38908fa61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100374"
---
# <span data-ttu-id="54b10-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="54b10-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="54b10-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54b10-102">SYNOPSIS</span></span>
<span data-ttu-id="54b10-103">Hämta listan med prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="54b10-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="54b10-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54b10-104">SYNTAX</span></span>

### <span data-ttu-id="54b10-105">CheckExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="54b10-105">CheckExpanded (Default)</span></span>
```
Test-AzsNameAvailability [-SubscriptionId <String>] [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="54b10-106">Igen</span><span class="sxs-lookup"><span data-stu-id="54b10-106">Check</span></span>
```
Test-AzsNameAvailability -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="54b10-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="54b10-107">CheckViaIdentity</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity>
 -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="54b10-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="54b10-108">CheckViaIdentityExpanded</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity> [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54b10-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54b10-109">DESCRIPTION</span></span>
<span data-ttu-id="54b10-110">Hämta listan med prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="54b10-110">Get the list of subscriptions.</span></span>

## <span data-ttu-id="54b10-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54b10-111">EXAMPLES</span></span>

### <span data-ttu-id="54b10-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54b10-112">Example 1</span></span>
```powershell
PS C:\> Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name "testoffer" | fl *

Message       : A resource of type 'Microsoft.Subscriptions.Admin/offers' with name 'testoffer' already exists. Please select a different name.
NameAvailable : False
Reason        : AlreadyExists
```

<span data-ttu-id="54b10-113">Returnerar tillgänglighet för den angivna resurs typen för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="54b10-113">Returns the availability of the specified subscription resource type and name</span></span>

## <span data-ttu-id="54b10-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54b10-114">PARAMETERS</span></span>

### <span data-ttu-id="54b10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b10-115">-DefaultProfile</span></span>
<span data-ttu-id="54b10-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54b10-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54b10-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54b10-117">-InputObject</span></span>
<span data-ttu-id="54b10-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="54b10-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="54b10-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="54b10-119">-Name</span></span>
<span data-ttu-id="54b10-120">Resurs namn som ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="54b10-120">The resource name to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="54b10-121">-NameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="54b10-121">-NameAvailabilityDefinition</span></span>
<span data-ttu-id="54b10-122">Åtgärds definitionen kontrol lera namn tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="54b10-122">The check name availability action definition.</span></span>
<span data-ttu-id="54b10-123">För att konstruera kan du läsa avsnittet anteckningar för NAMEAVAILABILITYDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="54b10-123">To construct, see NOTES section for NAMEAVAILABILITYDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="54b10-124">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="54b10-124">-ResourceType</span></span>
<span data-ttu-id="54b10-125">Resurs typen för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="54b10-125">The resource type to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="54b10-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54b10-126">-SubscriptionId</span></span>
<span data-ttu-id="54b10-127">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="54b10-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="54b10-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54b10-128">-Confirm</span></span>
<span data-ttu-id="54b10-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54b10-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54b10-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54b10-130">-WhatIf</span></span>
<span data-ttu-id="54b10-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54b10-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54b10-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54b10-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54b10-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b10-133">CommonParameters</span></span>
<span data-ttu-id="54b10-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54b10-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b10-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54b10-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b10-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54b10-136">INPUTS</span></span>

### <span data-ttu-id="54b10-137">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="54b10-137">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition</span></span>

### <span data-ttu-id="54b10-138">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="54b10-138">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="54b10-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54b10-139">OUTPUTS</span></span>

### <span data-ttu-id="54b10-140">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="54b10-140">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityResponse</span></span>

<span data-ttu-id="54b10-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="54b10-141">ALIASES</span></span>

## <span data-ttu-id="54b10-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54b10-142">NOTES</span></span>

<span data-ttu-id="54b10-143">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="54b10-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54b10-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="54b10-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="54b10-145">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="54b10-145">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="54b10-146">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="54b10-146">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="54b10-147">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="54b10-147">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="54b10-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="54b10-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="54b10-149">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="54b10-149">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="54b10-150">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="54b10-150">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="54b10-151">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="54b10-151">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="54b10-152">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="54b10-152">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="54b10-153">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="54b10-153">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="54b10-154">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="54b10-154">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="54b10-155">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="54b10-155">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="54b10-156">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="54b10-156">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="54b10-157">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="54b10-157">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="54b10-158">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="54b10-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="54b10-159">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="54b10-159">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="54b10-160">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="54b10-160">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="54b10-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition> : åtgärds definitionen kontrol lera namn tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="54b10-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition>: The check name availability action definition.</span></span>
  - <span data-ttu-id="54b10-162">`[Name <String>]`: Resurs namnet som ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="54b10-162">`[Name <String>]`: The resource name to verify.</span></span>
  - <span data-ttu-id="54b10-163">`[ResourceType <String>]`: Resurs typen som ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="54b10-163">`[ResourceType <String>]`: The resource type to verify.</span></span>

## <span data-ttu-id="54b10-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54b10-164">RELATED LINKS</span></span>

