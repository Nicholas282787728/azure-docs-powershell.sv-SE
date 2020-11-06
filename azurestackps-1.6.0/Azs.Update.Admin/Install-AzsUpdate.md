---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4406dc4cadecd1945e82b8a90e9937df2183b4da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572208"
---
# <span data-ttu-id="d5396-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="d5396-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="d5396-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5396-102">SYNOPSIS</span></span>
<span data-ttu-id="d5396-103">Tillämpa en specifik uppdatering på en uppdaterings plats.</span><span class="sxs-lookup"><span data-stu-id="d5396-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="d5396-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5396-104">SYNTAX</span></span>

### <span data-ttu-id="d5396-105">Tillämpa (standard)</span><span class="sxs-lookup"><span data-stu-id="d5396-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5396-106">ID</span><span class="sxs-lookup"><span data-stu-id="d5396-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5396-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5396-107">DESCRIPTION</span></span>
<span data-ttu-id="d5396-108">Tillämpa en specifik uppdatering på en uppdaterings plats.</span><span class="sxs-lookup"><span data-stu-id="d5396-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="d5396-109">När du har åberopat kan Get-AzsUpdateRun användas för att ändra uppdateringens status.</span><span class="sxs-lookup"><span data-stu-id="d5396-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="d5396-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5396-110">EXAMPLES</span></span>

### <span data-ttu-id="d5396-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d5396-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="d5396-112">Tillämpa en specifik uppdatering på en uppdaterings plats.</span><span class="sxs-lookup"><span data-stu-id="d5396-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="d5396-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5396-113">PARAMETERS</span></span>

### <span data-ttu-id="d5396-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5396-114">-AsJob</span></span>
<span data-ttu-id="d5396-115">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="d5396-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d5396-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d5396-116">-Force</span></span>
<span data-ttu-id="d5396-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d5396-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d5396-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="d5396-118">-Location</span></span>
<span data-ttu-id="d5396-119">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="d5396-119">The name of the update location.</span></span>

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

### <span data-ttu-id="d5396-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5396-120">-Name</span></span>
<span data-ttu-id="d5396-121">Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="d5396-121">Name of the update.</span></span>

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

### <span data-ttu-id="d5396-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5396-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5396-123">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="d5396-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d5396-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5396-124">-ResourceId</span></span>
<span data-ttu-id="d5396-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d5396-125">The resource id.</span></span>

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

### <span data-ttu-id="d5396-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5396-126">-Confirm</span></span>
<span data-ttu-id="d5396-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5396-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5396-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5396-128">-WhatIf</span></span>
<span data-ttu-id="d5396-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5396-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5396-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5396-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5396-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5396-131">CommonParameters</span></span>
<span data-ttu-id="d5396-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5396-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5396-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5396-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5396-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5396-134">INPUTS</span></span>

## <span data-ttu-id="d5396-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5396-135">OUTPUTS</span></span>

### <span data-ttu-id="d5396-136">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="d5396-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="d5396-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5396-137">NOTES</span></span>

## <span data-ttu-id="d5396-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5396-138">RELATED LINKS</span></span>

