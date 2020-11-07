---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b62b8ffbdcdcefff5bbb5c984a19ef0b7cb644
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921426"
---
# <span data-ttu-id="98a5a-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="98a5a-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="98a5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="98a5a-103">Ta bort en befintlig kvot</span><span class="sxs-lookup"><span data-stu-id="98a5a-103">Delete an existing quota</span></span>

## <span data-ttu-id="98a5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98a5a-104">SYNTAX</span></span>

### <span data-ttu-id="98a5a-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="98a5a-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98a5a-106">ID</span><span class="sxs-lookup"><span data-stu-id="98a5a-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98a5a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98a5a-107">DESCRIPTION</span></span>
<span data-ttu-id="98a5a-108">Ta bort en befintlig kvot</span><span class="sxs-lookup"><span data-stu-id="98a5a-108">Delete an existing quota</span></span>

## <span data-ttu-id="98a5a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98a5a-109">EXAMPLES</span></span>

### <span data-ttu-id="98a5a-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="98a5a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="98a5a-111">Ta bort en lagrings kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="98a5a-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="98a5a-112">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="98a5a-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="98a5a-113">Ta bort en lagrings kvot efter överföring.</span><span class="sxs-lookup"><span data-stu-id="98a5a-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="98a5a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98a5a-114">PARAMETERS</span></span>

### <span data-ttu-id="98a5a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="98a5a-115">-Force</span></span>
<span data-ttu-id="98a5a-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="98a5a-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="98a5a-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="98a5a-117">-Location</span></span>
<span data-ttu-id="98a5a-118">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="98a5a-118">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a5a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="98a5a-119">-Name</span></span>
<span data-ttu-id="98a5a-120">Namnet på lagrings kvoten.</span><span class="sxs-lookup"><span data-stu-id="98a5a-120">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a5a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98a5a-121">-ResourceId</span></span>
<span data-ttu-id="98a5a-122">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="98a5a-122">The resource id.</span></span>

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

### <span data-ttu-id="98a5a-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="98a5a-123">-Confirm</span></span>
<span data-ttu-id="98a5a-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98a5a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98a5a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98a5a-125">-WhatIf</span></span>
<span data-ttu-id="98a5a-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98a5a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98a5a-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="98a5a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98a5a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a5a-128">CommonParameters</span></span>
<span data-ttu-id="98a5a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98a5a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a5a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a5a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a5a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98a5a-131">INPUTS</span></span>

## <span data-ttu-id="98a5a-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98a5a-132">OUTPUTS</span></span>

## <span data-ttu-id="98a5a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98a5a-133">NOTES</span></span>

## <span data-ttu-id="98a5a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98a5a-134">RELATED LINKS</span></span>

