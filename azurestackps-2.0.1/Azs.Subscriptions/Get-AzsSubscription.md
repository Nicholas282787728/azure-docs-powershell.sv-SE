---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azssubscription
schema: 2.0.0
ms.openlocfilehash: 7dce95be9a936d341e0f063fd6d89701b18c2ce7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092900"
---
# <span data-ttu-id="e6a47-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="e6a47-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="e6a47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6a47-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a47-103">Hämtar information om vissa abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e6a47-103">Gets details about particular subscription.</span></span>

## <span data-ttu-id="e6a47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6a47-104">SYNTAX</span></span>

### <span data-ttu-id="e6a47-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="e6a47-105">List (Default)</span></span>
```
Get-AzsSubscription [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e6a47-106">Lära</span><span class="sxs-lookup"><span data-stu-id="e6a47-106">Get</span></span>
```
Get-AzsSubscription -SubscriptionId <String[]> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e6a47-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e6a47-107">GetViaIdentity</span></span>
```
Get-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e6a47-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6a47-108">DESCRIPTION</span></span>
<span data-ttu-id="e6a47-109">Hämtar information om vissa abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e6a47-109">Gets details about particular subscription.</span></span>

## <span data-ttu-id="e6a47-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6a47-110">EXAMPLES</span></span>

### <span data-ttu-id="e6a47-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e6a47-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsSubscription | fl *

DisplayName    : Test User
Id             : /subscriptions/97d84f7a-bef7-4f2d-b651-c553be472311
OfferId        : /delegatedProviders/default/offers/TestOffer-590376ac-c8dd-4b3d-9674-b5b8fcde095b
State          : Enabled
SubscriptionId : 97d84f7a-bef7-4f2d-b651-c553be472311
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb

DisplayName    : cnur
Id             : /subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId        : /delegatedProviders/default/offers/cnur4866tenantsubsvcoffer843
State          : Enabled
SubscriptionId : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="e6a47-112">Hämta listan med prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="e6a47-112">Get the list of subscriptions.</span></span>

## <span data-ttu-id="e6a47-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6a47-113">PARAMETERS</span></span>

### <span data-ttu-id="e6a47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a47-114">-DefaultProfile</span></span>
<span data-ttu-id="e6a47-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a47-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6a47-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6a47-116">-InputObject</span></span>
<span data-ttu-id="e6a47-117">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e6a47-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e6a47-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6a47-118">-SubscriptionId</span></span>
<span data-ttu-id="e6a47-119">ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e6a47-119">Id of the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e6a47-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a47-120">CommonParameters</span></span>
<span data-ttu-id="e6a47-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a47-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a47-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6a47-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a47-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6a47-123">INPUTS</span></span>

### <span data-ttu-id="e6a47-124">Microsoft. Azure. PowerShell. cmdletar. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="e6a47-124">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="e6a47-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6a47-125">OUTPUTS</span></span>

### <span data-ttu-id="e6a47-126">Microsoft. Azure. PowerShell. cmdletar. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="e6a47-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="e6a47-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6a47-127">NOTES</span></span>

<span data-ttu-id="e6a47-128">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e6a47-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6a47-129">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e6a47-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e6a47-130">INPUTOBJECT <ISubscriptionIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e6a47-130">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e6a47-131">`[DelegatedProviderId <String>]`: ID för den delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="e6a47-131">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="e6a47-132">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e6a47-132">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e6a47-133">`[OfferName <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="e6a47-133">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="e6a47-134">`[SubscriptionId <String>]`: ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e6a47-134">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="e6a47-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6a47-135">RELATED LINKS</span></span>
