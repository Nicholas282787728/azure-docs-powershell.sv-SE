---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 03fbbc38582bf301052074e674fa86abe97d6b61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100153"
---
# <span data-ttu-id="9ebb7-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="9ebb7-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="9ebb7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ebb7-102">SYNOPSIS</span></span>


## <span data-ttu-id="9ebb7-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ebb7-103">SYNTAX</span></span>

### <span data-ttu-id="9ebb7-104">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="9ebb7-104">Delete (Default)</span></span>
```
Remove-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9ebb7-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9ebb7-105">DeleteViaIdentity</span></span>
```
Remove-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Force]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9ebb7-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ebb7-106">DESCRIPTION</span></span>


## <span data-ttu-id="9ebb7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ebb7-107">EXAMPLES</span></span>

### <span data-ttu-id="9ebb7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9ebb7-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

```

<span data-ttu-id="9ebb7-109">Ta bort den angivna klient prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-109">Delete the specified tenant subscription.</span></span>

## <span data-ttu-id="9ebb7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ebb7-110">PARAMETERS</span></span>

### <span data-ttu-id="9ebb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ebb7-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="9ebb7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="9ebb7-112">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9ebb7-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ebb7-113">-InputObject</span></span>
<span data-ttu-id="9ebb7-114">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9ebb7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ebb7-115">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9ebb7-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ebb7-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9ebb7-117">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ebb7-117">-TargetSubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9ebb7-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9ebb7-118">-Confirm</span></span>
<span data-ttu-id="9ebb7-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9ebb7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ebb7-120">-WhatIf</span></span>
<span data-ttu-id="9ebb7-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ebb7-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9ebb7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ebb7-123">CommonParameters</span></span>
<span data-ttu-id="9ebb7-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ebb7-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ebb7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ebb7-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ebb7-126">INPUTS</span></span>

### <span data-ttu-id="9ebb7-127">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9ebb7-127">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="9ebb7-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ebb7-128">OUTPUTS</span></span>

### <span data-ttu-id="9ebb7-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ebb7-129">System.Boolean</span></span>

<span data-ttu-id="9ebb7-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9ebb7-130">ALIASES</span></span>

## <span data-ttu-id="9ebb7-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ebb7-131">NOTES</span></span>

<span data-ttu-id="9ebb7-132">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9ebb7-133">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9ebb7-134">INPUTOBJECT <ISubscriptionsAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="9ebb7-134">INPUTOBJECT <ISubscriptionsAdminIdentity>:</span></span> 
  - <span data-ttu-id="9ebb7-135">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-135">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="9ebb7-136">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-136">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="9ebb7-137">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9ebb7-137">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9ebb7-138">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-138">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="9ebb7-139">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-139">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="9ebb7-140">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-140">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="9ebb7-141">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-141">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="9ebb7-142">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-142">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="9ebb7-143">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-143">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="9ebb7-144">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="9ebb7-144">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="9ebb7-145">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-145">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9ebb7-146">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-146">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="9ebb7-147">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-147">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9ebb7-148">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-148">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="9ebb7-149">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="9ebb7-149">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="9ebb7-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ebb7-150">RELATED LINKS</span></span>

