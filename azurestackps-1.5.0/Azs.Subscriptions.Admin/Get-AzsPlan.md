---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75fef110a1266ca34bef645f39a879dda4aeeda4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571399"
---
# <span data-ttu-id="37e3f-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="37e3f-101">Get-AzsPlan</span></span>

## <span data-ttu-id="37e3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="37e3f-103">Lista alla abonnemang för alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="37e3f-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="37e3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37e3f-104">SYNTAX</span></span>

### <span data-ttu-id="37e3f-105">ListAll (standard)</span><span class="sxs-lookup"><span data-stu-id="37e3f-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="37e3f-106">Lära</span><span class="sxs-lookup"><span data-stu-id="37e3f-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="37e3f-107">Förteckning</span><span class="sxs-lookup"><span data-stu-id="37e3f-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="37e3f-108">ID</span><span class="sxs-lookup"><span data-stu-id="37e3f-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="37e3f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37e3f-109">DESCRIPTION</span></span>
<span data-ttu-id="37e3f-110">Lista alla abonnemang för alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="37e3f-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="37e3f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37e3f-111">EXAMPLES</span></span>

### <span data-ttu-id="37e3f-112">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="37e3f-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="37e3f-113">Skaffa ett specifik abonnemang under dessa abonnemang.</span><span class="sxs-lookup"><span data-stu-id="37e3f-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="37e3f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37e3f-114">PARAMETERS</span></span>

### <span data-ttu-id="37e3f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="37e3f-115">-Name</span></span>
<span data-ttu-id="37e3f-116">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="37e3f-116">Name of the plan.</span></span>

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

### <span data-ttu-id="37e3f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e3f-117">-ResourceGroupName</span></span>
<span data-ttu-id="37e3f-118">Namnet på resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="37e3f-118">The name of the resource group the resource is located under.</span></span>

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

### <span data-ttu-id="37e3f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37e3f-119">-ResourceId</span></span>
<span data-ttu-id="37e3f-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="37e3f-120">The resource id.</span></span>

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

### <span data-ttu-id="37e3f-121">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="37e3f-121">-Skip</span></span>
<span data-ttu-id="37e3f-122">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="37e3f-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="37e3f-123">-Överst</span><span class="sxs-lookup"><span data-stu-id="37e3f-123">-Top</span></span>
<span data-ttu-id="37e3f-124">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="37e3f-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="37e3f-125">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="37e3f-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="37e3f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e3f-126">CommonParameters</span></span>
<span data-ttu-id="37e3f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e3f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e3f-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37e3f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e3f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37e3f-129">INPUTS</span></span>

## <span data-ttu-id="37e3f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37e3f-130">OUTPUTS</span></span>

### <span data-ttu-id="37e3f-131">Microsoft. AzureStack. Management. abonnemang. admin. Models. plan</span><span class="sxs-lookup"><span data-stu-id="37e3f-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="37e3f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37e3f-132">NOTES</span></span>

## <span data-ttu-id="37e3f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37e3f-133">RELATED LINKS</span></span>

