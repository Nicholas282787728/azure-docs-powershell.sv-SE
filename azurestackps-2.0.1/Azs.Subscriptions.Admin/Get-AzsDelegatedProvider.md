---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovider
schema: 2.0.0
ms.openlocfilehash: 2c6c87ce0b40fae228756d4a9dd452b49ce1aad2
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092884"
---
# <span data-ttu-id="db6f5-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="db6f5-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="db6f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db6f5-102">SYNOPSIS</span></span>
<span data-ttu-id="db6f5-103">Hämta den angivna delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="db6f5-103">Get the specified delegated provider.</span></span>

## <span data-ttu-id="db6f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db6f5-104">SYNTAX</span></span>

### <span data-ttu-id="db6f5-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="db6f5-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="db6f5-106">Lära</span><span class="sxs-lookup"><span data-stu-id="db6f5-106">Get</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="db6f5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="db6f5-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProvider -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="db6f5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db6f5-108">DESCRIPTION</span></span>
<span data-ttu-id="db6f5-109">Hämta den angivna delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="db6f5-109">Get the specified delegated provider.</span></span>

## <span data-ttu-id="db6f5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db6f5-110">EXAMPLES</span></span>

### <span data-ttu-id="db6f5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="db6f5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProvider -DelegatedProviderId "ed3e275b-87d1-4e94-9962-b3700287bdbc" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : cnur4866tenantresellersubscription843
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/cnur4866resellersubscrrg843/providers/Microsoft.Subscriptions.Admin/offers/cnur4866tenantsubsvcoffe
                                  r843
Owner                           : tenantadmin1@msazurestack.onmicrosoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="db6f5-112">Skaffa en specifik delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="db6f5-112">Get a specific delegated provider.</span></span>

## <span data-ttu-id="db6f5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db6f5-113">PARAMETERS</span></span>

### <span data-ttu-id="db6f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6f5-114">-DefaultProfile</span></span>
<span data-ttu-id="db6f5-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db6f5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db6f5-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="db6f5-116">-DelegatedProviderId</span></span>
<span data-ttu-id="db6f5-117">DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="db6f5-117">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="db6f5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db6f5-118">-InputObject</span></span>
<span data-ttu-id="db6f5-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="db6f5-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="db6f5-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db6f5-120">-SubscriptionId</span></span>
<span data-ttu-id="db6f5-121">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="db6f5-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="db6f5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6f5-122">CommonParameters</span></span>
<span data-ttu-id="db6f5-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6f5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6f5-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db6f5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6f5-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db6f5-125">INPUTS</span></span>

### <span data-ttu-id="db6f5-126">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="db6f5-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="db6f5-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db6f5-127">OUTPUTS</span></span>

### <span data-ttu-id="db6f5-128">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="db6f5-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="db6f5-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="db6f5-129">ALIASES</span></span>

## <span data-ttu-id="db6f5-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db6f5-130">NOTES</span></span>

<span data-ttu-id="db6f5-131">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="db6f5-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db6f5-132">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db6f5-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="db6f5-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="db6f5-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db6f5-134">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="db6f5-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="db6f5-135">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="db6f5-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="db6f5-136">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="db6f5-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db6f5-137">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="db6f5-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="db6f5-138">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="db6f5-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="db6f5-139">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="db6f5-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="db6f5-140">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="db6f5-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="db6f5-141">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="db6f5-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="db6f5-142">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="db6f5-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="db6f5-143">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="db6f5-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="db6f5-144">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="db6f5-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="db6f5-145">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="db6f5-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="db6f5-146">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="db6f5-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="db6f5-147">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="db6f5-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="db6f5-148">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="db6f5-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="db6f5-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db6f5-149">RELATED LINKS</span></span>

