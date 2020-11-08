---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 6ccc47c6b6254e23050cf4341cae355bda78d8df
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092842"
---
# <span data-ttu-id="fe09a-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="fe09a-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="fe09a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe09a-102">SYNOPSIS</span></span>
<span data-ttu-id="fe09a-103">Skapar eller uppdaterar det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe09a-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="fe09a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe09a-104">SYNTAX</span></span>

### <span data-ttu-id="fe09a-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="fe09a-105">CreateExpanded (Default)</span></span>
```
New-AzsUserSubscription -OfferId <String> -Owner <String> [-TargetSubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-RoutingResourceManagerType <ResourceManagerType>] [-State <SubscriptionState>]
 [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fe09a-106">Göra</span><span class="sxs-lookup"><span data-stu-id="fe09a-106">Create</span></span>
```
New-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-TargetSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fe09a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe09a-107">DESCRIPTION</span></span>
<span data-ttu-id="fe09a-108">Skapar eller uppdaterar det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe09a-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="fe09a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe09a-109">EXAMPLES</span></span>

### <span data-ttu-id="fe09a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fe09a-110">Example 1</span></span>
```powershell
PS C:\> New-AzsUserSubscription -Owner "user@contoso.com" -OfferId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOffer" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : 
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/398466a8-7d43-455a-b842-772d356d119e
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOff
                                  er
Owner                           : user@contoso.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : 398466a8-7d43-455a-b842-772d356d119e
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="fe09a-111">Skapar en ny användar prenumeration</span><span class="sxs-lookup"><span data-stu-id="fe09a-111">Creates a new user subscription</span></span>

## <span data-ttu-id="fe09a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe09a-112">PARAMETERS</span></span>

### <span data-ttu-id="fe09a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe09a-113">-DefaultProfile</span></span>
<span data-ttu-id="fe09a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe09a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe09a-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe09a-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="fe09a-116">Överordnat abonnemang för DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="fe09a-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe09a-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fe09a-117">-DisplayName</span></span>
<span data-ttu-id="fe09a-118">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="fe09a-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe09a-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="fe09a-119">-ExternalReferenceId</span></span>
<span data-ttu-id="fe09a-120">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="fe09a-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe09a-121">-ID</span><span class="sxs-lookup"><span data-stu-id="fe09a-121">-Id</span></span>
<span data-ttu-id="fe09a-122">Fullständigt kvalificerad identifierare.</span><span class="sxs-lookup"><span data-stu-id="fe09a-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe09a-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="fe09a-123">-OfferId</span></span>
<span data-ttu-id="fe09a-124">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="fe09a-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe09a-125">-Owner</span><span class="sxs-lookup"><span data-stu-id="fe09a-125">-Owner</span></span>
<span data-ttu-id="fe09a-126">Abonnemangs ägare.</span><span class="sxs-lookup"><span data-stu-id="fe09a-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe09a-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="fe09a-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="fe09a-128">Routning Resource Manager-typ.</span><span class="sxs-lookup"><span data-stu-id="fe09a-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Default"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe09a-129">-State</span><span class="sxs-lookup"><span data-stu-id="fe09a-129">-State</span></span>
<span data-ttu-id="fe09a-130">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="fe09a-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe09a-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="fe09a-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="fe09a-132">Egenskaper för prenumerations objekt.</span><span class="sxs-lookup"><span data-stu-id="fe09a-132">Subscription object properties.</span></span>
<span data-ttu-id="fe09a-133">För att konstruera kan du läsa avsnittet anteckningar för SUBSCRIPTIONDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="fe09a-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fe09a-134">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe09a-134">-TargetSubscriptionId</span></span>
<span data-ttu-id="fe09a-135">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="fe09a-135">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe09a-136">-TenantId</span><span class="sxs-lookup"><span data-stu-id="fe09a-136">-TenantId</span></span>
<span data-ttu-id="fe09a-137">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="fe09a-137">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fe09a-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe09a-138">-Confirm</span></span>
<span data-ttu-id="fe09a-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe09a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe09a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe09a-140">-WhatIf</span></span>
<span data-ttu-id="fe09a-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe09a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe09a-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe09a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe09a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe09a-143">CommonParameters</span></span>
<span data-ttu-id="fe09a-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe09a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe09a-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe09a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe09a-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe09a-146">INPUTS</span></span>

### <span data-ttu-id="fe09a-147">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="fe09a-147">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="fe09a-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe09a-148">OUTPUTS</span></span>

### <span data-ttu-id="fe09a-149">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="fe09a-149">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="fe09a-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fe09a-150">ALIASES</span></span>

## <span data-ttu-id="fe09a-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe09a-151">NOTES</span></span>

<span data-ttu-id="fe09a-152">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="fe09a-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fe09a-153">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fe09a-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fe09a-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : egenskaper för prenumerations objekt.</span><span class="sxs-lookup"><span data-stu-id="fe09a-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="fe09a-155">`[DelegatedProviderSubscriptionId <String>]`: ID för överordnad DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="fe09a-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="fe09a-156">`[DisplayName <String>]`: Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="fe09a-156">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="fe09a-157">`[ExternalReferenceId <String>]`: Identifierare för extern referens.</span><span class="sxs-lookup"><span data-stu-id="fe09a-157">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="fe09a-158">`[Id <String>]`: Fullständigt kvalificerad identifierare.</span><span class="sxs-lookup"><span data-stu-id="fe09a-158">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="fe09a-159">`[OfferId <String>]`: ID för värdet under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="fe09a-159">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="fe09a-160">`[Owner <String>]`: Prenumerationens ägare.</span><span class="sxs-lookup"><span data-stu-id="fe09a-160">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="fe09a-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Operationsföljd Resource Manager-typ.</span><span class="sxs-lookup"><span data-stu-id="fe09a-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="fe09a-162">`[State <SubscriptionState?>]`: Prenumerations status.</span><span class="sxs-lookup"><span data-stu-id="fe09a-162">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="fe09a-163">`[SubscriptionId <String>]`: Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="fe09a-163">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="fe09a-164">`[TenantId <String>]`: ID för katalog innehavare.</span><span class="sxs-lookup"><span data-stu-id="fe09a-164">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="fe09a-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe09a-165">RELATED LINKS</span></span>
