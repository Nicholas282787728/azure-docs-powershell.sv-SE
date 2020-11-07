---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75010b9591b4211f32c5665aa969bae28d69aaea
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921617"
---
# <span data-ttu-id="24814-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="24814-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="24814-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24814-102">SYNOPSIS</span></span>
<span data-ttu-id="24814-103">Tar bort det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="24814-103">Removes the specified plan</span></span>

## <span data-ttu-id="24814-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24814-104">SYNTAX</span></span>

### <span data-ttu-id="24814-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="24814-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24814-106">ID</span><span class="sxs-lookup"><span data-stu-id="24814-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24814-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24814-107">DESCRIPTION</span></span>
<span data-ttu-id="24814-108">Tar bort det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="24814-108">Removes the specified plan</span></span>

## <span data-ttu-id="24814-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24814-109">EXAMPLES</span></span>

### <span data-ttu-id="24814-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="24814-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="24814-111">Tar bort det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="24814-111">Removes the specified plan</span></span>

## <span data-ttu-id="24814-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24814-112">PARAMETERS</span></span>

### <span data-ttu-id="24814-113">-Force</span><span class="sxs-lookup"><span data-stu-id="24814-113">-Force</span></span>
<span data-ttu-id="24814-114">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="24814-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="24814-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="24814-115">-Name</span></span>
<span data-ttu-id="24814-116">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="24814-116">Name of the plan.</span></span>

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

### <span data-ttu-id="24814-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24814-117">-ResourceGroupName</span></span>
<span data-ttu-id="24814-118">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="24814-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="24814-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24814-119">-ResourceId</span></span>
<span data-ttu-id="24814-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="24814-120">The resource id.</span></span>

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

### <span data-ttu-id="24814-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24814-121">-Confirm</span></span>
<span data-ttu-id="24814-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24814-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24814-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24814-123">-WhatIf</span></span>
<span data-ttu-id="24814-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24814-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24814-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24814-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24814-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24814-126">CommonParameters</span></span>
<span data-ttu-id="24814-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24814-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24814-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24814-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24814-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24814-129">INPUTS</span></span>

## <span data-ttu-id="24814-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24814-130">OUTPUTS</span></span>

## <span data-ttu-id="24814-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24814-131">NOTES</span></span>

## <span data-ttu-id="24814-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24814-132">RELATED LINKS</span></span>

