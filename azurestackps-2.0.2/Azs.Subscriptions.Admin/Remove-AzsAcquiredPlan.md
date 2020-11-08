---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 80a4353497d0c7894a8c0ac4d95e57e56a6211a1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100310"
---
# <span data-ttu-id="a5e64-101">Remove-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="a5e64-101">Remove-AzsAcquiredPlan</span></span>

## <span data-ttu-id="a5e64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5e64-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e64-103">Tar bort ett anskaffat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a5e64-103">Deletes an acquired plan.</span></span>

## <span data-ttu-id="a5e64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5e64-104">SYNTAX</span></span>

### <span data-ttu-id="a5e64-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="a5e64-105">Delete (Default)</span></span>
```
Remove-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a5e64-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a5e64-106">DeleteViaIdentity</span></span>
```
Remove-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5e64-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5e64-107">DESCRIPTION</span></span>
<span data-ttu-id="a5e64-108">Tar bort ett anskaffat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a5e64-108">Deletes an acquired plan.</span></span>

## <span data-ttu-id="a5e64-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5e64-109">EXAMPLES</span></span>

### <span data-ttu-id="a5e64-110">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="a5e64-110">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsAcquiredPlan -PlanAcquisitionId "718c7f7c-4868-479a-98ce-5caaa8f158c2" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

```

<span data-ttu-id="a5e64-111">Ta bort ett förvärvat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a5e64-111">Delete an acquired plan.</span></span>

## <span data-ttu-id="a5e64-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5e64-112">PARAMETERS</span></span>

### <span data-ttu-id="a5e64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e64-113">-DefaultProfile</span></span>
<span data-ttu-id="a5e64-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e64-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e64-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5e64-115">-InputObject</span></span>
<span data-ttu-id="a5e64-116">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a5e64-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5e64-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5e64-117">-PassThru</span></span>
<span data-ttu-id="a5e64-118">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="a5e64-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a5e64-119">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="a5e64-119">-PlanAcquisitionId</span></span>
<span data-ttu-id="a5e64-120">Abonnemangets anskaffnings identifierare</span><span class="sxs-lookup"><span data-stu-id="a5e64-120">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="a5e64-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5e64-121">-SubscriptionId</span></span>
<span data-ttu-id="a5e64-122">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a5e64-122">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a5e64-123">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5e64-123">-TargetSubscriptionId</span></span>
<span data-ttu-id="a5e64-124">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a5e64-124">The target subscription ID.</span></span>

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

### <span data-ttu-id="a5e64-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5e64-125">-Confirm</span></span>
<span data-ttu-id="a5e64-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5e64-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e64-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e64-127">-WhatIf</span></span>
<span data-ttu-id="a5e64-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5e64-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5e64-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5e64-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e64-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e64-130">CommonParameters</span></span>
<span data-ttu-id="a5e64-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e64-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e64-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5e64-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e64-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5e64-133">INPUTS</span></span>

### <span data-ttu-id="a5e64-134">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a5e64-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="a5e64-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5e64-135">OUTPUTS</span></span>

### <span data-ttu-id="a5e64-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5e64-136">System.Boolean</span></span>

<span data-ttu-id="a5e64-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a5e64-137">ALIASES</span></span>

### <span data-ttu-id="a5e64-138">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="a5e64-138">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="a5e64-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5e64-139">NOTES</span></span>

<span data-ttu-id="a5e64-140">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a5e64-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5e64-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5e64-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a5e64-142">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="a5e64-142">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a5e64-143">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="a5e64-143">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="a5e64-144">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="a5e64-144">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="a5e64-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="a5e64-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a5e64-146">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="a5e64-146">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="a5e64-147">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="a5e64-147">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="a5e64-148">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="a5e64-148">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="a5e64-149">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="a5e64-149">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="a5e64-150">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="a5e64-150">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="a5e64-151">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a5e64-151">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="a5e64-152">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="a5e64-152">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="a5e64-153">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="a5e64-153">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="a5e64-154">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="a5e64-154">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="a5e64-155">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a5e64-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a5e64-156">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a5e64-156">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="a5e64-157">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="a5e64-157">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="a5e64-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5e64-158">RELATED LINKS</span></span>

