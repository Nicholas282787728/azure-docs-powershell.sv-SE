---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921083"
---
# <span data-ttu-id="48695-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="48695-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="48695-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48695-102">SYNOPSIS</span></span>
<span data-ttu-id="48695-103">Starta skräp insamling på borttagna lagrings objekt.</span><span class="sxs-lookup"><span data-stu-id="48695-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="48695-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48695-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48695-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48695-105">DESCRIPTION</span></span>
<span data-ttu-id="48695-106">Starta skräp insamling på borttagna lagrings objekt.</span><span class="sxs-lookup"><span data-stu-id="48695-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="48695-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48695-107">EXAMPLES</span></span>

### <span data-ttu-id="48695-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="48695-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="48695-109">Starta skräp insamling.</span><span class="sxs-lookup"><span data-stu-id="48695-109">Start garbage collection.</span></span>

## <span data-ttu-id="48695-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48695-110">PARAMETERS</span></span>

### <span data-ttu-id="48695-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48695-111">-AsJob</span></span>
<span data-ttu-id="48695-112">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="48695-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="48695-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="48695-113">-FarmName</span></span>
<span data-ttu-id="48695-114">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="48695-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48695-115">-Force</span><span class="sxs-lookup"><span data-stu-id="48695-115">-Force</span></span>
<span data-ttu-id="48695-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="48695-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="48695-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48695-117">-ResourceGroupName</span></span>
<span data-ttu-id="48695-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="48695-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48695-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48695-119">-Confirm</span></span>
<span data-ttu-id="48695-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48695-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48695-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48695-121">-WhatIf</span></span>
<span data-ttu-id="48695-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="48695-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48695-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="48695-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48695-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48695-124">CommonParameters</span></span>
<span data-ttu-id="48695-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48695-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48695-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48695-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48695-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48695-127">INPUTS</span></span>

## <span data-ttu-id="48695-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48695-128">OUTPUTS</span></span>

## <span data-ttu-id="48695-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48695-129">NOTES</span></span>

## <span data-ttu-id="48695-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48695-130">RELATED LINKS</span></span>
