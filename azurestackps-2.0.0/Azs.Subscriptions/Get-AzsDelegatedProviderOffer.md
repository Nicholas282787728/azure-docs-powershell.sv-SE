---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsdelegatedprovideroffer
schema: 2.0.0
ms.openlocfilehash: 118834c020a198d355d3f3b9e6dc17699f88e0cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925341"
---
# <span data-ttu-id="8296a-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="8296a-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="8296a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8296a-102">SYNOPSIS</span></span>
<span data-ttu-id="8296a-103">Hämta det angivna anbudet för den delegerade leverantören.</span><span class="sxs-lookup"><span data-stu-id="8296a-103">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="8296a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8296a-104">SYNTAX</span></span>

### <span data-ttu-id="8296a-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8296a-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8296a-106">Lära</span><span class="sxs-lookup"><span data-stu-id="8296a-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> -OfferName <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8296a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8296a-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderOffer -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8296a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8296a-108">DESCRIPTION</span></span>
<span data-ttu-id="8296a-109">Hämta det angivna anbudet för den delegerade leverantören.</span><span class="sxs-lookup"><span data-stu-id="8296a-109">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="8296a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8296a-110">EXAMPLES</span></span>

### <span data-ttu-id="8296a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8296a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d

{{ Add output here }}
```

<span data-ttu-id="8296a-112">Hämta listan med erbjudanden för den angivna delegerade providern</span><span class="sxs-lookup"><span data-stu-id="8296a-112">Get the list of offers for the specified delegated provider</span></span>

## <span data-ttu-id="8296a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8296a-113">PARAMETERS</span></span>

### <span data-ttu-id="8296a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8296a-114">-DefaultProfile</span></span>
<span data-ttu-id="8296a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8296a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8296a-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="8296a-116">-DelegatedProviderId</span></span>
<span data-ttu-id="8296a-117">ID för den delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="8296a-117">Id of the delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8296a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8296a-118">-InputObject</span></span>
<span data-ttu-id="8296a-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8296a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8296a-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="8296a-120">-OfferName</span></span>
<span data-ttu-id="8296a-121">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="8296a-121">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8296a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8296a-122">CommonParameters</span></span>
<span data-ttu-id="8296a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8296a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8296a-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8296a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8296a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8296a-125">INPUTS</span></span>

### <span data-ttu-id="8296a-126">Microsoft. Azure. PowerShell. cmdletar. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="8296a-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="8296a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8296a-127">OUTPUTS</span></span>

### <span data-ttu-id="8296a-128">Microsoft. Azure. PowerShell. cmdletar. Subscription. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="8296a-128">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="8296a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8296a-129">NOTES</span></span>

<span data-ttu-id="8296a-130">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8296a-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8296a-131">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8296a-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8296a-132">INPUTOBJECT <ISubscriptionIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8296a-132">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8296a-133">`[DelegatedProviderId <String>]`: ID för den delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="8296a-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="8296a-134">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8296a-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8296a-135">`[OfferName <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="8296a-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="8296a-136">`[SubscriptionId <String>]`: ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8296a-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="8296a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8296a-137">RELATED LINKS</span></span>

