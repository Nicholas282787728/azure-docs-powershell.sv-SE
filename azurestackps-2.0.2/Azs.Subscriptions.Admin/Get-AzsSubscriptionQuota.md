---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azssubscriptionquota
schema: 2.0.0
ms.openlocfilehash: 8e1c03393c1d276f5c93425250bf7202e49022d8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100295"
---
# <span data-ttu-id="9747e-101">Get-AzsSubscriptionQuota</span><span class="sxs-lookup"><span data-stu-id="9747e-101">Get-AzsSubscriptionQuota</span></span>

## <span data-ttu-id="9747e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9747e-102">SYNOPSIS</span></span>
<span data-ttu-id="9747e-103">Hämtar en kvot med namn.</span><span class="sxs-lookup"><span data-stu-id="9747e-103">Gets a quota by name.</span></span>

## <span data-ttu-id="9747e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9747e-104">SYNTAX</span></span>

### <span data-ttu-id="9747e-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="9747e-105">List (Default)</span></span>
```
Get-AzsSubscriptionQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9747e-106">Lära</span><span class="sxs-lookup"><span data-stu-id="9747e-106">Get</span></span>
```
Get-AzsSubscriptionQuota -Quota <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9747e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9747e-107">GetViaIdentity</span></span>
```
Get-AzsSubscriptionQuota -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9747e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9747e-108">DESCRIPTION</span></span>
<span data-ttu-id="9747e-109">Hämtar en kvot med namn.</span><span class="sxs-lookup"><span data-stu-id="9747e-109">Gets a quota by name.</span></span>

## <span data-ttu-id="9747e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9747e-110">EXAMPLES</span></span>

### <span data-ttu-id="9747e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9747e-111">Example 1</span></span>
```powershell

```

<span data-ttu-id="9747e-112">Hämta listan med abonnemangs resurs leverantörs kvoter.</span><span class="sxs-lookup"><span data-stu-id="9747e-112">Get the list of subscription resource provider quotas.</span></span>

## <span data-ttu-id="9747e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9747e-113">PARAMETERS</span></span>

### <span data-ttu-id="9747e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9747e-114">-DefaultProfile</span></span>
<span data-ttu-id="9747e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9747e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9747e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9747e-116">-InputObject</span></span>
<span data-ttu-id="9747e-117">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9747e-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9747e-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="9747e-118">-Location</span></span>
<span data-ttu-id="9747e-119">AzureStack-platsen.</span><span class="sxs-lookup"><span data-stu-id="9747e-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9747e-120">-Kvot</span><span class="sxs-lookup"><span data-stu-id="9747e-120">-Quota</span></span>
<span data-ttu-id="9747e-121">Namn på kvoten.</span><span class="sxs-lookup"><span data-stu-id="9747e-121">Name of the quota.</span></span>

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

### <span data-ttu-id="9747e-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9747e-122">-SubscriptionId</span></span>
<span data-ttu-id="9747e-123">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9747e-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9747e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9747e-124">CommonParameters</span></span>
<span data-ttu-id="9747e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9747e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9747e-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9747e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9747e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9747e-127">INPUTS</span></span>

### <span data-ttu-id="9747e-128">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9747e-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="9747e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9747e-129">OUTPUTS</span></span>

### <span data-ttu-id="9747e-130">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IQuota</span><span class="sxs-lookup"><span data-stu-id="9747e-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IQuota</span></span>

<span data-ttu-id="9747e-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9747e-131">ALIASES</span></span>

<span data-ttu-id="9747e-132">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="9747e-132">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="9747e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9747e-133">NOTES</span></span>

<span data-ttu-id="9747e-134">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9747e-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9747e-135">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9747e-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9747e-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="9747e-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9747e-137">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="9747e-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="9747e-138">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="9747e-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="9747e-139">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9747e-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9747e-140">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="9747e-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="9747e-141">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="9747e-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="9747e-142">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="9747e-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="9747e-143">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="9747e-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="9747e-144">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="9747e-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="9747e-145">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9747e-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="9747e-146">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="9747e-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="9747e-147">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="9747e-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9747e-148">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="9747e-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="9747e-149">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9747e-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9747e-150">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9747e-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="9747e-151">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="9747e-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="9747e-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9747e-152">RELATED LINKS</span></span>

