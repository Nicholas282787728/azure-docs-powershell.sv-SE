---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af35419f3e0b28be9782e7bbe5d4eaaf1cdf0807
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921820"
---
# <span data-ttu-id="bf992-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bf992-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="bf992-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf992-102">SYNOPSIS</span></span>
<span data-ttu-id="bf992-103">Få en lista över alla virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="bf992-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="bf992-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf992-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="bf992-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf992-105">DESCRIPTION</span></span>
<span data-ttu-id="bf992-106">Få en lista över alla virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="bf992-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="bf992-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf992-107">EXAMPLES</span></span>

### <span data-ttu-id="bf992-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="bf992-108">EXAMPLE 1</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="bf992-109">Returnera en lista med virtuella nätverk för Azure-huvudstämpeln.</span><span class="sxs-lookup"><span data-stu-id="bf992-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="bf992-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf992-110">PARAMETERS</span></span>

### <span data-ttu-id="bf992-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="bf992-111">-Filter</span></span>
<span data-ttu-id="bf992-112">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="bf992-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="bf992-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="bf992-113">-OrderBy</span></span>
<span data-ttu-id="bf992-114">OData orderBy-parameter.</span><span class="sxs-lookup"><span data-stu-id="bf992-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="bf992-115">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="bf992-115">-Skip</span></span>
<span data-ttu-id="bf992-116">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="bf992-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bf992-117">-Överst</span><span class="sxs-lookup"><span data-stu-id="bf992-117">-Top</span></span>
<span data-ttu-id="bf992-118">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="bf992-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bf992-119">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="bf992-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bf992-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="bf992-120">-InlineCount</span></span>
<span data-ttu-id="bf992-121">Parameter för OData-antal.</span><span class="sxs-lookup"><span data-stu-id="bf992-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="bf992-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf992-122">CommonParameters</span></span>
<span data-ttu-id="bf992-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf992-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf992-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf992-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf992-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf992-125">INPUTS</span></span>

## <span data-ttu-id="bf992-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf992-126">OUTPUTS</span></span>

### <span data-ttu-id="bf992-127">Microsoft. AzureStack. Management. Network. admin. Models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bf992-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="bf992-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf992-128">NOTES</span></span>

## <span data-ttu-id="bf992-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf992-129">RELATED LINKS</span></span>
