---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0983e05a36de72148571ccbbc7f1454343ad393a
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921877"
---
# <span data-ttu-id="ac1e3-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="ac1e3-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="ac1e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac1e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1e3-103">Ta bort en befintlig kvot</span><span class="sxs-lookup"><span data-stu-id="ac1e3-103">Delete an existing quota</span></span>

## <span data-ttu-id="ac1e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac1e3-104">SYNTAX</span></span>

### <span data-ttu-id="ac1e3-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="ac1e3-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac1e3-106">ID</span><span class="sxs-lookup"><span data-stu-id="ac1e3-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac1e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac1e3-107">DESCRIPTION</span></span>
<span data-ttu-id="ac1e3-108">Ta bort en befintlig kvot</span><span class="sxs-lookup"><span data-stu-id="ac1e3-108">Delete an existing quota</span></span>

## <span data-ttu-id="ac1e3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac1e3-109">EXAMPLES</span></span>

### <span data-ttu-id="ac1e3-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="ac1e3-110">EXAMPLE 1</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="ac1e3-111">Ta bort en lagrings kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="ac1e3-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="ac1e3-112">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="ac1e3-112">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="ac1e3-113">Ta bort en lagrings kvot efter överföring.</span><span class="sxs-lookup"><span data-stu-id="ac1e3-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="ac1e3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac1e3-114">PARAMETERS</span></span>

### <span data-ttu-id="ac1e3-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac1e3-115">-Name</span></span>
<span data-ttu-id="ac1e3-116">Namnet på lagrings kvoten.</span><span class="sxs-lookup"><span data-stu-id="ac1e3-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="ac1e3-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="ac1e3-117">-Location</span></span>
<span data-ttu-id="ac1e3-118">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="ac1e3-118">Resource location.</span></span>

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

### <span data-ttu-id="ac1e3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac1e3-119">-ResourceId</span></span>
<span data-ttu-id="ac1e3-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ac1e3-120">The resource id.</span></span>

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

### <span data-ttu-id="ac1e3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ac1e3-121">-Force</span></span>
<span data-ttu-id="ac1e3-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ac1e3-122">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ac1e3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac1e3-123">-WhatIf</span></span>
<span data-ttu-id="ac1e3-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ac1e3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac1e3-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ac1e3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac1e3-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ac1e3-126">-Confirm</span></span>
<span data-ttu-id="ac1e3-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ac1e3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac1e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1e3-128">CommonParameters</span></span>
<span data-ttu-id="ac1e3-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac1e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1e3-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac1e3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1e3-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac1e3-131">INPUTS</span></span>

## <span data-ttu-id="ac1e3-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac1e3-132">OUTPUTS</span></span>

## <span data-ttu-id="ac1e3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac1e3-133">NOTES</span></span>

## <span data-ttu-id="ac1e3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac1e3-134">RELATED LINKS</span></span>
