---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571280"
---
# <span data-ttu-id="b1c14-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="b1c14-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="b1c14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1c14-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c14-103">Avbryt ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="b1c14-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="b1c14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1c14-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1c14-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1c14-105">DESCRIPTION</span></span>
<span data-ttu-id="b1c14-106">Avbryt ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="b1c14-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="b1c14-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1c14-107">EXAMPLES</span></span>

### <span data-ttu-id="b1c14-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1c14-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="b1c14-109">Avbryt migrering av container.</span><span class="sxs-lookup"><span data-stu-id="b1c14-109">Cancel container migration.</span></span>

## <span data-ttu-id="b1c14-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1c14-110">PARAMETERS</span></span>

### <span data-ttu-id="b1c14-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1c14-111">-AsJob</span></span>
<span data-ttu-id="b1c14-112">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="b1c14-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="b1c14-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="b1c14-113">-FarmName</span></span>
<span data-ttu-id="b1c14-114">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="b1c14-114">Farm Id.</span></span>

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

### <span data-ttu-id="b1c14-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b1c14-115">-Force</span></span>
<span data-ttu-id="b1c14-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b1c14-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b1c14-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="b1c14-117">-JobId</span></span>
<span data-ttu-id="b1c14-118">Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="b1c14-118">Operation Id.</span></span>

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

### <span data-ttu-id="b1c14-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c14-119">-ResourceGroupName</span></span>
<span data-ttu-id="b1c14-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b1c14-120">Resource group name.</span></span>

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

### <span data-ttu-id="b1c14-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b1c14-121">-Confirm</span></span>
<span data-ttu-id="b1c14-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b1c14-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1c14-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c14-123">-WhatIf</span></span>
<span data-ttu-id="b1c14-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b1c14-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1c14-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b1c14-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1c14-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c14-126">CommonParameters</span></span>
<span data-ttu-id="b1c14-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1c14-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c14-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1c14-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c14-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1c14-129">INPUTS</span></span>

## <span data-ttu-id="b1c14-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1c14-130">OUTPUTS</span></span>

## <span data-ttu-id="b1c14-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1c14-131">NOTES</span></span>

## <span data-ttu-id="b1c14-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1c14-132">RELATED LINKS</span></span>

