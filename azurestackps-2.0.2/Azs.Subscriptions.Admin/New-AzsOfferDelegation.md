---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 8a3797006bb5006b1b4e715b45c5e12763c49f32
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100373"
---
# <span data-ttu-id="c4a0a-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c4a0a-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="c4a0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a0a-103">Skapa eller uppdatera alternativet för att ge offerter.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="c4a0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4a0a-104">SYNTAX</span></span>

### <span data-ttu-id="c4a0a-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="c4a0a-105">CreateExpanded (Default)</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-TargetSubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4a0a-106">Göra</span><span class="sxs-lookup"><span data-stu-id="c4a0a-106">Create</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4a0a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4a0a-107">DESCRIPTION</span></span>
<span data-ttu-id="c4a0a-108">Skapa eller uppdatera alternativet för att ge offerter.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="c4a0a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4a0a-109">EXAMPLES</span></span>

### <span data-ttu-id="c4a0a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4a0a-110">Example 1</span></span>
```powershell
PS C:\> New-AzsOfferDelegation -Name "testofferdelegation" -OfferName "testoffer" -ResourceGroupName "testrg" -TargetSubscriptionId "dbc27112-f67a-4690-ba12-730f71cba018"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer/offerDelegations/testofferdel
                 egation
Location       : redmond
Name           : testoffer/testofferdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cba018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="c4a0a-111">Skapa en ny ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-111">Create a new offer delegation.</span></span>

## <span data-ttu-id="c4a0a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4a0a-112">PARAMETERS</span></span>

### <span data-ttu-id="c4a0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a0a-113">-DefaultProfile</span></span>
<span data-ttu-id="c4a0a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a0a-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="c4a0a-115">-Location</span></span>
<span data-ttu-id="c4a0a-116">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="c4a0a-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c4a0a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4a0a-117">-Name</span></span>
<span data-ttu-id="c4a0a-118">Namn på en ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="c4a0a-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="c4a0a-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="c4a0a-120">Ge ombud.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-120">Offer delegation.</span></span>
<span data-ttu-id="c4a0a-121">För att konstruera kan du läsa avsnittet anteckningar för OFFERDELEGATIONDEFINITION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c4a0a-122">-OfferName</span><span class="sxs-lookup"><span data-stu-id="c4a0a-122">-OfferName</span></span>
<span data-ttu-id="c4a0a-123">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-123">Name of an offer.</span></span>

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

### <span data-ttu-id="c4a0a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a0a-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4a0a-125">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-125">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c4a0a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4a0a-126">-SubscriptionId</span></span>
<span data-ttu-id="c4a0a-127">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c4a0a-128">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4a0a-128">-TargetSubscriptionId</span></span>
<span data-ttu-id="c4a0a-129">ID för det abonnemang som tar emot det delegerade erbjudandet.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-129">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="c4a0a-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4a0a-130">-Confirm</span></span>
<span data-ttu-id="c4a0a-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a0a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a0a-132">-WhatIf</span></span>
<span data-ttu-id="c4a0a-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a0a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a0a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a0a-135">CommonParameters</span></span>
<span data-ttu-id="c4a0a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a0a-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4a0a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a0a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4a0a-138">INPUTS</span></span>

### <span data-ttu-id="c4a0a-139">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c4a0a-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="c4a0a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4a0a-140">OUTPUTS</span></span>

### <span data-ttu-id="c4a0a-141">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c4a0a-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="c4a0a-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c4a0a-142">ALIASES</span></span>

## <span data-ttu-id="c4a0a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4a0a-143">NOTES</span></span>

<span data-ttu-id="c4a0a-144">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4a0a-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c4a0a-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : ge ombud.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="c4a0a-147">`[Location <String>]`: Resursens plats</span><span class="sxs-lookup"><span data-stu-id="c4a0a-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="c4a0a-148">`[SubscriptionId <String>]`: ID för den prenumeration som tar emot det delegerade erbjudandet.</span><span class="sxs-lookup"><span data-stu-id="c4a0a-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="c4a0a-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4a0a-149">RELATED LINKS</span></span>

