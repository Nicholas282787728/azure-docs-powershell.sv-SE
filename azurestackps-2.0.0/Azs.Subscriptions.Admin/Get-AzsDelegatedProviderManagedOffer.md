---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovidermanagedoffer
schema: 2.0.0
ms.openlocfilehash: 238fe2a9c3f0cf1d4fdefc5a09231066152cfe60
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092862"
---
# <span data-ttu-id="8532a-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="8532a-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="8532a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8532a-102">SYNOPSIS</span></span>
<span data-ttu-id="8532a-103">Skaffa det angivna alternativet för ombudet.</span><span class="sxs-lookup"><span data-stu-id="8532a-103">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="8532a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8532a-104">SYNTAX</span></span>

### <span data-ttu-id="8532a-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8532a-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8532a-106">Lära</span><span class="sxs-lookup"><span data-stu-id="8532a-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> -Name <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8532a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8532a-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8532a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8532a-108">DESCRIPTION</span></span>
<span data-ttu-id="8532a-109">Skaffa det angivna alternativet för ombudet.</span><span class="sxs-lookup"><span data-stu-id="8532a-109">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="8532a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8532a-110">EXAMPLES</span></span>

### <span data-ttu-id="8532a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8532a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

{{ Add output here }}
```

<span data-ttu-id="8532a-112">Hämta listan med erbjudanden för ombud.</span><span class="sxs-lookup"><span data-stu-id="8532a-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="8532a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8532a-113">PARAMETERS</span></span>

### <span data-ttu-id="8532a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8532a-114">-DefaultProfile</span></span>
<span data-ttu-id="8532a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8532a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8532a-116">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8532a-116">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="8532a-117">Prenumeration på abonnemang för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="8532a-117">Delegated provider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: DelegatedProviderId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8532a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8532a-118">-InputObject</span></span>
<span data-ttu-id="8532a-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8532a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8532a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="8532a-120">-Name</span></span>
<span data-ttu-id="8532a-121">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="8532a-121">Name of an offer.</span></span>

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

### <span data-ttu-id="8532a-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8532a-122">-SubscriptionId</span></span>
<span data-ttu-id="8532a-123">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8532a-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8532a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8532a-124">CommonParameters</span></span>
<span data-ttu-id="8532a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8532a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8532a-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8532a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8532a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8532a-127">INPUTS</span></span>

### <span data-ttu-id="8532a-128">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8532a-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="8532a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8532a-129">OUTPUTS</span></span>

### <span data-ttu-id="8532a-130">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="8532a-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDelegatedProviderOffer</span></span>

<span data-ttu-id="8532a-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8532a-131">ALIASES</span></span>

## <span data-ttu-id="8532a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8532a-132">NOTES</span></span>

<span data-ttu-id="8532a-133">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8532a-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8532a-134">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8532a-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8532a-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8532a-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8532a-136">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="8532a-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="8532a-137">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="8532a-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="8532a-138">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8532a-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8532a-139">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="8532a-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="8532a-140">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="8532a-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="8532a-141">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="8532a-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="8532a-142">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="8532a-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="8532a-143">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="8532a-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="8532a-144">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8532a-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="8532a-145">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="8532a-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="8532a-146">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="8532a-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="8532a-147">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="8532a-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="8532a-148">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8532a-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8532a-149">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8532a-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="8532a-150">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="8532a-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="8532a-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8532a-151">RELATED LINKS</span></span>

