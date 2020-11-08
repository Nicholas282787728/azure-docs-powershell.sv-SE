---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdirectorytenant
schema: 2.0.0
ms.openlocfilehash: f516562b6bc4a136c64a15fa1f128cd1bda502d9
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092858"
---
# <span data-ttu-id="31e15-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="31e15-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="31e15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31e15-102">SYNOPSIS</span></span>
<span data-ttu-id="31e15-103">Skaffa en katalog klient organisation via namn.</span><span class="sxs-lookup"><span data-stu-id="31e15-103">Get a directory tenant by name.</span></span>

## <span data-ttu-id="31e15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31e15-104">SYNTAX</span></span>

### <span data-ttu-id="31e15-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="31e15-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="31e15-106">Lära</span><span class="sxs-lookup"><span data-stu-id="31e15-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="31e15-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="31e15-107">GetViaIdentity</span></span>
```
Get-AzsDirectoryTenant -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="31e15-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31e15-108">DESCRIPTION</span></span>
<span data-ttu-id="31e15-109">Skaffa en katalog klient organisation via namn.</span><span class="sxs-lookup"><span data-stu-id="31e15-109">Get a directory tenant by name.</span></span>

## <span data-ttu-id="31e15-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31e15-110">EXAMPLES</span></span>

### <span data-ttu-id="31e15-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="31e15-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDirectoryTenant -ResourceGroupName 'system.redmond'

Location Name                           Type                                          
-------- ----                           ----                                          
redmond  azurestack01.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
redmond  azurestack02.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
```

<span data-ttu-id="31e15-112">Visar alla katalog innehavare under aktuell prenumeration och angivet resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="31e15-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="31e15-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31e15-113">PARAMETERS</span></span>

### <span data-ttu-id="31e15-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e15-114">-DefaultProfile</span></span>
<span data-ttu-id="31e15-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31e15-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31e15-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31e15-116">-InputObject</span></span>
<span data-ttu-id="31e15-117">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="31e15-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="31e15-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="31e15-118">-Name</span></span>
<span data-ttu-id="31e15-119">Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="31e15-119">Directory tenant name.</span></span>

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

### <span data-ttu-id="31e15-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e15-120">-ResourceGroupName</span></span>
<span data-ttu-id="31e15-121">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="31e15-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="31e15-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31e15-122">-SubscriptionId</span></span>
<span data-ttu-id="31e15-123">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="31e15-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="31e15-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e15-124">CommonParameters</span></span>
<span data-ttu-id="31e15-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e15-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e15-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31e15-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e15-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31e15-127">INPUTS</span></span>

### <span data-ttu-id="31e15-128">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="31e15-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="31e15-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31e15-129">OUTPUTS</span></span>

### <span data-ttu-id="31e15-130">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="31e15-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDirectoryTenant</span></span>

<span data-ttu-id="31e15-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="31e15-131">ALIASES</span></span>

## <span data-ttu-id="31e15-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31e15-132">NOTES</span></span>

<span data-ttu-id="31e15-133">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="31e15-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="31e15-134">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="31e15-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="31e15-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="31e15-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="31e15-136">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="31e15-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="31e15-137">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="31e15-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="31e15-138">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="31e15-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="31e15-139">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="31e15-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="31e15-140">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="31e15-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="31e15-141">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="31e15-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="31e15-142">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="31e15-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="31e15-143">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="31e15-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="31e15-144">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="31e15-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="31e15-145">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="31e15-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="31e15-146">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="31e15-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="31e15-147">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="31e15-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="31e15-148">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="31e15-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="31e15-149">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="31e15-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="31e15-150">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="31e15-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="31e15-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31e15-151">RELATED LINKS</span></span>

