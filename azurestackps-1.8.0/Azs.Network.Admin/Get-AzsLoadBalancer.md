---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b280b9e99fa91c53371d2eff38d42003873951bb
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921542"
---
# <span data-ttu-id="bbf6d-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbf6d-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="bbf6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbf6d-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf6d-103">Få en lista över alla belastnings utjämningar.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="bbf6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbf6d-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="bbf6d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbf6d-105">DESCRIPTION</span></span>
<span data-ttu-id="bbf6d-106">Få en lista över alla belastnings utjämningar.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="bbf6d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbf6d-107">EXAMPLES</span></span>

### <span data-ttu-id="bbf6d-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="bbf6d-108">EXAMPLE 1</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="bbf6d-109">Få en lista över alla belastnings utjämningar.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="bbf6d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbf6d-110">PARAMETERS</span></span>

### <span data-ttu-id="bbf6d-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="bbf6d-111">-Filter</span></span>
<span data-ttu-id="bbf6d-112">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="bbf6d-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="bbf6d-113">-OrderBy</span></span>
<span data-ttu-id="bbf6d-114">OData orderBy-parameter.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="bbf6d-115">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="bbf6d-115">-Skip</span></span>
<span data-ttu-id="bbf6d-116">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bbf6d-117">-Överst</span><span class="sxs-lookup"><span data-stu-id="bbf6d-117">-Top</span></span>
<span data-ttu-id="bbf6d-118">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bbf6d-119">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bbf6d-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="bbf6d-120">-InlineCount</span></span>
<span data-ttu-id="bbf6d-121">Parameter för OData-antal.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="bbf6d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf6d-122">CommonParameters</span></span>
<span data-ttu-id="bbf6d-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf6d-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbf6d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf6d-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbf6d-125">INPUTS</span></span>

## <span data-ttu-id="bbf6d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbf6d-126">OUTPUTS</span></span>

### <span data-ttu-id="bbf6d-127">Microsoft. AzureStack. Management. Network. admin. Models. LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbf6d-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="bbf6d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbf6d-128">NOTES</span></span>

## <span data-ttu-id="bbf6d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbf6d-129">RELATED LINKS</span></span>
