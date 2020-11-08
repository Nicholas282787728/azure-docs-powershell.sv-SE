---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplan
schema: 2.0.0
ms.openlocfilehash: 4aa59d41bc13d79e487465a6a0721ec19ed68bb8
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092812"
---
# <span data-ttu-id="3e306-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="3e306-101">Get-AzsPlan</span></span>

## <span data-ttu-id="3e306-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e306-102">SYNOPSIS</span></span>
<span data-ttu-id="3e306-103">Skaffa det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3e306-103">Get the specified plan.</span></span>

## <span data-ttu-id="3e306-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e306-104">SYNTAX</span></span>

### <span data-ttu-id="3e306-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="3e306-105">List (Default)</span></span>
```
Get-AzsPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e306-106">Lära</span><span class="sxs-lookup"><span data-stu-id="3e306-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e306-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3e306-107">GetViaIdentity</span></span>
```
Get-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e306-108">List1</span><span class="sxs-lookup"><span data-stu-id="3e306-108">List1</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e306-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e306-109">DESCRIPTION</span></span>
<span data-ttu-id="3e306-110">Skaffa det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3e306-110">Get the specified plan.</span></span>

## <span data-ttu-id="3e306-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e306-111">EXAMPLES</span></span>

### <span data-ttu-id="3e306-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e306-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 1
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="3e306-113">Skaffa ett specifik abonnemang under dessa abonnemang.</span><span class="sxs-lookup"><span data-stu-id="3e306-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="3e306-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e306-114">PARAMETERS</span></span>

### <span data-ttu-id="3e306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e306-115">-DefaultProfile</span></span>
<span data-ttu-id="3e306-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e306-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e306-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e306-117">-InputObject</span></span>
<span data-ttu-id="3e306-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3e306-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3e306-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e306-119">-Name</span></span>
<span data-ttu-id="3e306-120">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3e306-120">Name of the plan.</span></span>

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

### <span data-ttu-id="3e306-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e306-121">-ResourceGroupName</span></span>
<span data-ttu-id="3e306-122">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="3e306-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3e306-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e306-123">-SubscriptionId</span></span>
<span data-ttu-id="3e306-124">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3e306-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3e306-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e306-125">CommonParameters</span></span>
<span data-ttu-id="3e306-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e306-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e306-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e306-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e306-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e306-128">INPUTS</span></span>

### <span data-ttu-id="3e306-129">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3e306-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="3e306-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e306-130">OUTPUTS</span></span>

### <span data-ttu-id="3e306-131">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="3e306-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="3e306-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3e306-132">ALIASES</span></span>

## <span data-ttu-id="3e306-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e306-133">NOTES</span></span>

<span data-ttu-id="3e306-134">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="3e306-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e306-135">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e306-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3e306-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="3e306-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3e306-137">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="3e306-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="3e306-138">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="3e306-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="3e306-139">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="3e306-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e306-140">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="3e306-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="3e306-141">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="3e306-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="3e306-142">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="3e306-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="3e306-143">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="3e306-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="3e306-144">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="3e306-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="3e306-145">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3e306-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="3e306-146">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="3e306-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="3e306-147">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="3e306-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3e306-148">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="3e306-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="3e306-149">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3e306-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3e306-150">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3e306-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="3e306-151">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="3e306-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="3e306-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e306-152">RELATED LINKS</span></span>
