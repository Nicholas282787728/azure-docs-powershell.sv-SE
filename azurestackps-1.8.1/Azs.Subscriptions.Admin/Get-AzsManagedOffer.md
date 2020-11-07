---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e30a1501cb5df34dc8f8b2ab51041f867a5ee6c1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921873"
---
# <span data-ttu-id="eb8d6-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="eb8d6-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="eb8d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8d6-103">Få en lista med erbjudanden som administratör.</span><span class="sxs-lookup"><span data-stu-id="eb8d6-103">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="eb8d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb8d6-104">SYNTAX</span></span>

### <span data-ttu-id="eb8d6-105">ListAll (standard)</span><span class="sxs-lookup"><span data-stu-id="eb8d6-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="eb8d6-106">Lära</span><span class="sxs-lookup"><span data-stu-id="eb8d6-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="eb8d6-107">Förteckning</span><span class="sxs-lookup"><span data-stu-id="eb8d6-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="eb8d6-108">ID</span><span class="sxs-lookup"><span data-stu-id="eb8d6-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="eb8d6-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb8d6-109">DESCRIPTION</span></span>
<span data-ttu-id="eb8d6-110">Hämta listan med erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="eb8d6-110">Get the list of offers.</span></span>

## <span data-ttu-id="eb8d6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb8d6-111">EXAMPLES</span></span>

### <span data-ttu-id="eb8d6-112">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eb8d6-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="eb8d6-113">Få en lista med erbjudanden som administratör.</span><span class="sxs-lookup"><span data-stu-id="eb8d6-113">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="eb8d6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb8d6-114">PARAMETERS</span></span>

### <span data-ttu-id="eb8d6-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb8d6-115">-Name</span></span>
<span data-ttu-id="eb8d6-116">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="eb8d6-116">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8d6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb8d6-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb8d6-118">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="eb8d6-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8d6-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb8d6-119">-ResourceId</span></span>
<span data-ttu-id="eb8d6-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="eb8d6-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8d6-121">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="eb8d6-121">-Skip</span></span>
<span data-ttu-id="eb8d6-122">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="eb8d6-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8d6-123">-Överst</span><span class="sxs-lookup"><span data-stu-id="eb8d6-123">-Top</span></span>
<span data-ttu-id="eb8d6-124">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="eb8d6-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="eb8d6-125">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="eb8d6-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8d6-126">CommonParameters</span></span>
<span data-ttu-id="eb8d6-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb8d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8d6-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8d6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8d6-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb8d6-129">INPUTS</span></span>

## <span data-ttu-id="eb8d6-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb8d6-130">OUTPUTS</span></span>

### <span data-ttu-id="eb8d6-131">Microsoft. AzureStack. Management. abonnemang. admin. Models. erbjuda</span><span class="sxs-lookup"><span data-stu-id="eb8d6-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="eb8d6-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb8d6-132">NOTES</span></span>

## <span data-ttu-id="eb8d6-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb8d6-133">RELATED LINKS</span></span>

