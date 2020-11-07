---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93921944"
---
# <span data-ttu-id="37718-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="37718-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="37718-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37718-102">SYNOPSIS</span></span>
<span data-ttu-id="37718-103">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="37718-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="37718-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37718-104">SYNTAX</span></span>

### <span data-ttu-id="37718-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="37718-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="37718-106">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="37718-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="37718-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37718-107">DESCRIPTION</span></span>
<span data-ttu-id="37718-108">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="37718-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="37718-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37718-109">EXAMPLES</span></span>

### <span data-ttu-id="37718-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="37718-110">Example 1</span></span>
```powershell
PS C:\> $subscription = Get-AzsSubscription | where DisplayName -eq 'testsubscription'
$subscription.DisplayName = 'update subscription'
$subscription | Set-AzsSubscription | fl *

DisplayName    : update subscription
Id             : /subscriptions/f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
OfferId        : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
State          : Enabled
SubscriptionId : f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="37718-111">Uppdaterar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="37718-111">Updates a subscription.</span></span>

## <span data-ttu-id="37718-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37718-112">PARAMETERS</span></span>

### <span data-ttu-id="37718-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37718-113">-DefaultProfile</span></span>
<span data-ttu-id="37718-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37718-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37718-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="37718-115">-DisplayName</span></span>
<span data-ttu-id="37718-116">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="37718-116">Subscription name.</span></span>

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

### <span data-ttu-id="37718-117">-ID</span><span class="sxs-lookup"><span data-stu-id="37718-117">-Id</span></span>
<span data-ttu-id="37718-118">Fullständigt kvalificerad identifierare.</span><span class="sxs-lookup"><span data-stu-id="37718-118">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="37718-119">-OfferId</span><span class="sxs-lookup"><span data-stu-id="37718-119">-OfferId</span></span>
<span data-ttu-id="37718-120">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="37718-120">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="37718-121">-State</span><span class="sxs-lookup"><span data-stu-id="37718-121">-State</span></span>
<span data-ttu-id="37718-122">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="37718-122">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37718-123">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="37718-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="37718-124">Lista över funktioner som stöds.</span><span class="sxs-lookup"><span data-stu-id="37718-124">List of supported operations.</span></span>
<span data-ttu-id="37718-125">För att konstruera kan du läsa avsnittet anteckningar för SUBSCRIPTIONDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="37718-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="37718-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37718-126">-SubscriptionId</span></span>
<span data-ttu-id="37718-127">ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="37718-127">Id of the subscription.</span></span>

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

### <span data-ttu-id="37718-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="37718-128">-TenantId</span></span>
<span data-ttu-id="37718-129">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="37718-129">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="37718-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37718-130">-Confirm</span></span>
<span data-ttu-id="37718-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37718-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37718-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37718-132">-WhatIf</span></span>
<span data-ttu-id="37718-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="37718-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37718-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="37718-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37718-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37718-135">CommonParameters</span></span>
<span data-ttu-id="37718-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37718-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37718-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37718-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37718-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37718-138">INPUTS</span></span>

### <span data-ttu-id="37718-139">Microsoft. Azure. PowerShell. cmdletar. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="37718-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="37718-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37718-140">OUTPUTS</span></span>

### <span data-ttu-id="37718-141">Microsoft. Azure. PowerShell. cmdletar. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="37718-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="37718-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37718-142">NOTES</span></span>

<span data-ttu-id="37718-143">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="37718-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37718-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37718-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="37718-145">SUBSCRIPTIONDEFINITION <ISubscription> : lista över funktioner som stöds.</span><span class="sxs-lookup"><span data-stu-id="37718-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="37718-146">`[DisplayName <String>]`: Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="37718-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="37718-147">`[Id <String>]`: Fullständigt kvalificerad identifierare.</span><span class="sxs-lookup"><span data-stu-id="37718-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="37718-148">`[OfferId <String>]`: ID för värdet under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="37718-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="37718-149">`[State <SubscriptionState?>]`: Prenumerations status.</span><span class="sxs-lookup"><span data-stu-id="37718-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="37718-150">`[SubscriptionId <String>]`: Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="37718-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="37718-151">`[TenantId <String>]`: ID för katalog innehavare.</span><span class="sxs-lookup"><span data-stu-id="37718-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="37718-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37718-152">RELATED LINKS</span></span>

