---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66d8deb8551dfee98c15fcc5524c993c741bca0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572108"
---
# <span data-ttu-id="9b651-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="9b651-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="9b651-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b651-102">SYNOPSIS</span></span>
<span data-ttu-id="9b651-103">Hämta listan med erbjudanden som operatör.</span><span class="sxs-lookup"><span data-stu-id="9b651-103">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="9b651-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b651-104">SYNTAX</span></span>

### <span data-ttu-id="9b651-105">ListAll (standard)</span><span class="sxs-lookup"><span data-stu-id="9b651-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9b651-106">Lära</span><span class="sxs-lookup"><span data-stu-id="9b651-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="9b651-107">Förteckning</span><span class="sxs-lookup"><span data-stu-id="9b651-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9b651-108">ID</span><span class="sxs-lookup"><span data-stu-id="9b651-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9b651-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b651-109">DESCRIPTION</span></span>
<span data-ttu-id="9b651-110">Hämta listan med erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="9b651-110">Get the list of offers.</span></span>

## <span data-ttu-id="9b651-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b651-111">EXAMPLES</span></span>

### <span data-ttu-id="9b651-112">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9b651-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="9b651-113">Hämta listan med erbjudanden som operatör.</span><span class="sxs-lookup"><span data-stu-id="9b651-113">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="9b651-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b651-114">PARAMETERS</span></span>

### <span data-ttu-id="9b651-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b651-115">-Name</span></span>
<span data-ttu-id="9b651-116">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="9b651-116">Name of an offer.</span></span>

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

### <span data-ttu-id="9b651-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b651-117">-ResourceGroupName</span></span>
<span data-ttu-id="9b651-118">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="9b651-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="9b651-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b651-119">-ResourceId</span></span>
<span data-ttu-id="9b651-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9b651-120">The resource id.</span></span>

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

### <span data-ttu-id="9b651-121">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="9b651-121">-Skip</span></span>
<span data-ttu-id="9b651-122">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="9b651-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9b651-123">-Överst</span><span class="sxs-lookup"><span data-stu-id="9b651-123">-Top</span></span>
<span data-ttu-id="9b651-124">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="9b651-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9b651-125">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="9b651-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9b651-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b651-126">CommonParameters</span></span>
<span data-ttu-id="9b651-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b651-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b651-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b651-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b651-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b651-129">INPUTS</span></span>

## <span data-ttu-id="9b651-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b651-130">OUTPUTS</span></span>

### <span data-ttu-id="9b651-131">Microsoft. AzureStack. Management. abonnemang. admin. Models. erbjuda</span><span class="sxs-lookup"><span data-stu-id="9b651-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="9b651-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b651-132">NOTES</span></span>

## <span data-ttu-id="9b651-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b651-133">RELATED LINKS</span></span>

