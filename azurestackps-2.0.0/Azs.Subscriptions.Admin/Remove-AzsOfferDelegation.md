---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: e9de73f68501071bceb87c115c2c9882fc5ea988
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092841"
---
# <span data-ttu-id="aac97-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="aac97-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="aac97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aac97-102">SYNOPSIS</span></span>
<span data-ttu-id="aac97-103">Ta bort den angivna offer-delegeringen.</span><span class="sxs-lookup"><span data-stu-id="aac97-103">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="aac97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aac97-104">SYNTAX</span></span>

### <span data-ttu-id="aac97-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="aac97-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aac97-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aac97-106">DeleteViaIdentity</span></span>
```
Remove-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aac97-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aac97-107">DESCRIPTION</span></span>
<span data-ttu-id="aac97-108">Ta bort den angivna offer-delegeringen.</span><span class="sxs-lookup"><span data-stu-id="aac97-108">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="aac97-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aac97-109">EXAMPLES</span></span>

### <span data-ttu-id="aac97-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="aac97-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1

{{ Add output here }}
```

<span data-ttu-id="aac97-111">Tar bort alternativet för att ge offerter</span><span class="sxs-lookup"><span data-stu-id="aac97-111">Removes the offer delegation</span></span>

## <span data-ttu-id="aac97-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aac97-112">PARAMETERS</span></span>

### <span data-ttu-id="aac97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac97-113">-DefaultProfile</span></span>
<span data-ttu-id="aac97-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aac97-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aac97-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aac97-115">-InputObject</span></span>
<span data-ttu-id="aac97-116">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="aac97-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="aac97-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="aac97-117">-Name</span></span>
<span data-ttu-id="aac97-118">Namn på en ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="aac97-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aac97-119">-OfferName</span><span class="sxs-lookup"><span data-stu-id="aac97-119">-OfferName</span></span>
<span data-ttu-id="aac97-120">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="aac97-120">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aac97-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aac97-121">-PassThru</span></span>
<span data-ttu-id="aac97-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="aac97-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aac97-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac97-123">-ResourceGroupName</span></span>
<span data-ttu-id="aac97-124">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="aac97-124">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aac97-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aac97-125">-SubscriptionId</span></span>
<span data-ttu-id="aac97-126">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="aac97-126">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aac97-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aac97-127">-Confirm</span></span>
<span data-ttu-id="aac97-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aac97-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aac97-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aac97-129">-WhatIf</span></span>
<span data-ttu-id="aac97-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aac97-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aac97-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aac97-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aac97-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac97-132">CommonParameters</span></span>
<span data-ttu-id="aac97-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac97-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac97-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aac97-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac97-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aac97-135">INPUTS</span></span>

### <span data-ttu-id="aac97-136">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="aac97-136">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="aac97-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aac97-137">OUTPUTS</span></span>

### <span data-ttu-id="aac97-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aac97-138">System.Boolean</span></span>

<span data-ttu-id="aac97-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="aac97-139">ALIASES</span></span>

## <span data-ttu-id="aac97-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aac97-140">NOTES</span></span>

<span data-ttu-id="aac97-141">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="aac97-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aac97-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aac97-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="aac97-143">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="aac97-143">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aac97-144">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="aac97-144">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="aac97-145">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="aac97-145">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="aac97-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="aac97-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aac97-147">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="aac97-147">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="aac97-148">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="aac97-148">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="aac97-149">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="aac97-149">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="aac97-150">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="aac97-150">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="aac97-151">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="aac97-151">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="aac97-152">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="aac97-152">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="aac97-153">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="aac97-153">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="aac97-154">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="aac97-154">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="aac97-155">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="aac97-155">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="aac97-156">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="aac97-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="aac97-157">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="aac97-157">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="aac97-158">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="aac97-158">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="aac97-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aac97-159">RELATED LINKS</span></span>

