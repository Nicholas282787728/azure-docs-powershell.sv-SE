---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95ea9afa5d3dce953f4e51e84d011886e4ba5688
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921567"
---
# <span data-ttu-id="e9694-101">Get-AzsStorageFarmMetric</span><span class="sxs-lookup"><span data-stu-id="e9694-101">Get-AzsStorageFarmMetric</span></span>

## <span data-ttu-id="e9694-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9694-102">SYNOPSIS</span></span>
<span data-ttu-id="e9694-103">Returnerar en lista över mått för lagrings grupper.</span><span class="sxs-lookup"><span data-stu-id="e9694-103">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="e9694-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9694-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9694-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9694-105">DESCRIPTION</span></span>
<span data-ttu-id="e9694-106">Returnerar en lista över mått för lagrings grupper.</span><span class="sxs-lookup"><span data-stu-id="e9694-106">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="e9694-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9694-107">EXAMPLES</span></span>

### <span data-ttu-id="e9694-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e9694-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarmMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="e9694-109">Skaffa en lista över lagrings mått.</span><span class="sxs-lookup"><span data-stu-id="e9694-109">Get the list of storage farm metrics.</span></span>

## <span data-ttu-id="e9694-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9694-110">PARAMETERS</span></span>

### <span data-ttu-id="e9694-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="e9694-111">-FarmName</span></span>
<span data-ttu-id="e9694-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="e9694-112">Farm Id.</span></span>

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

### <span data-ttu-id="e9694-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9694-113">-ResourceGroupName</span></span>
<span data-ttu-id="e9694-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e9694-114">Resource group name.</span></span>

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

### <span data-ttu-id="e9694-115">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="e9694-115">-Skip</span></span>
<span data-ttu-id="e9694-116">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="e9694-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e9694-117">-Överst</span><span class="sxs-lookup"><span data-stu-id="e9694-117">-Top</span></span>
<span data-ttu-id="e9694-118">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="e9694-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e9694-119">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="e9694-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e9694-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9694-120">CommonParameters</span></span>
<span data-ttu-id="e9694-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9694-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9694-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9694-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9694-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9694-123">INPUTS</span></span>

## <span data-ttu-id="e9694-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9694-124">OUTPUTS</span></span>

### <span data-ttu-id="e9694-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="e9694-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="e9694-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9694-126">NOTES</span></span>

## <span data-ttu-id="e9694-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9694-127">RELATED LINKS</span></span>

