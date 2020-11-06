---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4e3e69a0c55188514a31dbe7377f8336784b114
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571803"
---
# <span data-ttu-id="755b5-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="755b5-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="755b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="755b5-102">SYNOPSIS</span></span>
<span data-ttu-id="755b5-103">Ta bort ett borttaget lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="755b5-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="755b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="755b5-104">SYNTAX</span></span>

### <span data-ttu-id="755b5-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="755b5-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="755b5-106">ID</span><span class="sxs-lookup"><span data-stu-id="755b5-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="755b5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="755b5-107">DESCRIPTION</span></span>
<span data-ttu-id="755b5-108">Ta bort ett borttaget lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="755b5-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="755b5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="755b5-109">EXAMPLES</span></span>

### <span data-ttu-id="755b5-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="755b5-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="755b5-111">Ta bort ett borttaget lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="755b5-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="755b5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="755b5-112">PARAMETERS</span></span>

### <span data-ttu-id="755b5-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="755b5-113">-FarmName</span></span>
<span data-ttu-id="755b5-114">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="755b5-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755b5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="755b5-115">-Force</span></span>
<span data-ttu-id="755b5-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="755b5-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="755b5-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="755b5-117">-Name</span></span>
<span data-ttu-id="755b5-118">Internt lagrings konto-ID som inte är synligt för klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="755b5-118">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755b5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755b5-119">-ResourceGroupName</span></span>
<span data-ttu-id="755b5-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="755b5-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755b5-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="755b5-121">-ResourceId</span></span>
<span data-ttu-id="755b5-122">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="755b5-122">The resource id.</span></span>

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

### <span data-ttu-id="755b5-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="755b5-123">-Confirm</span></span>
<span data-ttu-id="755b5-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="755b5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="755b5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755b5-125">-WhatIf</span></span>
<span data-ttu-id="755b5-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="755b5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="755b5-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="755b5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="755b5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755b5-128">CommonParameters</span></span>
<span data-ttu-id="755b5-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755b5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755b5-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="755b5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755b5-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="755b5-131">INPUTS</span></span>

## <span data-ttu-id="755b5-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="755b5-132">OUTPUTS</span></span>

## <span data-ttu-id="755b5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="755b5-133">NOTES</span></span>

## <span data-ttu-id="755b5-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="755b5-134">RELATED LINKS</span></span>

