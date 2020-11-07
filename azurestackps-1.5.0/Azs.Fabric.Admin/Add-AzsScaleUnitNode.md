---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09391f521a2b75663b25731c6cc20ef78a658d5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93755000"
---
# <span data-ttu-id="674a3-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="674a3-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="674a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="674a3-102">SYNOPSIS</span></span>
<span data-ttu-id="674a3-103">Skala ut en skalen het.</span><span class="sxs-lookup"><span data-stu-id="674a3-103">Scale out a scale unit.</span></span>

## <span data-ttu-id="674a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="674a3-104">SYNTAX</span></span>

```
Add-AzsScaleUnitNode [-NodeList] <ScaleOutScaleUnitParameters[]> [[-ResourceGroupName] <String>]
 [-ScaleUnit] <String> [[-Location] <String>] [-AwaitStorageConvergence] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="674a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="674a3-105">DESCRIPTION</span></span>
<span data-ttu-id="674a3-106">Lägga till en ny nod för skalnings enhet i ett kluster för skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="674a3-106">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="674a3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="674a3-107">EXAMPLES</span></span>

### <span data-ttu-id="674a3-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="674a3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName
```

<span data-ttu-id="674a3-109">Lägger till en lista med noder till enheten.</span><span class="sxs-lookup"><span data-stu-id="674a3-109">Adds a list of nodes to the scale unit.</span></span>

## <span data-ttu-id="674a3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="674a3-110">PARAMETERS</span></span>

### <span data-ttu-id="674a3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="674a3-111">-AsJob</span></span>
<span data-ttu-id="674a3-112">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="674a3-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674a3-113">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="674a3-113">-AwaitStorageConvergence</span></span>
<span data-ttu-id="674a3-114">Vänta tills lagringsreplik är klar innan du returnerar framgång.</span><span class="sxs-lookup"><span data-stu-id="674a3-114">Wait for storage replication to complete before returning success.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674a3-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="674a3-115">-Location</span></span>
<span data-ttu-id="674a3-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="674a3-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674a3-117">-NodeList</span><span class="sxs-lookup"><span data-stu-id="674a3-117">-NodeList</span></span>
<span data-ttu-id="674a3-118">En lista över indata som gör att du kan lägga till en uppsättning noder för skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="674a3-118">A list of input data that allows for adding a set of scale unit nodes.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="674a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="674a3-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="674a3-120">Name of the resource group.</span></span>

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

### <span data-ttu-id="674a3-121">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="674a3-121">-ScaleUnit</span></span>
<span data-ttu-id="674a3-122">Namnet på enheten.</span><span class="sxs-lookup"><span data-stu-id="674a3-122">Name of the scale units.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="674a3-123">CommonParameters</span></span>
<span data-ttu-id="674a3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="674a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="674a3-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="674a3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="674a3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="674a3-126">INPUTS</span></span>

## <span data-ttu-id="674a3-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="674a3-127">OUTPUTS</span></span>

## <span data-ttu-id="674a3-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="674a3-128">NOTES</span></span>

## <span data-ttu-id="674a3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="674a3-129">RELATED LINKS</span></span>

