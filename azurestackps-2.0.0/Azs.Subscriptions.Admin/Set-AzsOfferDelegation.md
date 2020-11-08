---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 59afc363d040724bbd525afc6e1f599a995cfdcb
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092828"
---
# <span data-ttu-id="a85f1-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a85f1-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="a85f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a85f1-102">SYNOPSIS</span></span>
<span data-ttu-id="a85f1-103">Skapa eller uppdatera alternativet för att ge offerter.</span><span class="sxs-lookup"><span data-stu-id="a85f1-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="a85f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a85f1-104">SYNTAX</span></span>

### <span data-ttu-id="a85f1-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="a85f1-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-PropertiesSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a85f1-106">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="a85f1-106">Update</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a85f1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a85f1-107">DESCRIPTION</span></span>
<span data-ttu-id="a85f1-108">Skapa eller uppdatera alternativet för att ge offerter.</span><span class="sxs-lookup"><span data-stu-id="a85f1-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="a85f1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a85f1-109">EXAMPLES</span></span>

### <span data-ttu-id="a85f1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a85f1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"

{{ Add output here }}
```

<span data-ttu-id="a85f1-111">Uppdaterar alternativet för att tillhandahålla offerter.</span><span class="sxs-lookup"><span data-stu-id="a85f1-111">Updates the offer delegation.</span></span>

## <span data-ttu-id="a85f1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a85f1-112">PARAMETERS</span></span>

### <span data-ttu-id="a85f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85f1-113">-DefaultProfile</span></span>
<span data-ttu-id="a85f1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a85f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a85f1-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="a85f1-115">-Location</span></span>
<span data-ttu-id="a85f1-116">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="a85f1-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a85f1-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a85f1-117">-Name</span></span>
<span data-ttu-id="a85f1-118">Namn på en ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="a85f1-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a85f1-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="a85f1-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="a85f1-120">Ge ombud.</span><span class="sxs-lookup"><span data-stu-id="a85f1-120">Offer delegation.</span></span>
<span data-ttu-id="a85f1-121">För att konstruera kan du läsa avsnittet anteckningar för OFFERDELEGATIONDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a85f1-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a85f1-122">-OfferName</span><span class="sxs-lookup"><span data-stu-id="a85f1-122">-OfferName</span></span>
<span data-ttu-id="a85f1-123">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="a85f1-123">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a85f1-124">-PropertiesSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a85f1-124">-PropertiesSubscriptionId</span></span>
<span data-ttu-id="a85f1-125">ID för det abonnemang som tar emot det delegerade erbjudandet.</span><span class="sxs-lookup"><span data-stu-id="a85f1-125">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="a85f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a85f1-126">-ResourceGroupName</span></span>
<span data-ttu-id="a85f1-127">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="a85f1-127">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a85f1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a85f1-128">-SubscriptionId</span></span>
<span data-ttu-id="a85f1-129">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a85f1-129">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a85f1-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a85f1-130">-Confirm</span></span>
<span data-ttu-id="a85f1-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a85f1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a85f1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a85f1-132">-WhatIf</span></span>
<span data-ttu-id="a85f1-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a85f1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a85f1-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a85f1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a85f1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85f1-135">CommonParameters</span></span>
<span data-ttu-id="a85f1-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a85f1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85f1-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a85f1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85f1-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a85f1-138">INPUTS</span></span>

### <span data-ttu-id="a85f1-139">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a85f1-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="a85f1-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a85f1-140">OUTPUTS</span></span>

### <span data-ttu-id="a85f1-141">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a85f1-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="a85f1-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a85f1-142">ALIASES</span></span>

## <span data-ttu-id="a85f1-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a85f1-143">NOTES</span></span>

<span data-ttu-id="a85f1-144">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a85f1-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a85f1-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a85f1-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a85f1-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : ge ombud.</span><span class="sxs-lookup"><span data-stu-id="a85f1-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="a85f1-147">`[Location <String>]`: Resursens plats</span><span class="sxs-lookup"><span data-stu-id="a85f1-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="a85f1-148">`[SubscriptionId <String>]`: ID för den prenumeration som tar emot det delegerade erbjudandet.</span><span class="sxs-lookup"><span data-stu-id="a85f1-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="a85f1-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a85f1-149">RELATED LINKS</span></span>

