---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac33f0feae7d54798753637f8f7898ab796f0939
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572036"
---
# <span data-ttu-id="c2a1b-101">Get-AzsQueueServiceMetric</span><span class="sxs-lookup"><span data-stu-id="c2a1b-101">Get-AzsQueueServiceMetric</span></span>

## <span data-ttu-id="c2a1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a1b-103">Returnerar en lista med mät värden för kötjänsten.</span><span class="sxs-lookup"><span data-stu-id="c2a1b-103">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="c2a1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2a1b-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2a1b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="c2a1b-106">Returnerar en lista med mät värden för kötjänsten.</span><span class="sxs-lookup"><span data-stu-id="c2a1b-106">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="c2a1b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2a1b-107">EXAMPLES</span></span>

### <span data-ttu-id="c2a1b-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c2a1b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="c2a1b-109">Få en lista över Mät värden för kötjänsten.</span><span class="sxs-lookup"><span data-stu-id="c2a1b-109">Get the list of metrics for queue service.</span></span>

## <span data-ttu-id="c2a1b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2a1b-110">PARAMETERS</span></span>

### <span data-ttu-id="c2a1b-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="c2a1b-111">-FarmName</span></span>
<span data-ttu-id="c2a1b-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="c2a1b-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2a1b-113">-ResourceGroupName</span></span>
<span data-ttu-id="c2a1b-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c2a1b-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1b-115">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="c2a1b-115">-Skip</span></span>
<span data-ttu-id="c2a1b-116">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="c2a1b-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1b-117">-Överst</span><span class="sxs-lookup"><span data-stu-id="c2a1b-117">-Top</span></span>
<span data-ttu-id="c2a1b-118">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="c2a1b-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c2a1b-119">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="c2a1b-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a1b-120">CommonParameters</span></span>
<span data-ttu-id="c2a1b-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a1b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a1b-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2a1b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a1b-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2a1b-123">INPUTS</span></span>

## <span data-ttu-id="c2a1b-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2a1b-124">OUTPUTS</span></span>

### <span data-ttu-id="c2a1b-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="c2a1b-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="c2a1b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2a1b-126">NOTES</span></span>

## <span data-ttu-id="c2a1b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2a1b-127">RELATED LINKS</span></span>

