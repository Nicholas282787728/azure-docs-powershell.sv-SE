---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ebc1ebae40d6d1726ee6c23def6f82ff1efc8517
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921400"
---
# <span data-ttu-id="602f3-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="602f3-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="602f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="602f3-102">SYNOPSIS</span></span>
<span data-ttu-id="602f3-103">Tar bort angiven Beräknad kvot.</span><span class="sxs-lookup"><span data-stu-id="602f3-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="602f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="602f3-104">SYNTAX</span></span>

### <span data-ttu-id="602f3-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="602f3-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="602f3-106">ID</span><span class="sxs-lookup"><span data-stu-id="602f3-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="602f3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="602f3-107">DESCRIPTION</span></span>
<span data-ttu-id="602f3-108">Ta bort en befintlig kvot.</span><span class="sxs-lookup"><span data-stu-id="602f3-108">Delete an existing quota.</span></span>

## <span data-ttu-id="602f3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="602f3-109">EXAMPLES</span></span>

### <span data-ttu-id="602f3-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="602f3-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="602f3-111">Ta bort en Compute-kvot med alla parametrar.</span><span class="sxs-lookup"><span data-stu-id="602f3-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="602f3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="602f3-112">PARAMETERS</span></span>

### <span data-ttu-id="602f3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="602f3-113">-Force</span></span>
<span data-ttu-id="602f3-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="602f3-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="602f3-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="602f3-115">-Location</span></span>
<span data-ttu-id="602f3-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="602f3-116">Location of the resource.</span></span> <span data-ttu-id="602f3-117">Om inget anges får vi standard platsen som är bunden till tenat-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="602f3-117">If not given we default to the location bound to the tenat's subscription.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602f3-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="602f3-118">-Name</span></span>
<span data-ttu-id="602f3-119">Namn på kvoten.</span><span class="sxs-lookup"><span data-stu-id="602f3-119">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602f3-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="602f3-120">-ResourceId</span></span>
<span data-ttu-id="602f3-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="602f3-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="602f3-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="602f3-122">-Confirm</span></span>
<span data-ttu-id="602f3-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="602f3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602f3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="602f3-124">-WhatIf</span></span>
<span data-ttu-id="602f3-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="602f3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="602f3-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="602f3-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="602f3-127">CommonParameters</span></span>
<span data-ttu-id="602f3-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="602f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="602f3-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="602f3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="602f3-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="602f3-130">INPUTS</span></span>

## <span data-ttu-id="602f3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="602f3-131">OUTPUTS</span></span>

## <span data-ttu-id="602f3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="602f3-132">NOTES</span></span>

## <span data-ttu-id="602f3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="602f3-133">RELATED LINKS</span></span>

