---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bf583c30d2faff1055debf366a84a0739789467
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921866"
---
# <span data-ttu-id="63ca0-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="63ca0-101">Start-AzsBackup</span></span>

## <span data-ttu-id="63ca0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="63ca0-103">Säkerhetskopiera en specifik plats.</span><span class="sxs-lookup"><span data-stu-id="63ca0-103">Back up a specific location.</span></span>

## <span data-ttu-id="63ca0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63ca0-104">SYNTAX</span></span>

### <span data-ttu-id="63ca0-105">CreateBackup (standard)</span><span class="sxs-lookup"><span data-stu-id="63ca0-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63ca0-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="63ca0-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63ca0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63ca0-107">DESCRIPTION</span></span>
<span data-ttu-id="63ca0-108">Säkerhetskopiera en specifik plats.</span><span class="sxs-lookup"><span data-stu-id="63ca0-108">Back up a specific location.</span></span>

## <span data-ttu-id="63ca0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63ca0-109">EXAMPLES</span></span>

### <span data-ttu-id="63ca0-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="63ca0-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="63ca0-111">Starta en Azure-Stack-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="63ca0-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="63ca0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63ca0-112">PARAMETERS</span></span>

### <span data-ttu-id="63ca0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63ca0-113">-AsJob</span></span>
<span data-ttu-id="63ca0-114">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="63ca0-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="63ca0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="63ca0-115">-Force</span></span>
<span data-ttu-id="63ca0-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="63ca0-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="63ca0-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="63ca0-117">-Location</span></span>
<span data-ttu-id="63ca0-118">Namn på platsen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="63ca0-118">Name of the backup location.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ca0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63ca0-119">-ResourceGroupName</span></span>
<span data-ttu-id="63ca0-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="63ca0-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ca0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63ca0-121">-ResourceId</span></span>
<span data-ttu-id="63ca0-122">{{Fill ResourceId}}</span><span class="sxs-lookup"><span data-stu-id="63ca0-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63ca0-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63ca0-123">-Confirm</span></span>
<span data-ttu-id="63ca0-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63ca0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63ca0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63ca0-125">-WhatIf</span></span>
<span data-ttu-id="63ca0-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63ca0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63ca0-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63ca0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63ca0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ca0-128">CommonParameters</span></span>
<span data-ttu-id="63ca0-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63ca0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ca0-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63ca0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ca0-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63ca0-131">INPUTS</span></span>

## <span data-ttu-id="63ca0-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63ca0-132">OUTPUTS</span></span>

### <span data-ttu-id="63ca0-133">Microsoft. AzureStack. Management. backup. admin. Models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="63ca0-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="63ca0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63ca0-134">NOTES</span></span>

## <span data-ttu-id="63ca0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63ca0-135">RELATED LINKS</span></span>

