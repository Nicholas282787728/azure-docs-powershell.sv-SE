---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099833"
---
# <span data-ttu-id="e5bfd-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="e5bfd-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="e5bfd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="e5bfd-103">Avbryt ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="e5bfd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5bfd-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5bfd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5bfd-105">DESCRIPTION</span></span>
<span data-ttu-id="e5bfd-106">Avbryt ett migreringsjobb-jobb.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="e5bfd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5bfd-107">EXAMPLES</span></span>

### <span data-ttu-id="e5bfd-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="e5bfd-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="e5bfd-109">Avbryt migrering av container.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-109">Cancel container migration.</span></span>

## <span data-ttu-id="e5bfd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5bfd-110">PARAMETERS</span></span>

### <span data-ttu-id="e5bfd-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="e5bfd-111">-JobId</span></span>
<span data-ttu-id="e5bfd-112">Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-112">Operation Id.</span></span>

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

### <span data-ttu-id="e5bfd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5bfd-113">-ResourceGroupName</span></span>
<span data-ttu-id="e5bfd-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-114">Resource group name.</span></span>

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

### <span data-ttu-id="e5bfd-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="e5bfd-115">-FarmName</span></span>
<span data-ttu-id="e5bfd-116">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-116">Farm Id.</span></span>

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

### <span data-ttu-id="e5bfd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5bfd-117">-AsJob</span></span>
<span data-ttu-id="e5bfd-118">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e5bfd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e5bfd-119">-Force</span></span>
<span data-ttu-id="e5bfd-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e5bfd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5bfd-121">-WhatIf</span></span>
<span data-ttu-id="e5bfd-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5bfd-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5bfd-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e5bfd-124">-Confirm</span></span>
<span data-ttu-id="e5bfd-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5bfd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5bfd-126">CommonParameters</span></span>
<span data-ttu-id="e5bfd-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5bfd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5bfd-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5bfd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5bfd-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5bfd-129">INPUTS</span></span>

## <span data-ttu-id="e5bfd-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5bfd-130">OUTPUTS</span></span>

## <span data-ttu-id="e5bfd-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5bfd-131">NOTES</span></span>

## <span data-ttu-id="e5bfd-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5bfd-132">RELATED LINKS</span></span>
