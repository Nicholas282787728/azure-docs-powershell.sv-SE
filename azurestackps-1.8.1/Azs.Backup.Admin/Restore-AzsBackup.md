---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 573a47b3684020817130e1d41c764abef717de0a
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921915"
---
# <span data-ttu-id="77c34-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="77c34-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="77c34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77c34-102">SYNOPSIS</span></span>
<span data-ttu-id="77c34-103">Återställa en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="77c34-103">Restore a backup.</span></span>

## <span data-ttu-id="77c34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77c34-104">SYNTAX</span></span>

### <span data-ttu-id="77c34-105">Backups_Restore (standard)</span><span class="sxs-lookup"><span data-stu-id="77c34-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77c34-106">ID</span><span class="sxs-lookup"><span data-stu-id="77c34-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77c34-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77c34-107">DESCRIPTION</span></span>
<span data-ttu-id="77c34-108">Återställa en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="77c34-108">Restore a backup.</span></span>

## <span data-ttu-id="77c34-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77c34-109">EXAMPLES</span></span>

### <span data-ttu-id="77c34-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="77c34-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="77c34-111">Återställ från en Azure Stack-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="77c34-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="77c34-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77c34-112">PARAMETERS</span></span>

### <span data-ttu-id="77c34-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77c34-113">-AsJob</span></span>
<span data-ttu-id="77c34-114">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="77c34-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="77c34-115">-Force</span><span class="sxs-lookup"><span data-stu-id="77c34-115">-Force</span></span>
<span data-ttu-id="77c34-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="77c34-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="77c34-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="77c34-117">-Location</span></span>
<span data-ttu-id="77c34-118">Namn på plats för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="77c34-118">Name of location to backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c34-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="77c34-119">-Name</span></span>
<span data-ttu-id="77c34-120">Namn på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="77c34-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c34-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77c34-121">-ResourceGroupName</span></span>
<span data-ttu-id="77c34-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="77c34-122">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c34-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77c34-123">-ResourceId</span></span>
<span data-ttu-id="77c34-124">{{Fill ResourceId}}</span><span class="sxs-lookup"><span data-stu-id="77c34-124">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="77c34-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77c34-125">-Confirm</span></span>
<span data-ttu-id="77c34-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77c34-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77c34-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77c34-127">-WhatIf</span></span>
<span data-ttu-id="77c34-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77c34-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77c34-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77c34-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77c34-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c34-130">CommonParameters</span></span>
<span data-ttu-id="77c34-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77c34-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c34-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77c34-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c34-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77c34-133">INPUTS</span></span>

## <span data-ttu-id="77c34-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77c34-134">OUTPUTS</span></span>

## <span data-ttu-id="77c34-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77c34-135">NOTES</span></span>

## <span data-ttu-id="77c34-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77c34-136">RELATED LINKS</span></span>

