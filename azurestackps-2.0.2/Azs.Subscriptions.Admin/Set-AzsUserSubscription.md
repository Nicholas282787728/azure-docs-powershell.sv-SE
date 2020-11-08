---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100387"
---
# <span data-ttu-id="4588f-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="4588f-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="4588f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4588f-102">SYNOPSIS</span></span>
<span data-ttu-id="4588f-103">Skapar eller uppdaterar det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4588f-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="4588f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4588f-104">SYNTAX</span></span>

### <span data-ttu-id="4588f-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="4588f-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4588f-106">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="4588f-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4588f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4588f-107">DESCRIPTION</span></span>
<span data-ttu-id="4588f-108">Skapar eller uppdaterar det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4588f-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="4588f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4588f-109">EXAMPLES</span></span>

### <span data-ttu-id="4588f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4588f-110">Example 1</span></span>
```powershell
PS C:\> $Subscription = Get-AzsUserSubscription | Select-Object -First 1
$Subscription.DisplayName = 'Update User Subscription'
$Subscription | Set-AzsUserSubscription | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : Update User Subscription
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="4588f-111">Uppdaterar ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="4588f-111">Updates a subscription</span></span>

## <span data-ttu-id="4588f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4588f-112">PARAMETERS</span></span>

### <span data-ttu-id="4588f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4588f-113">-DefaultProfile</span></span>
<span data-ttu-id="4588f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4588f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4588f-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4588f-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="4588f-116">Överordnat abonnemang för DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="4588f-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4588f-117">-DisplayName</span></span>
<span data-ttu-id="4588f-118">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="4588f-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="4588f-119">-ExternalReferenceId</span></span>
<span data-ttu-id="4588f-120">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="4588f-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-121">-ID</span><span class="sxs-lookup"><span data-stu-id="4588f-121">-Id</span></span>
<span data-ttu-id="4588f-122">Fullständigt kvalificerad identifierare.</span><span class="sxs-lookup"><span data-stu-id="4588f-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="4588f-123">-OfferId</span></span>
<span data-ttu-id="4588f-124">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="4588f-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-125">-Owner</span><span class="sxs-lookup"><span data-stu-id="4588f-125">-Owner</span></span>
<span data-ttu-id="4588f-126">Abonnemangs ägare.</span><span class="sxs-lookup"><span data-stu-id="4588f-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="4588f-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="4588f-128">Routning Resource Manager-typ.</span><span class="sxs-lookup"><span data-stu-id="4588f-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-129">-State</span><span class="sxs-lookup"><span data-stu-id="4588f-129">-State</span></span>
<span data-ttu-id="4588f-130">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="4588f-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="4588f-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="4588f-132">Egenskaper för prenumerations objekt.</span><span class="sxs-lookup"><span data-stu-id="4588f-132">Subscription object properties.</span></span>
<span data-ttu-id="4588f-133">För att konstruera kan du läsa avsnittet anteckningar för SUBSCRIPTIONDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4588f-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4588f-134">-SubscriptionId</span></span>
<span data-ttu-id="4588f-135">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="4588f-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="4588f-136">-SubscriptionId1</span></span>
<span data-ttu-id="4588f-137">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="4588f-137">Subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-138">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4588f-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="4588f-139">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4588f-139">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-140">-TenantId</span><span class="sxs-lookup"><span data-stu-id="4588f-140">-TenantId</span></span>
<span data-ttu-id="4588f-141">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="4588f-141">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4588f-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4588f-142">-Confirm</span></span>
<span data-ttu-id="4588f-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4588f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4588f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4588f-144">-WhatIf</span></span>
<span data-ttu-id="4588f-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4588f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4588f-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4588f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4588f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4588f-147">CommonParameters</span></span>
<span data-ttu-id="4588f-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4588f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4588f-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4588f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4588f-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4588f-150">INPUTS</span></span>

### <span data-ttu-id="4588f-151">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="4588f-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="4588f-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4588f-152">OUTPUTS</span></span>

### <span data-ttu-id="4588f-153">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="4588f-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="4588f-154">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4588f-154">ALIASES</span></span>

## <span data-ttu-id="4588f-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4588f-155">NOTES</span></span>

<span data-ttu-id="4588f-156">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="4588f-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4588f-157">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4588f-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4588f-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : egenskaper för prenumerations objekt.</span><span class="sxs-lookup"><span data-stu-id="4588f-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="4588f-159">`[DelegatedProviderSubscriptionId <String>]`: ID för överordnad DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="4588f-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="4588f-160">`[DisplayName <String>]`: Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="4588f-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="4588f-161">`[ExternalReferenceId <String>]`: Identifierare för extern referens.</span><span class="sxs-lookup"><span data-stu-id="4588f-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="4588f-162">`[Id <String>]`: Fullständigt kvalificerad identifierare.</span><span class="sxs-lookup"><span data-stu-id="4588f-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="4588f-163">`[OfferId <String>]`: ID för värdet under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="4588f-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="4588f-164">`[Owner <String>]`: Prenumerationens ägare.</span><span class="sxs-lookup"><span data-stu-id="4588f-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="4588f-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Operationsföljd Resource Manager-typ.</span><span class="sxs-lookup"><span data-stu-id="4588f-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="4588f-166">`[State <SubscriptionState?>]`: Prenumerations status.</span><span class="sxs-lookup"><span data-stu-id="4588f-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="4588f-167">`[SubscriptionId <String>]`: Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="4588f-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="4588f-168">`[TenantId <String>]`: ID för katalog innehavare.</span><span class="sxs-lookup"><span data-stu-id="4588f-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="4588f-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4588f-169">RELATED LINKS</span></span>

