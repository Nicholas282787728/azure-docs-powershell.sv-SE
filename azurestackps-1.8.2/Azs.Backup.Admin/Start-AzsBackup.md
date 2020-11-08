---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bf583c30d2faff1055debf366a84a0739789467
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100034"
---
# <span data-ttu-id="8a064-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="8a064-101">Start-AzsBackup</span></span>

## <span data-ttu-id="8a064-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a064-102">SYNOPSIS</span></span>
<span data-ttu-id="8a064-103">Säkerhetskopiera en specifik plats.</span><span class="sxs-lookup"><span data-stu-id="8a064-103">Back up a specific location.</span></span>

## <span data-ttu-id="8a064-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a064-104">SYNTAX</span></span>

### <span data-ttu-id="8a064-105">CreateBackup (standard)</span><span class="sxs-lookup"><span data-stu-id="8a064-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a064-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="8a064-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a064-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a064-107">DESCRIPTION</span></span>
<span data-ttu-id="8a064-108">Säkerhetskopiera en specifik plats.</span><span class="sxs-lookup"><span data-stu-id="8a064-108">Back up a specific location.</span></span>

## <span data-ttu-id="8a064-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a064-109">EXAMPLES</span></span>

### <span data-ttu-id="8a064-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8a064-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="8a064-111">Starta en Azure-Stack-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="8a064-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="8a064-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a064-112">PARAMETERS</span></span>

### <span data-ttu-id="8a064-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a064-113">-AsJob</span></span>
<span data-ttu-id="8a064-114">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="8a064-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8a064-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8a064-115">-Force</span></span>
<span data-ttu-id="8a064-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8a064-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8a064-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="8a064-117">-Location</span></span>
<span data-ttu-id="8a064-118">Namn på platsen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="8a064-118">Name of the backup location.</span></span>

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

### <span data-ttu-id="8a064-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a064-119">-ResourceGroupName</span></span>
<span data-ttu-id="8a064-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8a064-120">Name of the resource group.</span></span>

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

### <span data-ttu-id="8a064-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a064-121">-ResourceId</span></span>
<span data-ttu-id="8a064-122">{{Fill ResourceId}}</span><span class="sxs-lookup"><span data-stu-id="8a064-122">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="8a064-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a064-123">-Confirm</span></span>
<span data-ttu-id="8a064-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a064-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a064-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a064-125">-WhatIf</span></span>
<span data-ttu-id="8a064-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a064-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a064-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a064-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a064-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a064-128">CommonParameters</span></span>
<span data-ttu-id="8a064-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a064-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a064-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a064-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a064-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a064-131">INPUTS</span></span>

## <span data-ttu-id="8a064-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a064-132">OUTPUTS</span></span>

### <span data-ttu-id="8a064-133">Microsoft. AzureStack. Management. backup. admin. Models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="8a064-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="8a064-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a064-134">NOTES</span></span>

## <span data-ttu-id="8a064-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a064-135">RELATED LINKS</span></span>

