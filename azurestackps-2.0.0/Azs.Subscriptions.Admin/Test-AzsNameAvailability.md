---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsnameavailability
schema: 2.0.0
ms.openlocfilehash: d92c2558375a180c96ff20260977bdb38908fa61
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092824"
---
# <span data-ttu-id="25017-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="25017-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="25017-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25017-102">SYNOPSIS</span></span>
<span data-ttu-id="25017-103">Hämta listan med prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="25017-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="25017-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25017-104">SYNTAX</span></span>

### <span data-ttu-id="25017-105">CheckExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="25017-105">CheckExpanded (Default)</span></span>
```
Test-AzsNameAvailability [-SubscriptionId <String>] [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25017-106">Igen</span><span class="sxs-lookup"><span data-stu-id="25017-106">Check</span></span>
```
Test-AzsNameAvailability -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25017-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25017-107">CheckViaIdentity</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity>
 -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25017-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="25017-108">CheckViaIdentityExpanded</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity> [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25017-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25017-109">DESCRIPTION</span></span>
<span data-ttu-id="25017-110">Hämta listan med prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="25017-110">Get the list of subscriptions.</span></span>

## <span data-ttu-id="25017-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25017-111">EXAMPLES</span></span>

### <span data-ttu-id="25017-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25017-112">Example 1</span></span>
```powershell
PS C:\> Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name "testoffer" | fl *

Message       : A resource of type 'Microsoft.Subscriptions.Admin/offers' with name 'testoffer' already exists. Please select a different name.
NameAvailable : False
Reason        : AlreadyExists
```

<span data-ttu-id="25017-113">Returnerar tillgänglighet för den angivna resurs typen för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="25017-113">Returns the availability of the specified subscription resource type and name</span></span>

## <span data-ttu-id="25017-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25017-114">PARAMETERS</span></span>

### <span data-ttu-id="25017-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25017-115">-DefaultProfile</span></span>
<span data-ttu-id="25017-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25017-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25017-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25017-117">-InputObject</span></span>
<span data-ttu-id="25017-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="25017-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="25017-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="25017-119">-Name</span></span>
<span data-ttu-id="25017-120">Resurs namn som ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="25017-120">The resource name to verify.</span></span>

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

### <span data-ttu-id="25017-121">-NameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="25017-121">-NameAvailabilityDefinition</span></span>
<span data-ttu-id="25017-122">Åtgärds definitionen kontrol lera namn tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="25017-122">The check name availability action definition.</span></span>
<span data-ttu-id="25017-123">För att konstruera kan du läsa avsnittet anteckningar för NAMEAVAILABILITYDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="25017-123">To construct, see NOTES section for NAMEAVAILABILITYDEFINITION properties and create a hash table.</span></span>

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

### <span data-ttu-id="25017-124">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="25017-124">-ResourceType</span></span>
<span data-ttu-id="25017-125">Resurs typen för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="25017-125">The resource type to verify.</span></span>

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

### <span data-ttu-id="25017-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25017-126">-SubscriptionId</span></span>
<span data-ttu-id="25017-127">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="25017-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="25017-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="25017-128">-Confirm</span></span>
<span data-ttu-id="25017-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="25017-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25017-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25017-130">-WhatIf</span></span>
<span data-ttu-id="25017-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="25017-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25017-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="25017-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25017-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25017-133">CommonParameters</span></span>
<span data-ttu-id="25017-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25017-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25017-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25017-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25017-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25017-136">INPUTS</span></span>

### <span data-ttu-id="25017-137">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="25017-137">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition</span></span>

### <span data-ttu-id="25017-138">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="25017-138">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="25017-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25017-139">OUTPUTS</span></span>

### <span data-ttu-id="25017-140">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="25017-140">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityResponse</span></span>

<span data-ttu-id="25017-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="25017-141">ALIASES</span></span>

## <span data-ttu-id="25017-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25017-142">NOTES</span></span>

<span data-ttu-id="25017-143">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="25017-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25017-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="25017-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="25017-145">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="25017-145">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25017-146">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="25017-146">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="25017-147">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="25017-147">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="25017-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="25017-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25017-149">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="25017-149">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="25017-150">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="25017-150">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="25017-151">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="25017-151">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="25017-152">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="25017-152">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="25017-153">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="25017-153">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="25017-154">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="25017-154">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="25017-155">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="25017-155">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="25017-156">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="25017-156">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="25017-157">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="25017-157">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="25017-158">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="25017-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="25017-159">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="25017-159">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="25017-160">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="25017-160">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="25017-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition> : åtgärds definitionen kontrol lera namn tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="25017-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition>: The check name availability action definition.</span></span>
  - <span data-ttu-id="25017-162">`[Name <String>]`: Resurs namnet som ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="25017-162">`[Name <String>]`: The resource name to verify.</span></span>
  - <span data-ttu-id="25017-163">`[ResourceType <String>]`: Resurs typen som ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="25017-163">`[ResourceType <String>]`: The resource type to verify.</span></span>

## <span data-ttu-id="25017-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25017-164">RELATED LINKS</span></span>

