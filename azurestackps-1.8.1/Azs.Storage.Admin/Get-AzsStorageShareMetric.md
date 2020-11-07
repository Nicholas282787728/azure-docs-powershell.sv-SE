---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 80c80cb38013701d3e58d6d6bf77f774e2d61548
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921894"
---
# <span data-ttu-id="c0502-101">Get-AzsStorageShareMetric</span><span class="sxs-lookup"><span data-stu-id="c0502-101">Get-AzsStorageShareMetric</span></span>

## <span data-ttu-id="c0502-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0502-102">SYNOPSIS</span></span>
<span data-ttu-id="c0502-103">Returnerar en lista med mät värden för en lagrings resurs.</span><span class="sxs-lookup"><span data-stu-id="c0502-103">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="c0502-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0502-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetric [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c0502-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0502-105">DESCRIPTION</span></span>
<span data-ttu-id="c0502-106">Returnerar en lista med mät värden för en lagrings resurs.</span><span class="sxs-lookup"><span data-stu-id="c0502-106">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="c0502-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0502-107">EXAMPLES</span></span>

### <span data-ttu-id="c0502-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="c0502-108">EXAMPLE 1</span></span>
```
Get-AzsStorageShareMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="c0502-109">Få en lista över Mät värden för en lagrings resurs.</span><span class="sxs-lookup"><span data-stu-id="c0502-109">Get the list of metrics for a storage share.</span></span>

## <span data-ttu-id="c0502-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0502-110">PARAMETERS</span></span>

### <span data-ttu-id="c0502-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="c0502-111">-FarmName</span></span>
<span data-ttu-id="c0502-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="c0502-112">Farm Id.</span></span>

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

### <span data-ttu-id="c0502-113">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c0502-113">-ShareName</span></span>
<span data-ttu-id="c0502-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c0502-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0502-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0502-115">-ResourceGroupName</span></span>
<span data-ttu-id="c0502-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c0502-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0502-117">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="c0502-117">-Skip</span></span>
<span data-ttu-id="c0502-118">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="c0502-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c0502-119">-Överst</span><span class="sxs-lookup"><span data-stu-id="c0502-119">-Top</span></span>
<span data-ttu-id="c0502-120">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="c0502-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c0502-121">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="c0502-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0502-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0502-122">CommonParameters</span></span>
<span data-ttu-id="c0502-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0502-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0502-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0502-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0502-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0502-125">INPUTS</span></span>

## <span data-ttu-id="c0502-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0502-126">OUTPUTS</span></span>

### <span data-ttu-id="c0502-127">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="c0502-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="c0502-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0502-128">NOTES</span></span>

## <span data-ttu-id="c0502-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0502-129">RELATED LINKS</span></span>
