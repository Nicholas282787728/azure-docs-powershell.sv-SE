---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e127b0cb9198471d237df62bfedf8d2d57ecdca2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100321"
---
# <span data-ttu-id="79af9-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="79af9-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="79af9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79af9-102">SYNOPSIS</span></span>
<span data-ttu-id="79af9-103">Returnerar en lista med mått definitioner för en lagrings resurs.</span><span class="sxs-lookup"><span data-stu-id="79af9-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="79af9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79af9-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="79af9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79af9-105">DESCRIPTION</span></span>
<span data-ttu-id="79af9-106">Returnerar en lista med mått definitioner för en lagrings resurs.</span><span class="sxs-lookup"><span data-stu-id="79af9-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="79af9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79af9-107">EXAMPLES</span></span>

### <span data-ttu-id="79af9-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="79af9-108">EXAMPLE 1</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="79af9-109">Hämta listan med mått definitioner för en lagrings resurs.</span><span class="sxs-lookup"><span data-stu-id="79af9-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="79af9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79af9-110">PARAMETERS</span></span>

### <span data-ttu-id="79af9-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="79af9-111">-FarmName</span></span>
<span data-ttu-id="79af9-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="79af9-112">Farm Id.</span></span>

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

### <span data-ttu-id="79af9-113">-ShareName</span><span class="sxs-lookup"><span data-stu-id="79af9-113">-ShareName</span></span>
<span data-ttu-id="79af9-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="79af9-114">Share name.</span></span>

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

### <span data-ttu-id="79af9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79af9-115">-ResourceGroupName</span></span>
<span data-ttu-id="79af9-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="79af9-116">Resource group name.</span></span>

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

### <span data-ttu-id="79af9-117">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="79af9-117">-Skip</span></span>
<span data-ttu-id="79af9-118">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="79af9-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="79af9-119">-Överst</span><span class="sxs-lookup"><span data-stu-id="79af9-119">-Top</span></span>
<span data-ttu-id="79af9-120">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="79af9-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="79af9-121">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="79af9-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="79af9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79af9-122">CommonParameters</span></span>
<span data-ttu-id="79af9-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79af9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79af9-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79af9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79af9-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79af9-125">INPUTS</span></span>

## <span data-ttu-id="79af9-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79af9-126">OUTPUTS</span></span>

### <span data-ttu-id="79af9-127">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="79af9-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="79af9-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79af9-128">NOTES</span></span>

## <span data-ttu-id="79af9-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79af9-129">RELATED LINKS</span></span>
