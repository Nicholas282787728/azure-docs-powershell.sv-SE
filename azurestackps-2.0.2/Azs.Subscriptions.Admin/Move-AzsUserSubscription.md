---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/move-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 51ad63ef1531e7494b3929b8508e88e988155081
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100058"
---
# <span data-ttu-id="e754a-101">Move-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="e754a-101">Move-AzsUserSubscription</span></span>

## <span data-ttu-id="e754a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e754a-102">SYNOPSIS</span></span>
<span data-ttu-id="e754a-103">Flytta abonnemang mellan delegerade leverantörs erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="e754a-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="e754a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e754a-104">SYNTAX</span></span>

### <span data-ttu-id="e754a-105">MoveExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="e754a-105">MoveExpanded (Default)</span></span>
```
Move-AzsUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e754a-106">Flyttas</span><span class="sxs-lookup"><span data-stu-id="e754a-106">Move</span></span>
```
Move-AzsUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e754a-107">MoveViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e754a-107">MoveViaIdentity</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e754a-108">MoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e754a-108">MoveViaIdentityExpanded</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e754a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e754a-109">DESCRIPTION</span></span>
<span data-ttu-id="e754a-110">Flytta abonnemang mellan delegerade leverantörs erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="e754a-110">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="e754a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e754a-111">EXAMPLES</span></span>

### <span data-ttu-id="e754a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e754a-112">Example 1</span></span>
```powershell
PS C:\> Move-AzsSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

{{ Add output here }}
```

<span data-ttu-id="e754a-113">Flytta användar abonnemang till ett leverantörs förslag.</span><span class="sxs-lookup"><span data-stu-id="e754a-113">Move user subscriptions to a delegated provider offer.</span></span>

### <span data-ttu-id="e754a-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e754a-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id
Move-AzsSubscription -ResourceId $resourceIds

{{ Add output here }}
```

<span data-ttu-id="e754a-115">Flytta användar abonnemang från en delegerad leverantör till standardprovidern.</span><span class="sxs-lookup"><span data-stu-id="e754a-115">Move user subscriptions from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="e754a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e754a-116">PARAMETERS</span></span>

### <span data-ttu-id="e754a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e754a-117">-AsJob</span></span>
<span data-ttu-id="e754a-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="e754a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e754a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e754a-119">-DefaultProfile</span></span>
<span data-ttu-id="e754a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e754a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e754a-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="e754a-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="e754a-122">Den delegerade providerns identifierare (från administratörs kontexten) som abonnemangen ska flyttas till.</span><span class="sxs-lookup"><span data-stu-id="e754a-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e754a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e754a-123">-InputObject</span></span>
<span data-ttu-id="e754a-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e754a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: MoveViaIdentity, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e754a-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="e754a-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="e754a-126">Åtgärds definitionen flytta abonnemang för att konstruera, se avsnittet anteckningar för MOVESUBSCRIPTIONSDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e754a-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Move, MoveViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e754a-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e754a-127">-NoWait</span></span>
<span data-ttu-id="e754a-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="e754a-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e754a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e754a-129">-PassThru</span></span>
<span data-ttu-id="e754a-130">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="e754a-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e754a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e754a-131">-ResourceId</span></span>
<span data-ttu-id="e754a-132">En samling prenumerationer som kan flyttas till det mottagande målet.</span><span class="sxs-lookup"><span data-stu-id="e754a-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e754a-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e754a-133">-SubscriptionId</span></span>
<span data-ttu-id="e754a-134">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e754a-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Move, MoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e754a-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e754a-135">-Confirm</span></span>
<span data-ttu-id="e754a-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e754a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e754a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e754a-137">-WhatIf</span></span>
<span data-ttu-id="e754a-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e754a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e754a-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e754a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e754a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e754a-140">CommonParameters</span></span>
<span data-ttu-id="e754a-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e754a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e754a-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e754a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e754a-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e754a-143">INPUTS</span></span>

### <span data-ttu-id="e754a-144">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IMoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="e754a-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="e754a-145">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e754a-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="e754a-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e754a-146">OUTPUTS</span></span>

### <span data-ttu-id="e754a-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e754a-147">System.Boolean</span></span>

<span data-ttu-id="e754a-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e754a-148">ALIASES</span></span>

## <span data-ttu-id="e754a-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e754a-149">NOTES</span></span>

<span data-ttu-id="e754a-150">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e754a-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e754a-151">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e754a-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e754a-152">INPUTOBJECT <ISubscriptionsAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e754a-152">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e754a-153">`[DelegatedProvider <String>]`: DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="e754a-153">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="e754a-154">`[DelegatedProviderSubscriptionId <String>]`: ID för prenumeration för delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="e754a-154">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="e754a-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e754a-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e754a-156">`[Location <String>]`: AzureStack plats.</span><span class="sxs-lookup"><span data-stu-id="e754a-156">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="e754a-157">`[ManifestName <String>]`: Manifest namnet.</span><span class="sxs-lookup"><span data-stu-id="e754a-157">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="e754a-158">`[Offer <String>]`: Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="e754a-158">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="e754a-159">`[OfferDelegationName <String>]`: Namn på en förslags delegation.</span><span class="sxs-lookup"><span data-stu-id="e754a-159">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="e754a-160">`[OperationsStatusName <String>]`: Namnet på åtgärds status.</span><span class="sxs-lookup"><span data-stu-id="e754a-160">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="e754a-161">`[Plan <String>]`: Namnet på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e754a-161">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="e754a-162">`[PlanAcquisitionId <String>]`: ID för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="e754a-162">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="e754a-163">`[Quota <String>]`: Kvotens namn.</span><span class="sxs-lookup"><span data-stu-id="e754a-163">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e754a-164">`[ResourceGroupName <String>]`: Resurs gruppen finns under.</span><span class="sxs-lookup"><span data-stu-id="e754a-164">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="e754a-165">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e754a-165">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e754a-166">`[TargetSubscriptionId <String>]`: ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e754a-166">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="e754a-167">`[Tenant <String>]`: Katalog innehavarens namn.</span><span class="sxs-lookup"><span data-stu-id="e754a-167">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="e754a-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : åtgärds definitionen för flytta abonnemang</span><span class="sxs-lookup"><span data-stu-id="e754a-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="e754a-169">`Resources <String[]>`: En samling prenumerationer som kan flyttas till det mottagande målet.</span><span class="sxs-lookup"><span data-stu-id="e754a-169">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="e754a-170">`[TargetDelegatedProviderOffer <String>]`: ID för den delegerade providern (från administratörs kontexten) som abonnemangen ska flyttas till.</span><span class="sxs-lookup"><span data-stu-id="e754a-170">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="e754a-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e754a-171">RELATED LINKS</span></span>

