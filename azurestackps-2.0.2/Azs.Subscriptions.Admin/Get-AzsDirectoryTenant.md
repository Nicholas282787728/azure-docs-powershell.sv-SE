---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdirectorytenant
schema: 2.0.0
ms.openlocfilehash: f516562b6bc4a136c64a15fa1f128cd1bda502d9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100104"
---
# <span data-ttu-id="d3d90-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="d3d90-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="d3d90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3d90-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d90-103">Skaffa en katalog klient organisation via namn.</span><span class="sxs-lookup"><span data-stu-id="d3d90-103">Get a directory tenant by name.</span></span>

## <span data-ttu-id="d3d90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3d90-104">SYNTAX</span></span>

### <span data-ttu-id="d3d90-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="d3d90-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3d90-106">Lära</span><span class="sxs-lookup"><span data-stu-id="d3d90-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d3d90-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d3d90-107">GetViaIdentity</span></span>
```
Get-AzsDirectoryTenant -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3d90-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3d90-108">DESCRIPTION</span></span>
<span data-ttu-id="d3d90-109">Skaffa en katalog klient organisation via namn.</span><span class="sxs-lookup"><span data-stu-id="d3d90-109">Get a directory tenant by name.</span></span>

## <span data-ttu-id="d3d90-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3d90-110">EXAMPLES</span></span>

### <span data-ttu-id="d3d90-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d3d90-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDirectoryTenant -ResourceGroupName 'system.redmond'

Location Name                           Type                                          
-------- ----                           ----                                          
redmond  azurestack01.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
redmond  azurestack02.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
```

<span data-ttu-id="d3d90-112">Visar alla katalog innehavare under aktuell prenumeration och angivet resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="d3d90-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="d3d90-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3d90-113">PARAMETERS</span></span>

### <span data-ttu-id="d3d90-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d90-114">-DefaultProfile</span></span>
<span data-ttu-id="d3d90-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d90-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3d90-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3d90-116">-InputObject</span></span>
<span data-ttu-id="d3d90-117">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d3d90-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d3d90-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3d90-118">-Name</span></span>
<span data-ttu-id="d3d90-119">Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="d3d90-119">Directory tenant name.</span></span>

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

### <span data-ttu-id="d3d90-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3d90-120">-ResourceGroupName</span></span>
<span data-ttu-id="d3d90-121">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="d3d90-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d3d90-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3d90-122">-SubscriptionId</span></span>
<span data-ttu-id="d3d90-123">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="d3d90-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d3d90-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d90-124">CommonParameters</span></span>
<span data-ttu-id="d3d90-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d90-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d90-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3d90-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d90-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3d90-127">INPUTS</span></span>

### <span data-ttu-id="d3d90-128">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d3d90-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="d3d90-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3d90-129">OUTPUTS</span></span>

### <span data-ttu-id="d3d90-130">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="d3d90-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDirectoryTenant</span></span>

<span data-ttu-id="d3d90-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d3d90-131">ALIASES</span></span>

## <span data-ttu-id="d3d90-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3d90-132">NOTES</span></span>

<span data-ttu-id="d3d90-133">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="d3d90-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d3d90-134">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d3d90-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d3d90-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d3d90-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d3d90-136">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="d3d90-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="d3d90-137">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="d3d90-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="d3d90-138">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d3d90-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d3d90-139">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="d3d90-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="d3d90-140">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="d3d90-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="d3d90-141">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="d3d90-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="d3d90-142">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="d3d90-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="d3d90-143">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="d3d90-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="d3d90-144">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d3d90-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="d3d90-145">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="d3d90-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="d3d90-146">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="d3d90-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d3d90-147">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="d3d90-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="d3d90-148">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="d3d90-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d3d90-149">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d3d90-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="d3d90-150">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="d3d90-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="d3d90-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3d90-151">RELATED LINKS</span></span>

