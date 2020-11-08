---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsadminmanagedoffer
schema: 2.0.0
ms.openlocfilehash: 79cac7a530a9aedc1e53120b29eb2dd8cb73489b
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092867"
---
# <span data-ttu-id="e88aa-101">Get-AzsAdminManagedOffer</span><span class="sxs-lookup"><span data-stu-id="e88aa-101">Get-AzsAdminManagedOffer</span></span>

## <span data-ttu-id="e88aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e88aa-102">SYNOPSIS</span></span>
<span data-ttu-id="e88aa-103">Skaffa det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="e88aa-103">Get the specified offer.</span></span>

## <span data-ttu-id="e88aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e88aa-104">SYNTAX</span></span>

### <span data-ttu-id="e88aa-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="e88aa-105">List (Default)</span></span>
```
Get-AzsAdminManagedOffer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e88aa-106">Lära</span><span class="sxs-lookup"><span data-stu-id="e88aa-106">Get</span></span>
```
Get-AzsAdminManagedOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e88aa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e88aa-107">GetViaIdentity</span></span>
```
Get-AzsAdminManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e88aa-108">List1</span><span class="sxs-lookup"><span data-stu-id="e88aa-108">List1</span></span>
```
Get-AzsAdminManagedOffer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e88aa-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e88aa-109">DESCRIPTION</span></span>
<span data-ttu-id="e88aa-110">Skaffa det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="e88aa-110">Get the specified offer.</span></span>

## <span data-ttu-id="e88aa-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e88aa-111">EXAMPLES</span></span>

### <span data-ttu-id="e88aa-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e88aa-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsAdminManagedOffer -Name "testoffer" -ResourceGroupName "testrg"

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="e88aa-113">Skaffa bud via namn och ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88aa-113">Get offer by Name and ResourceGroupName</span></span>

## <span data-ttu-id="e88aa-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e88aa-114">PARAMETERS</span></span>

### <span data-ttu-id="e88aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88aa-115">-DefaultProfile</span></span>
<span data-ttu-id="e88aa-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e88aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e88aa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e88aa-117">-InputObject</span></span>
<span data-ttu-id="e88aa-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e88aa-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e88aa-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e88aa-119">-Name</span></span>
<span data-ttu-id="e88aa-120">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="e88aa-120">Name of an offer.</span></span>

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

### <span data-ttu-id="e88aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="e88aa-122">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="e88aa-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e88aa-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e88aa-123">-SubscriptionId</span></span>
<span data-ttu-id="e88aa-124">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e88aa-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e88aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88aa-125">CommonParameters</span></span>
<span data-ttu-id="e88aa-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e88aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88aa-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e88aa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88aa-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e88aa-128">INPUTS</span></span>

### <span data-ttu-id="e88aa-129">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e88aa-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="e88aa-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e88aa-130">OUTPUTS</span></span>

### <span data-ttu-id="e88aa-131">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="e88aa-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="e88aa-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e88aa-132">ALIASES</span></span>

<span data-ttu-id="e88aa-133">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="e88aa-133">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="e88aa-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e88aa-134">NOTES</span></span>

<span data-ttu-id="e88aa-135">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e88aa-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e88aa-136">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e88aa-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e88aa-137">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e88aa-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e88aa-138">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="e88aa-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="e88aa-139">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="e88aa-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="e88aa-140">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e88aa-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e88aa-141">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="e88aa-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="e88aa-142">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="e88aa-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="e88aa-143">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="e88aa-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="e88aa-144">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="e88aa-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="e88aa-145">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="e88aa-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="e88aa-146">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e88aa-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="e88aa-147">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="e88aa-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="e88aa-148">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="e88aa-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e88aa-149">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="e88aa-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="e88aa-150">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e88aa-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e88aa-151">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e88aa-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="e88aa-152">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="e88aa-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="e88aa-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e88aa-153">RELATED LINKS</span></span>

