---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87966f8ac96ab70f7617f857d9f1d83945b5e639
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920998"
---
# <span data-ttu-id="b7a01-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7a01-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="b7a01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7a01-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a01-103">Få en lista över alla belastnings utjämningar.</span><span class="sxs-lookup"><span data-stu-id="b7a01-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="b7a01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7a01-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b7a01-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7a01-105">DESCRIPTION</span></span>
<span data-ttu-id="b7a01-106">Få en lista över alla belastnings utjämningar.</span><span class="sxs-lookup"><span data-stu-id="b7a01-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="b7a01-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7a01-107">EXAMPLES</span></span>

### <span data-ttu-id="b7a01-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b7a01-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="b7a01-109">Få en lista över alla belastnings utjämningar.</span><span class="sxs-lookup"><span data-stu-id="b7a01-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="b7a01-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7a01-110">PARAMETERS</span></span>

### <span data-ttu-id="b7a01-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="b7a01-111">-Filter</span></span>
<span data-ttu-id="b7a01-112">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="b7a01-112">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a01-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="b7a01-113">-InlineCount</span></span>
<span data-ttu-id="b7a01-114">Parameter för OData-antal.</span><span class="sxs-lookup"><span data-stu-id="b7a01-114">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a01-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b7a01-115">-OrderBy</span></span>
<span data-ttu-id="b7a01-116">OData orderBy-parameter.</span><span class="sxs-lookup"><span data-stu-id="b7a01-116">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a01-117">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="b7a01-117">-Skip</span></span>
<span data-ttu-id="b7a01-118">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b7a01-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a01-119">-Överst</span><span class="sxs-lookup"><span data-stu-id="b7a01-119">-Top</span></span>
<span data-ttu-id="b7a01-120">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b7a01-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b7a01-121">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="b7a01-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a01-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a01-122">CommonParameters</span></span>
<span data-ttu-id="b7a01-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a01-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a01-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7a01-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a01-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7a01-125">INPUTS</span></span>

## <span data-ttu-id="b7a01-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7a01-126">OUTPUTS</span></span>

### <span data-ttu-id="b7a01-127">Microsoft. AzureStack. Management. Network. admin. Models. LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b7a01-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="b7a01-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7a01-128">NOTES</span></span>

## <span data-ttu-id="b7a01-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7a01-129">RELATED LINKS</span></span>
