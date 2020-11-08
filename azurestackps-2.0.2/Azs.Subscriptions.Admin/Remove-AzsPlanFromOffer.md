---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplanfromoffer
schema: 2.0.0
ms.openlocfilehash: c3a68c028abc9033cef9d9fd7e8fbd39e4066d2d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100156"
---
# <span data-ttu-id="8006d-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="8006d-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="8006d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8006d-102">SYNOPSIS</span></span>
<span data-ttu-id="8006d-103">Koppla bort en plan från ett bud.</span><span class="sxs-lookup"><span data-stu-id="8006d-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="8006d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8006d-104">SYNTAX</span></span>

### <span data-ttu-id="8006d-105">UnlinkExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="8006d-105">UnlinkExpanded (Default)</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8006d-106">Koppla bort</span><span class="sxs-lookup"><span data-stu-id="8006d-106">Unlink</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8006d-107">UnlinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8006d-107">UnlinkViaIdentity</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8006d-108">UnlinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8006d-108">UnlinkViaIdentityExpanded</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8006d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8006d-109">DESCRIPTION</span></span>
<span data-ttu-id="8006d-110">Koppla bort en plan från ett bud.</span><span class="sxs-lookup"><span data-stu-id="8006d-110">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="8006d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8006d-111">EXAMPLES</span></span>

### <span data-ttu-id="8006d-112">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="8006d-112">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsPlanFromOffer -PlanName "testplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="8006d-113">Koppla bort en plan från ett bud.</span><span class="sxs-lookup"><span data-stu-id="8006d-113">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="8006d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8006d-114">PARAMETERS</span></span>

### <span data-ttu-id="8006d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8006d-115">-DefaultProfile</span></span>
<span data-ttu-id="8006d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8006d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8006d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8006d-117">-InputObject</span></span>
<span data-ttu-id="8006d-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8006d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: UnlinkViaIdentity, UnlinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8006d-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="8006d-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="8006d-120">Maximalt antal köp via abonnenter</span><span class="sxs-lookup"><span data-stu-id="8006d-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8006d-121">-OfferName</span><span class="sxs-lookup"><span data-stu-id="8006d-121">-OfferName</span></span>
<span data-ttu-id="8006d-122">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="8006d-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8006d-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="8006d-123">-PlanLink</span></span>
<span data-ttu-id="8006d-124">Definition för att länka och ta bort länkar till erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="8006d-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="8006d-125">För att konstruera kan du läsa avsnittet anteckningar för PLANLINK-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8006d-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Unlink, UnlinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8006d-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="8006d-126">-PlanLinkType</span></span>
<span data-ttu-id="8006d-127">Typ av abonnemangs länk.</span><span class="sxs-lookup"><span data-stu-id="8006d-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8006d-128">-PlanName</span><span class="sxs-lookup"><span data-stu-id="8006d-128">-PlanName</span></span>
<span data-ttu-id="8006d-129">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8006d-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8006d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8006d-130">-ResourceGroupName</span></span>
<span data-ttu-id="8006d-131">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="8006d-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8006d-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8006d-132">-SubscriptionId</span></span>
<span data-ttu-id="8006d-133">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8006d-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8006d-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8006d-134">-Confirm</span></span>
<span data-ttu-id="8006d-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8006d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8006d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8006d-136">-WhatIf</span></span>
<span data-ttu-id="8006d-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8006d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8006d-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8006d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8006d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8006d-139">CommonParameters</span></span>
<span data-ttu-id="8006d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8006d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8006d-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8006d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8006d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8006d-142">INPUTS</span></span>

### <span data-ttu-id="8006d-143">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IPlanLinkDefinition</span><span class="sxs-lookup"><span data-stu-id="8006d-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="8006d-144">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8006d-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="8006d-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8006d-145">OUTPUTS</span></span>

### <span data-ttu-id="8006d-146">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="8006d-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="8006d-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8006d-147">ALIASES</span></span>

## <span data-ttu-id="8006d-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8006d-148">NOTES</span></span>

<span data-ttu-id="8006d-149">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8006d-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8006d-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8006d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8006d-151">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8006d-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8006d-152">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="8006d-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="8006d-153">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="8006d-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="8006d-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8006d-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8006d-155">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="8006d-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="8006d-156">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="8006d-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="8006d-157">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="8006d-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="8006d-158">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="8006d-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="8006d-159">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="8006d-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="8006d-160">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8006d-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="8006d-161">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="8006d-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="8006d-162">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="8006d-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="8006d-163">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="8006d-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="8006d-164">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8006d-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8006d-165">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8006d-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="8006d-166">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="8006d-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="8006d-167">PLANLINK <IPlanLinkDefinition> : definition för att länka och ta bort länkar till erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="8006d-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="8006d-168">`[MaxAcquisitionCount <Int32?>]`: Det högsta antalet köp per prenumeranter</span><span class="sxs-lookup"><span data-stu-id="8006d-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="8006d-169">`[PlanLinkType <PlanLinkType?>]`: Typ av abonnemangs länk.</span><span class="sxs-lookup"><span data-stu-id="8006d-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="8006d-170">`[PlanName <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8006d-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="8006d-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8006d-171">RELATED LINKS</span></span>

