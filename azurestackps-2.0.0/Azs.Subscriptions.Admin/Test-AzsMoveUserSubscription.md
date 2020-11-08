---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsmoveusersubscription
schema: 2.0.0
ms.openlocfilehash: c0e80b7d0f17bf505c0b3bb8d22539afffea851a
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092825"
---
# <span data-ttu-id="7fc66-101">Test-AzsMoveUserSubscription</span><span class="sxs-lookup"><span data-stu-id="7fc66-101">Test-AzsMoveUserSubscription</span></span>

## <span data-ttu-id="7fc66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fc66-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc66-103">Verifiera att användar prenumerationer kan flyttas mellan erbjudna leverantörs erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="7fc66-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="7fc66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fc66-104">SYNTAX</span></span>

### <span data-ttu-id="7fc66-105">ValidateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="7fc66-105">ValidateExpanded (Default)</span></span>
```
Test-AzsMoveUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7fc66-106">Kontrollerat</span><span class="sxs-lookup"><span data-stu-id="7fc66-106">Validate</span></span>
```
Test-AzsMoveUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7fc66-107">ValidateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7fc66-107">ValidateViaIdentity</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7fc66-108">ValidateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7fc66-108">ValidateViaIdentityExpanded</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7fc66-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fc66-109">DESCRIPTION</span></span>
<span data-ttu-id="7fc66-110">Verifiera att användar prenumerationer kan flyttas mellan erbjudna leverantörs erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="7fc66-110">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="7fc66-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fc66-111">EXAMPLES</span></span>

### <span data-ttu-id="7fc66-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7fc66-112">Example 1</span></span>
```powershell
PS C:\> Test-MoveUserSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

```

<span data-ttu-id="7fc66-113">Testa att användar abonnemang kan flyttas till ett delegerat leverantörs utbud.</span><span class="sxs-lookup"><span data-stu-id="7fc66-113">Test that user subscriptions can be moved to a delegated provider offer.</span></span>

### <span data-ttu-id="7fc66-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7fc66-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where Displayname -eq "testsubscription" | Select -ExpandProperty Id
Test-MoveUserSubscription -ResourceId $resourceIds

```

<span data-ttu-id="7fc66-115">Testa att användar abonnemang kan flyttas från en delegerad leverantör till standardprovidern.</span><span class="sxs-lookup"><span data-stu-id="7fc66-115">Test that user subscriptions can be moved from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="7fc66-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fc66-116">PARAMETERS</span></span>

### <span data-ttu-id="7fc66-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fc66-117">-AsJob</span></span>
<span data-ttu-id="7fc66-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="7fc66-118">Run the command as a job</span></span>

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

### <span data-ttu-id="7fc66-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc66-119">-DefaultProfile</span></span>
<span data-ttu-id="7fc66-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc66-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fc66-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="7fc66-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="7fc66-122">Den delegerade providerns identifierare (från administratörs kontexten) som abonnemangen ska flyttas till.</span><span class="sxs-lookup"><span data-stu-id="7fc66-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7fc66-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fc66-123">-InputObject</span></span>
<span data-ttu-id="7fc66-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7fc66-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: ValidateViaIdentity, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7fc66-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="7fc66-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="7fc66-126">Åtgärds definitionen flytta abonnemang för att konstruera, se avsnittet anteckningar för MOVESUBSCRIPTIONSDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7fc66-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Validate, ValidateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7fc66-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7fc66-127">-NoWait</span></span>
<span data-ttu-id="7fc66-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="7fc66-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7fc66-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fc66-129">-PassThru</span></span>
<span data-ttu-id="7fc66-130">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="7fc66-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7fc66-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fc66-131">-ResourceId</span></span>
<span data-ttu-id="7fc66-132">En samling prenumerationer som kan flyttas till det mottagande målet.</span><span class="sxs-lookup"><span data-stu-id="7fc66-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7fc66-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fc66-133">-SubscriptionId</span></span>
<span data-ttu-id="7fc66-134">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7fc66-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Validate, ValidateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7fc66-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7fc66-135">-Confirm</span></span>
<span data-ttu-id="7fc66-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7fc66-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fc66-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fc66-137">-WhatIf</span></span>
<span data-ttu-id="7fc66-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7fc66-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fc66-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7fc66-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fc66-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc66-140">CommonParameters</span></span>
<span data-ttu-id="7fc66-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fc66-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc66-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fc66-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc66-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fc66-143">INPUTS</span></span>

### <span data-ttu-id="7fc66-144">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IMoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="7fc66-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="7fc66-145">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7fc66-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="7fc66-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fc66-146">OUTPUTS</span></span>

### <span data-ttu-id="7fc66-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7fc66-147">System.Boolean</span></span>

<span data-ttu-id="7fc66-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7fc66-148">ALIASES</span></span>

### <span data-ttu-id="7fc66-149">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="7fc66-149">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="7fc66-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fc66-150">NOTES</span></span>

<span data-ttu-id="7fc66-151">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7fc66-151">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7fc66-152">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7fc66-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7fc66-153">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="7fc66-153">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7fc66-154">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="7fc66-154">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="7fc66-155">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="7fc66-155">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="7fc66-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="7fc66-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7fc66-157">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="7fc66-157">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="7fc66-158">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="7fc66-158">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="7fc66-159">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="7fc66-159">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="7fc66-160">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="7fc66-160">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="7fc66-161">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="7fc66-161">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="7fc66-162">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7fc66-162">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="7fc66-163">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="7fc66-163">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="7fc66-164">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="7fc66-164">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="7fc66-165">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="7fc66-165">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="7fc66-166">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7fc66-166">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7fc66-167">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7fc66-167">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="7fc66-168">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="7fc66-168">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="7fc66-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : åtgärds definitionen för flytta abonnemang</span><span class="sxs-lookup"><span data-stu-id="7fc66-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="7fc66-170">`Resources <String[]>`: En samling prenumerationer som kan flyttas till det mottagande målet.</span><span class="sxs-lookup"><span data-stu-id="7fc66-170">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="7fc66-171">`[TargetDelegatedProviderOffer <String>]`: ID för den delegerade providern (från administratörs kontexten) som abonnemangen ska flyttas till.</span><span class="sxs-lookup"><span data-stu-id="7fc66-171">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="7fc66-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fc66-172">RELATED LINKS</span></span>

