---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: a36406499be15c53e9bfabd8aa9abf56b2afa1c7
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092874"
---
# <span data-ttu-id="0a6a0-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="0a6a0-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="0a6a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a6a0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6a0-103">Skaffa ett angivet abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-103">Get a specified subscription.</span></span>

## <span data-ttu-id="0a6a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a6a0-104">SYNTAX</span></span>

### <span data-ttu-id="0a6a0-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="0a6a0-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a6a0-106">Lära</span><span class="sxs-lookup"><span data-stu-id="0a6a0-106">Get</span></span>
```
Get-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0a6a0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0a6a0-107">GetViaIdentity</span></span>
```
Get-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a6a0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a6a0-108">DESCRIPTION</span></span>
<span data-ttu-id="0a6a0-109">Skaffa ett angivet abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-109">Get a specified subscription.</span></span>

## <span data-ttu-id="0a6a0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a6a0-110">EXAMPLES</span></span>

### <span data-ttu-id="0a6a0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0a6a0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsUserSubscription | Select-Object -First 1 | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : DRPTestffbffbe5-test-test-test-test-test-test
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="0a6a0-112">Hämta listan med användar abonnemang som operator.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-112">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="0a6a0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a6a0-113">PARAMETERS</span></span>

### <span data-ttu-id="0a6a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6a0-114">-DefaultProfile</span></span>
<span data-ttu-id="0a6a0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a6a0-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="0a6a0-116">-Filter</span></span>
<span data-ttu-id="0a6a0-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0a6a0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a6a0-118">-InputObject</span></span>
<span data-ttu-id="0a6a0-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0a6a0-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a6a0-120">-SubscriptionId</span></span>
<span data-ttu-id="0a6a0-121">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0a6a0-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a6a0-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="0a6a0-123">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="0a6a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6a0-124">CommonParameters</span></span>
<span data-ttu-id="0a6a0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6a0-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a6a0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6a0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a6a0-127">INPUTS</span></span>

### <span data-ttu-id="0a6a0-128">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0a6a0-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="0a6a0-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a6a0-129">OUTPUTS</span></span>

### <span data-ttu-id="0a6a0-130">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="0a6a0-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="0a6a0-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0a6a0-131">ALIASES</span></span>

## <span data-ttu-id="0a6a0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a6a0-132">NOTES</span></span>

<span data-ttu-id="0a6a0-133">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a6a0-134">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0a6a0-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0a6a0-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0a6a0-136">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="0a6a0-137">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="0a6a0-138">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0a6a0-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a6a0-139">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="0a6a0-140">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="0a6a0-141">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="0a6a0-142">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="0a6a0-143">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="0a6a0-144">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="0a6a0-145">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="0a6a0-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="0a6a0-146">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="0a6a0-147">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="0a6a0-148">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0a6a0-149">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="0a6a0-150">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="0a6a0-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="0a6a0-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a6a0-151">RELATED LINKS</span></span>

