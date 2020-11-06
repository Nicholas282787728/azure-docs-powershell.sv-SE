---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43691cfa3299fc0534ce2d44fd2a2f6ed1043d04
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572244"
---
# <span data-ttu-id="70fbd-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70fbd-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="70fbd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="70fbd-103">Få en lista över alla virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="70fbd-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="70fbd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70fbd-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="70fbd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="70fbd-106">Få en lista över alla virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="70fbd-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="70fbd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70fbd-107">EXAMPLES</span></span>

### <span data-ttu-id="70fbd-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="70fbd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="70fbd-109">Returnera en lista med virtuella nätverk för Azure-huvudstämpeln.</span><span class="sxs-lookup"><span data-stu-id="70fbd-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="70fbd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70fbd-110">PARAMETERS</span></span>

### <span data-ttu-id="70fbd-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="70fbd-111">-Filter</span></span>
<span data-ttu-id="70fbd-112">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="70fbd-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="70fbd-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="70fbd-113">-InlineCount</span></span>
<span data-ttu-id="70fbd-114">Parameter för OData-antal.</span><span class="sxs-lookup"><span data-stu-id="70fbd-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="70fbd-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="70fbd-115">-OrderBy</span></span>
<span data-ttu-id="70fbd-116">OData orderBy-parameter.</span><span class="sxs-lookup"><span data-stu-id="70fbd-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="70fbd-117">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="70fbd-117">-Skip</span></span>
<span data-ttu-id="70fbd-118">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="70fbd-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="70fbd-119">-Överst</span><span class="sxs-lookup"><span data-stu-id="70fbd-119">-Top</span></span>
<span data-ttu-id="70fbd-120">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="70fbd-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="70fbd-121">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="70fbd-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="70fbd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70fbd-122">CommonParameters</span></span>
<span data-ttu-id="70fbd-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70fbd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70fbd-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70fbd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70fbd-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70fbd-125">INPUTS</span></span>

## <span data-ttu-id="70fbd-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70fbd-126">OUTPUTS</span></span>

### <span data-ttu-id="70fbd-127">Microsoft. AzureStack. Management. Network. admin. Models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70fbd-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="70fbd-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70fbd-128">NOTES</span></span>

## <span data-ttu-id="70fbd-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70fbd-129">RELATED LINKS</span></span>

