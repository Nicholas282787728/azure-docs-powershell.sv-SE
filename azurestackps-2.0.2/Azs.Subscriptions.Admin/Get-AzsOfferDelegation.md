---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 995d7296ef1e5b6f846d5343fd072909a877b1ec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100079"
---
# <span data-ttu-id="51df6-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="51df6-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="51df6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51df6-102">SYNOPSIS</span></span>
<span data-ttu-id="51df6-103">Skaffa den angivna offerts-delegeringen.</span><span class="sxs-lookup"><span data-stu-id="51df6-103">Get the specified offer delegation.</span></span>

## <span data-ttu-id="51df6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51df6-104">SYNTAX</span></span>

### <span data-ttu-id="51df6-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="51df6-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51df6-106">Lära</span><span class="sxs-lookup"><span data-stu-id="51df6-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51df6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="51df6-107">GetViaIdentity</span></span>
```
Get-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="51df6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51df6-108">DESCRIPTION</span></span>
<span data-ttu-id="51df6-109">Skaffa den angivna offerts-delegeringen.</span><span class="sxs-lookup"><span data-stu-id="51df6-109">Get the specified offer delegation.</span></span>

## <span data-ttu-id="51df6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51df6-110">EXAMPLES</span></span>

### <span data-ttu-id="51df6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51df6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferDelegation -OfferName "delegatedoffer" -ResourceGroupName "testrg"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/delegatedoffer/offerDelegations/offerdelegation
Location       : redmond
Name           : delegatedoffer/offerdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cbb018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="51df6-112">Hämta listan med ombud.</span><span class="sxs-lookup"><span data-stu-id="51df6-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="51df6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51df6-113">PARAMETERS</span></span>

### <span data-ttu-id="51df6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51df6-114">-DefaultProfile</span></span>
<span data-ttu-id="51df6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51df6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51df6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51df6-116">-InputObject</span></span>
<span data-ttu-id="51df6-117">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="51df6-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="51df6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="51df6-118">-Name</span></span>
<span data-ttu-id="51df6-119">Namn på en ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="51df6-119">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51df6-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="51df6-120">-OfferName</span></span>
<span data-ttu-id="51df6-121">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="51df6-121">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51df6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51df6-122">-ResourceGroupName</span></span>
<span data-ttu-id="51df6-123">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="51df6-123">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51df6-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51df6-124">-SubscriptionId</span></span>
<span data-ttu-id="51df6-125">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="51df6-125">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51df6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51df6-126">CommonParameters</span></span>
<span data-ttu-id="51df6-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51df6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51df6-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51df6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51df6-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51df6-129">INPUTS</span></span>

### <span data-ttu-id="51df6-130">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="51df6-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="51df6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51df6-131">OUTPUTS</span></span>

### <span data-ttu-id="51df6-132">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="51df6-132">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="51df6-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="51df6-133">ALIASES</span></span>

## <span data-ttu-id="51df6-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51df6-134">NOTES</span></span>

<span data-ttu-id="51df6-135">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="51df6-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51df6-136">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="51df6-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="51df6-137">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="51df6-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51df6-138">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="51df6-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="51df6-139">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="51df6-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="51df6-140">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="51df6-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51df6-141">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="51df6-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="51df6-142">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="51df6-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="51df6-143">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="51df6-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="51df6-144">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="51df6-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="51df6-145">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="51df6-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="51df6-146">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="51df6-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="51df6-147">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="51df6-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="51df6-148">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="51df6-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="51df6-149">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="51df6-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="51df6-150">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="51df6-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="51df6-151">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="51df6-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="51df6-152">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="51df6-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="51df6-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51df6-153">RELATED LINKS</span></span>

