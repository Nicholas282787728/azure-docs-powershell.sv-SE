---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f87690c20357cbff7f85a405dd6d3fae3a72dc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571623"
---
# <span data-ttu-id="56e24-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="56e24-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="56e24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56e24-102">SYNOPSIS</span></span>
<span data-ttu-id="56e24-103">Tar bort en tilläggs bild för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="56e24-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="56e24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56e24-104">SYNTAX</span></span>

### <span data-ttu-id="56e24-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="56e24-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e24-106">ID</span><span class="sxs-lookup"><span data-stu-id="56e24-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56e24-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56e24-107">DESCRIPTION</span></span>
<span data-ttu-id="56e24-108">Tar bort den angivna tilläggs avbildningen för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="56e24-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="56e24-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56e24-109">EXAMPLES</span></span>

### <span data-ttu-id="56e24-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="56e24-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="56e24-111">Ta bort en plattforms bilds tillägg.</span><span class="sxs-lookup"><span data-stu-id="56e24-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="56e24-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56e24-112">PARAMETERS</span></span>

### <span data-ttu-id="56e24-113">-Force</span><span class="sxs-lookup"><span data-stu-id="56e24-113">-Force</span></span>
<span data-ttu-id="56e24-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="56e24-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="56e24-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="56e24-115">-Location</span></span>
<span data-ttu-id="56e24-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="56e24-116">Location of the resource.</span></span>

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

### <span data-ttu-id="56e24-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="56e24-117">-Publisher</span></span>
<span data-ttu-id="56e24-118">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="56e24-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="56e24-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56e24-119">-ResourceId</span></span>
<span data-ttu-id="56e24-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="56e24-120">The resource id.</span></span>

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

### <span data-ttu-id="56e24-121">– Skriv</span><span class="sxs-lookup"><span data-stu-id="56e24-121">-Type</span></span>
<span data-ttu-id="56e24-122">Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="56e24-122">Type of extension.</span></span>

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

### <span data-ttu-id="56e24-123">-Version</span><span class="sxs-lookup"><span data-stu-id="56e24-123">-Version</span></span>
<span data-ttu-id="56e24-124">Versionen av tillägget för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="56e24-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="56e24-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="56e24-125">-Confirm</span></span>
<span data-ttu-id="56e24-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56e24-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56e24-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e24-127">-WhatIf</span></span>
<span data-ttu-id="56e24-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="56e24-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56e24-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="56e24-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56e24-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e24-130">CommonParameters</span></span>
<span data-ttu-id="56e24-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e24-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e24-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e24-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e24-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56e24-133">INPUTS</span></span>

## <span data-ttu-id="56e24-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56e24-134">OUTPUTS</span></span>

## <span data-ttu-id="56e24-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56e24-135">NOTES</span></span>

## <span data-ttu-id="56e24-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56e24-136">RELATED LINKS</span></span>

