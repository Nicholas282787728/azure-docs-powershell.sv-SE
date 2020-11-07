---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921628"
---
# <span data-ttu-id="7f889-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="7f889-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="7f889-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f889-102">SYNOPSIS</span></span>
<span data-ttu-id="7f889-103">Avbryt ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="7f889-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="7f889-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f889-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f889-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f889-105">DESCRIPTION</span></span>
<span data-ttu-id="7f889-106">Avbryt ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="7f889-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="7f889-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f889-107">EXAMPLES</span></span>

### <span data-ttu-id="7f889-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="7f889-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="7f889-109">Avbryt migrering av container.</span><span class="sxs-lookup"><span data-stu-id="7f889-109">Cancel container migration.</span></span>

## <span data-ttu-id="7f889-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f889-110">PARAMETERS</span></span>

### <span data-ttu-id="7f889-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="7f889-111">-JobId</span></span>
<span data-ttu-id="7f889-112">Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="7f889-112">Operation Id.</span></span>

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

### <span data-ttu-id="7f889-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f889-113">-ResourceGroupName</span></span>
<span data-ttu-id="7f889-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7f889-114">Resource group name.</span></span>

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

### <span data-ttu-id="7f889-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="7f889-115">-FarmName</span></span>
<span data-ttu-id="7f889-116">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="7f889-116">Farm Id.</span></span>

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

### <span data-ttu-id="7f889-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f889-117">-AsJob</span></span>
<span data-ttu-id="7f889-118">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="7f889-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7f889-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7f889-119">-Force</span></span>
<span data-ttu-id="7f889-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7f889-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7f889-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f889-121">-WhatIf</span></span>
<span data-ttu-id="7f889-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7f889-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f889-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7f889-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f889-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7f889-124">-Confirm</span></span>
<span data-ttu-id="7f889-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7f889-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f889-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f889-126">CommonParameters</span></span>
<span data-ttu-id="7f889-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f889-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f889-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f889-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f889-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f889-129">INPUTS</span></span>

## <span data-ttu-id="7f889-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f889-130">OUTPUTS</span></span>

## <span data-ttu-id="7f889-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f889-131">NOTES</span></span>

## <span data-ttu-id="7f889-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f889-132">RELATED LINKS</span></span>
