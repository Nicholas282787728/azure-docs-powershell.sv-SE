---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: c73a4c4bcc482b7e6e1281d0bc4ee6c29921b745
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092870"
---
# <span data-ttu-id="7b034-101">Get-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="7b034-101">Get-AzsAcquiredPlan</span></span>

## <span data-ttu-id="7b034-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b034-102">SYNOPSIS</span></span>
<span data-ttu-id="7b034-103">Hämtar det angivna abonnemanget från en prenumeration som tar upp erbjudandet.</span><span class="sxs-lookup"><span data-stu-id="7b034-103">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="7b034-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b034-104">SYNTAX</span></span>

### <span data-ttu-id="7b034-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="7b034-105">List (Default)</span></span>
```
Get-AzsAcquiredPlan -TargetSubscriptionId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b034-106">Lära</span><span class="sxs-lookup"><span data-stu-id="7b034-106">Get</span></span>
```
Get-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7b034-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7b034-107">GetViaIdentity</span></span>
```
Get-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b034-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b034-108">DESCRIPTION</span></span>
<span data-ttu-id="7b034-109">Hämtar det angivna abonnemanget från en prenumeration som tar upp erbjudandet.</span><span class="sxs-lookup"><span data-stu-id="7b034-109">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="7b034-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b034-110">EXAMPLES</span></span>

### <span data-ttu-id="7b034-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7b034-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsAcquiredPlan -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="7b034-112">Få en samling av alla hämtade abonnemang som abonnemanget har åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="7b034-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="7b034-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b034-113">PARAMETERS</span></span>

### <span data-ttu-id="7b034-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b034-114">-DefaultProfile</span></span>
<span data-ttu-id="7b034-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b034-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b034-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b034-116">-InputObject</span></span>
<span data-ttu-id="7b034-117">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7b034-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7b034-118">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="7b034-118">-PlanAcquisitionId</span></span>
<span data-ttu-id="7b034-119">Abonnemangets anskaffnings identifierare</span><span class="sxs-lookup"><span data-stu-id="7b034-119">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="7b034-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b034-120">-SubscriptionId</span></span>
<span data-ttu-id="7b034-121">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7b034-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7b034-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b034-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="7b034-123">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7b034-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="7b034-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b034-124">CommonParameters</span></span>
<span data-ttu-id="7b034-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b034-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b034-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b034-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b034-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b034-127">INPUTS</span></span>

### <span data-ttu-id="7b034-128">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7b034-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="7b034-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b034-129">OUTPUTS</span></span>

### <span data-ttu-id="7b034-130">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="7b034-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="7b034-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7b034-131">ALIASES</span></span>

<span data-ttu-id="7b034-132">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="7b034-132">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="7b034-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b034-133">NOTES</span></span>

<span data-ttu-id="7b034-134">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7b034-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b034-135">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7b034-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7b034-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="7b034-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7b034-137">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="7b034-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="7b034-138">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="7b034-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="7b034-139">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="7b034-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7b034-140">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="7b034-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="7b034-141">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="7b034-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="7b034-142">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="7b034-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="7b034-143">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="7b034-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="7b034-144">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="7b034-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="7b034-145">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7b034-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="7b034-146">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="7b034-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="7b034-147">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="7b034-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="7b034-148">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="7b034-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="7b034-149">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7b034-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7b034-150">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7b034-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="7b034-151">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="7b034-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="7b034-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b034-152">RELATED LINKS</span></span>

