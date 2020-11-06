---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b43acb45bc5b606303cbd33c20f0975919bb6b59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572519"
---
# <span data-ttu-id="901ea-101">Get-AzsBlobServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="901ea-101">Get-AzsBlobServiceMetricDefinition</span></span>

## <span data-ttu-id="901ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="901ea-102">SYNOPSIS</span></span>
<span data-ttu-id="901ea-103">Returnerar listan över mått definitioner för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="901ea-103">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="901ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="901ea-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="901ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="901ea-105">DESCRIPTION</span></span>
<span data-ttu-id="901ea-106">Returnerar listan över mått definitioner för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="901ea-106">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="901ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="901ea-107">EXAMPLES</span></span>

### <span data-ttu-id="901ea-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="901ea-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="901ea-109">Få en lista över mått definitioner för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="901ea-109">Get a list of metric definitions for the blob service.</span></span>

## <span data-ttu-id="901ea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="901ea-110">PARAMETERS</span></span>

### <span data-ttu-id="901ea-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="901ea-111">-FarmName</span></span>
<span data-ttu-id="901ea-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="901ea-112">Farm Id.</span></span>

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

### <span data-ttu-id="901ea-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="901ea-113">-ResourceGroupName</span></span>
<span data-ttu-id="901ea-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="901ea-114">Resource group name.</span></span>

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

### <span data-ttu-id="901ea-115">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="901ea-115">-Skip</span></span>
<span data-ttu-id="901ea-116">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="901ea-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="901ea-117">-Överst</span><span class="sxs-lookup"><span data-stu-id="901ea-117">-Top</span></span>
<span data-ttu-id="901ea-118">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="901ea-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="901ea-119">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="901ea-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="901ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901ea-120">CommonParameters</span></span>
<span data-ttu-id="901ea-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="901ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901ea-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="901ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901ea-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="901ea-123">INPUTS</span></span>

## <span data-ttu-id="901ea-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="901ea-124">OUTPUTS</span></span>

### <span data-ttu-id="901ea-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="901ea-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="901ea-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="901ea-126">NOTES</span></span>

## <span data-ttu-id="901ea-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="901ea-127">RELATED LINKS</span></span>

