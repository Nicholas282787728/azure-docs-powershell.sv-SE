---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab432625ab6af4a8fbd23895cb82e1d9f83954c8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921295"
---
# <span data-ttu-id="6161e-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="6161e-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="6161e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6161e-102">SYNOPSIS</span></span>
<span data-ttu-id="6161e-103">Tillämpa en specifik uppdatering på en uppdaterings plats.</span><span class="sxs-lookup"><span data-stu-id="6161e-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="6161e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6161e-104">SYNTAX</span></span>

### <span data-ttu-id="6161e-105">Tillämpa (standard)</span><span class="sxs-lookup"><span data-stu-id="6161e-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6161e-106">ID</span><span class="sxs-lookup"><span data-stu-id="6161e-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6161e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6161e-107">DESCRIPTION</span></span>
<span data-ttu-id="6161e-108">Tillämpa en specifik uppdatering på en uppdaterings plats.</span><span class="sxs-lookup"><span data-stu-id="6161e-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="6161e-109">När du har åberopat kan Get-AzsUpdateRun användas för att ändra uppdateringens status.</span><span class="sxs-lookup"><span data-stu-id="6161e-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="6161e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6161e-110">EXAMPLES</span></span>

### <span data-ttu-id="6161e-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="6161e-111">EXAMPLE 1</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="6161e-112">Tillämpa en specifik uppdatering på en uppdaterings plats.</span><span class="sxs-lookup"><span data-stu-id="6161e-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="6161e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6161e-113">PARAMETERS</span></span>

### <span data-ttu-id="6161e-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="6161e-114">-Name</span></span>
<span data-ttu-id="6161e-115">Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="6161e-115">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6161e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6161e-116">-ResourceGroupName</span></span>
<span data-ttu-id="6161e-117">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="6161e-117">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6161e-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="6161e-118">-Location</span></span>
<span data-ttu-id="6161e-119">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="6161e-119">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6161e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6161e-120">-AsJob</span></span>
<span data-ttu-id="6161e-121">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="6161e-121">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6161e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6161e-122">-ResourceId</span></span>
<span data-ttu-id="6161e-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6161e-123">The resource id.</span></span>

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

### <span data-ttu-id="6161e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6161e-124">-Force</span></span>
<span data-ttu-id="6161e-125">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6161e-125">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="6161e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6161e-126">-WhatIf</span></span>
<span data-ttu-id="6161e-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6161e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6161e-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6161e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6161e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6161e-129">-Confirm</span></span>
<span data-ttu-id="6161e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6161e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6161e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6161e-131">CommonParameters</span></span>
<span data-ttu-id="6161e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6161e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6161e-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6161e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6161e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6161e-134">INPUTS</span></span>

## <span data-ttu-id="6161e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6161e-135">OUTPUTS</span></span>

### <span data-ttu-id="6161e-136">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="6161e-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="6161e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6161e-137">NOTES</span></span>

## <span data-ttu-id="6161e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6161e-138">RELATED LINKS</span></span>
