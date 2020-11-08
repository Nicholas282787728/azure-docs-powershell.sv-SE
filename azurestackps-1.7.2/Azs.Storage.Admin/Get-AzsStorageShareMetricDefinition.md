---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 646ee96dec361ac6318b4cfe48b80ec4c3686321
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921084"
---
# <span data-ttu-id="38118-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="38118-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="38118-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38118-102">SYNOPSIS</span></span>
<span data-ttu-id="38118-103">Returnerar en lista med mått definitioner för en lagrings resurs.</span><span class="sxs-lookup"><span data-stu-id="38118-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="38118-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38118-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-Name] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="38118-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38118-105">DESCRIPTION</span></span>
<span data-ttu-id="38118-106">Returnerar en lista med mått definitioner för en lagrings resurs.</span><span class="sxs-lookup"><span data-stu-id="38118-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="38118-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38118-107">EXAMPLES</span></span>

### <span data-ttu-id="38118-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="38118-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Name "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="38118-109">Hämta listan med mått definitioner för en lagrings resurs.</span><span class="sxs-lookup"><span data-stu-id="38118-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="38118-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38118-110">PARAMETERS</span></span>

### <span data-ttu-id="38118-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="38118-111">-FarmName</span></span>
<span data-ttu-id="38118-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="38118-112">Farm Id.</span></span>

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

### <span data-ttu-id="38118-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="38118-113">-Name</span></span>
<span data-ttu-id="38118-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="38118-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38118-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38118-115">-ResourceGroupName</span></span>
<span data-ttu-id="38118-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="38118-116">Resource group name.</span></span>

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

### <span data-ttu-id="38118-117">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="38118-117">-Skip</span></span>
<span data-ttu-id="38118-118">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="38118-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="38118-119">-Överst</span><span class="sxs-lookup"><span data-stu-id="38118-119">-Top</span></span>
<span data-ttu-id="38118-120">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="38118-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="38118-121">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="38118-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="38118-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38118-122">CommonParameters</span></span>
<span data-ttu-id="38118-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38118-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38118-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38118-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38118-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38118-125">INPUTS</span></span>

## <span data-ttu-id="38118-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38118-126">OUTPUTS</span></span>

### <span data-ttu-id="38118-127">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="38118-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="38118-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38118-128">NOTES</span></span>

## <span data-ttu-id="38118-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38118-129">RELATED LINKS</span></span>
