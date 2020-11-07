---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b280b9e99fa91c53371d2eff38d42003873951bb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921825"
---
# <span data-ttu-id="93184-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="93184-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="93184-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93184-102">SYNOPSIS</span></span>
<span data-ttu-id="93184-103">Få en lista över alla belastnings utjämningar.</span><span class="sxs-lookup"><span data-stu-id="93184-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="93184-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93184-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="93184-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93184-105">DESCRIPTION</span></span>
<span data-ttu-id="93184-106">Få en lista över alla belastnings utjämningar.</span><span class="sxs-lookup"><span data-stu-id="93184-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="93184-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93184-107">EXAMPLES</span></span>

### <span data-ttu-id="93184-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="93184-108">EXAMPLE 1</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="93184-109">Få en lista över alla belastnings utjämningar.</span><span class="sxs-lookup"><span data-stu-id="93184-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="93184-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93184-110">PARAMETERS</span></span>

### <span data-ttu-id="93184-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="93184-111">-Filter</span></span>
<span data-ttu-id="93184-112">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="93184-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="93184-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="93184-113">-OrderBy</span></span>
<span data-ttu-id="93184-114">OData orderBy-parameter.</span><span class="sxs-lookup"><span data-stu-id="93184-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="93184-115">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="93184-115">-Skip</span></span>
<span data-ttu-id="93184-116">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="93184-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="93184-117">-Överst</span><span class="sxs-lookup"><span data-stu-id="93184-117">-Top</span></span>
<span data-ttu-id="93184-118">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="93184-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="93184-119">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="93184-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="93184-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="93184-120">-InlineCount</span></span>
<span data-ttu-id="93184-121">Parameter för OData-antal.</span><span class="sxs-lookup"><span data-stu-id="93184-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="93184-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93184-122">CommonParameters</span></span>
<span data-ttu-id="93184-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93184-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93184-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93184-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93184-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93184-125">INPUTS</span></span>

## <span data-ttu-id="93184-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93184-126">OUTPUTS</span></span>

### <span data-ttu-id="93184-127">Microsoft. AzureStack. Management. Network. admin. Models. LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="93184-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="93184-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93184-128">NOTES</span></span>

## <span data-ttu-id="93184-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93184-129">RELATED LINKS</span></span>
