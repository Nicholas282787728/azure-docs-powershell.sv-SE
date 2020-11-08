---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb583ca37f610d47c880fd2e15ae3e7b8182b5ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920987"
---
# <span data-ttu-id="6bed1-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="6bed1-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="6bed1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6bed1-102">SYNOPSIS</span></span>
<span data-ttu-id="6bed1-103">Få en samling av alla hämtade abonnemang som abonnemanget har åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="6bed1-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="6bed1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6bed1-104">SYNTAX</span></span>

### <span data-ttu-id="6bed1-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="6bed1-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6bed1-106">Lära</span><span class="sxs-lookup"><span data-stu-id="6bed1-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="6bed1-107">ID</span><span class="sxs-lookup"><span data-stu-id="6bed1-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6bed1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6bed1-108">DESCRIPTION</span></span>
<span data-ttu-id="6bed1-109">Få en samling av alla hämtade abonnemang som abonnemanget har åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="6bed1-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="6bed1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6bed1-110">EXAMPLES</span></span>

### <span data-ttu-id="6bed1-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6bed1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="6bed1-112">Få en samling av alla hämtade abonnemang som abonnemanget har åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="6bed1-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="6bed1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6bed1-113">PARAMETERS</span></span>

### <span data-ttu-id="6bed1-114">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="6bed1-114">-AcquisitionId</span></span>
<span data-ttu-id="6bed1-115">Abonnemangets anskaffnings identifierare</span><span class="sxs-lookup"><span data-stu-id="6bed1-115">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bed1-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bed1-116">-ResourceId</span></span>
<span data-ttu-id="6bed1-117">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6bed1-117">The resource id.</span></span>

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

### <span data-ttu-id="6bed1-118">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="6bed1-118">-Skip</span></span>
<span data-ttu-id="6bed1-119">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="6bed1-119">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bed1-120">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6bed1-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="6bed1-121">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6bed1-121">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bed1-122">-Överst</span><span class="sxs-lookup"><span data-stu-id="6bed1-122">-Top</span></span>
<span data-ttu-id="6bed1-123">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="6bed1-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6bed1-124">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="6bed1-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bed1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bed1-125">CommonParameters</span></span>
<span data-ttu-id="6bed1-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bed1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bed1-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bed1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bed1-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6bed1-128">INPUTS</span></span>

## <span data-ttu-id="6bed1-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6bed1-129">OUTPUTS</span></span>

### <span data-ttu-id="6bed1-130">Microsoft. AzureStack. Management. abonnemang. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="6bed1-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="6bed1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6bed1-131">NOTES</span></span>

## <span data-ttu-id="6bed1-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6bed1-132">RELATED LINKS</span></span>
