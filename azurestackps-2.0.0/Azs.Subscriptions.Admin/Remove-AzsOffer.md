---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsoffer
schema: 2.0.0
ms.openlocfilehash: d38c7493e49888fe638cae4fbb5cb937ec41ccba
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092840"
---
# <span data-ttu-id="90062-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="90062-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="90062-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90062-102">SYNOPSIS</span></span>
<span data-ttu-id="90062-103">Ta bort det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="90062-103">Delete the specified offer.</span></span>

## <span data-ttu-id="90062-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90062-104">SYNTAX</span></span>

### <span data-ttu-id="90062-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="90062-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90062-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="90062-106">DeleteViaIdentity</span></span>
```
Remove-AzsOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90062-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90062-107">DESCRIPTION</span></span>
<span data-ttu-id="90062-108">Ta bort det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="90062-108">Delete the specified offer.</span></span>

## <span data-ttu-id="90062-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90062-109">EXAMPLES</span></span>

### <span data-ttu-id="90062-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="90062-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOffer -Name "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="90062-111">Ta bort det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="90062-111">Delete the specified offer.</span></span>

## <span data-ttu-id="90062-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90062-112">PARAMETERS</span></span>

### <span data-ttu-id="90062-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90062-113">-DefaultProfile</span></span>
<span data-ttu-id="90062-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90062-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90062-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90062-115">-InputObject</span></span>
<span data-ttu-id="90062-116">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="90062-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="90062-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="90062-117">-Name</span></span>
<span data-ttu-id="90062-118">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="90062-118">Name of an offer.</span></span>

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

### <span data-ttu-id="90062-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90062-119">-PassThru</span></span>
<span data-ttu-id="90062-120">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="90062-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="90062-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90062-121">-ResourceGroupName</span></span>
<span data-ttu-id="90062-122">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="90062-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="90062-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90062-123">-SubscriptionId</span></span>
<span data-ttu-id="90062-124">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="90062-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="90062-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="90062-125">-Confirm</span></span>
<span data-ttu-id="90062-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="90062-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90062-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90062-127">-WhatIf</span></span>
<span data-ttu-id="90062-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="90062-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90062-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="90062-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90062-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90062-130">CommonParameters</span></span>
<span data-ttu-id="90062-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90062-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90062-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90062-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90062-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90062-133">INPUTS</span></span>

### <span data-ttu-id="90062-134">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="90062-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="90062-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90062-135">OUTPUTS</span></span>

### <span data-ttu-id="90062-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90062-136">System.Boolean</span></span>

<span data-ttu-id="90062-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="90062-137">ALIASES</span></span>

## <span data-ttu-id="90062-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90062-138">NOTES</span></span>

<span data-ttu-id="90062-139">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="90062-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90062-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90062-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="90062-141">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="90062-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90062-142">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="90062-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="90062-143">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="90062-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="90062-144">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="90062-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90062-145">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="90062-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="90062-146">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="90062-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="90062-147">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="90062-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="90062-148">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="90062-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="90062-149">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="90062-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="90062-150">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="90062-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="90062-151">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="90062-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="90062-152">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="90062-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="90062-153">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="90062-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="90062-154">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="90062-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="90062-155">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="90062-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="90062-156">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="90062-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="90062-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90062-157">RELATED LINKS</span></span>

