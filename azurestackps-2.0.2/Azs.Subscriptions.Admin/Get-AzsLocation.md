---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azslocation
schema: 2.0.0
ms.openlocfilehash: 431989f382d51b596cafc74d4cf229c6e803ccd6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099963"
---
# <span data-ttu-id="5cde4-101">Get-AzsLocation</span><span class="sxs-lookup"><span data-stu-id="5cde4-101">Get-AzsLocation</span></span>

## <span data-ttu-id="5cde4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5cde4-102">SYNOPSIS</span></span>
<span data-ttu-id="5cde4-103">Hämta den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="5cde4-103">Get the specified location.</span></span>

## <span data-ttu-id="5cde4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5cde4-104">SYNTAX</span></span>

### <span data-ttu-id="5cde4-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="5cde4-105">List (Default)</span></span>
```
Get-AzsLocation [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cde4-106">Lära</span><span class="sxs-lookup"><span data-stu-id="5cde4-106">Get</span></span>
```
Get-AzsLocation -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cde4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5cde4-107">GetViaIdentity</span></span>
```
Get-AzsLocation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5cde4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5cde4-108">DESCRIPTION</span></span>
<span data-ttu-id="5cde4-109">Hämta den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="5cde4-109">Get the specified location.</span></span>

## <span data-ttu-id="5cde4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5cde4-110">EXAMPLES</span></span>

### <span data-ttu-id="5cde4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5cde4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsLocation

DisplayName Latitude Longitude Name   
----------- -------- --------- ----   
redmond                        redmond
```

<span data-ttu-id="5cde4-112">Få en lista över alla AzureStack-platser.</span><span class="sxs-lookup"><span data-stu-id="5cde4-112">Get a list of all AzureStack locations.</span></span>

## <span data-ttu-id="5cde4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5cde4-113">PARAMETERS</span></span>

### <span data-ttu-id="5cde4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cde4-114">-DefaultProfile</span></span>
<span data-ttu-id="5cde4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5cde4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cde4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cde4-116">-InputObject</span></span>
<span data-ttu-id="5cde4-117">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5cde4-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cde4-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="5cde4-118">-Name</span></span>
<span data-ttu-id="5cde4-119">AzureStack-platsen.</span><span class="sxs-lookup"><span data-stu-id="5cde4-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Location

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5cde4-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cde4-120">-SubscriptionId</span></span>
<span data-ttu-id="5cde4-121">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5cde4-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5cde4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cde4-122">CommonParameters</span></span>
<span data-ttu-id="5cde4-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cde4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cde4-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cde4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cde4-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5cde4-125">INPUTS</span></span>

### <span data-ttu-id="5cde4-126">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5cde4-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="5cde4-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5cde4-127">OUTPUTS</span></span>

### <span data-ttu-id="5cde4-128">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. ILocation</span><span class="sxs-lookup"><span data-stu-id="5cde4-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ILocation</span></span>

<span data-ttu-id="5cde4-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5cde4-129">ALIASES</span></span>

## <span data-ttu-id="5cde4-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5cde4-130">NOTES</span></span>

<span data-ttu-id="5cde4-131">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="5cde4-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cde4-132">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5cde4-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5cde4-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5cde4-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5cde4-134">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="5cde4-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="5cde4-135">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="5cde4-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="5cde4-136">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5cde4-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5cde4-137">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="5cde4-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="5cde4-138">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="5cde4-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="5cde4-139">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="5cde4-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="5cde4-140">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="5cde4-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="5cde4-141">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="5cde4-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="5cde4-142">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5cde4-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="5cde4-143">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="5cde4-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="5cde4-144">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="5cde4-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="5cde4-145">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="5cde4-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="5cde4-146">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5cde4-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5cde4-147">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5cde4-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="5cde4-148">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="5cde4-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="5cde4-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5cde4-149">RELATED LINKS</span></span>

