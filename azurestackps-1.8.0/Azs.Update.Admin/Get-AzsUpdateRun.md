---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0bbd694fff313f4c7b8983521dee8cd1c01f7561
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921297"
---
# <span data-ttu-id="00c67-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="00c67-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="00c67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00c67-102">SYNOPSIS</span></span>
<span data-ttu-id="00c67-103">Hämta listan med uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="00c67-103">Get the list of update runs.</span></span>

## <span data-ttu-id="00c67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00c67-104">SYNTAX</span></span>

### <span data-ttu-id="00c67-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="00c67-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="00c67-106">Lära</span><span class="sxs-lookup"><span data-stu-id="00c67-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="00c67-107">ID</span><span class="sxs-lookup"><span data-stu-id="00c67-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="00c67-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00c67-108">DESCRIPTION</span></span>
<span data-ttu-id="00c67-109">Hämta listan med uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="00c67-109">Get the list of update runs.</span></span> <span data-ttu-id="00c67-110">Förekomster av UpdateRun-objekt som returnerats kan vara piped att starta om-AzsUpdateRun när så är tillämpligt.</span><span class="sxs-lookup"><span data-stu-id="00c67-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="00c67-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00c67-111">EXAMPLES</span></span>

### <span data-ttu-id="00c67-112">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="00c67-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="00c67-113">Få en lista över alla försök att tillämpa en viss uppdatering.</span><span class="sxs-lookup"><span data-stu-id="00c67-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="00c67-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00c67-114">PARAMETERS</span></span>

### <span data-ttu-id="00c67-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="00c67-115">-Name</span></span>
<span data-ttu-id="00c67-116">Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="00c67-116">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00c67-117">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="00c67-117">-UpdateName</span></span>
<span data-ttu-id="00c67-118">Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="00c67-118">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00c67-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="00c67-119">-Location</span></span>
<span data-ttu-id="00c67-120">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="00c67-120">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00c67-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00c67-121">-ResourceGroupName</span></span>
<span data-ttu-id="00c67-122">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="00c67-122">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00c67-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00c67-123">-ResourceId</span></span>
<span data-ttu-id="00c67-124">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="00c67-124">The resource id.</span></span>

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

### <span data-ttu-id="00c67-125">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="00c67-125">-Skip</span></span>
<span data-ttu-id="00c67-126">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="00c67-126">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00c67-127">-Överst</span><span class="sxs-lookup"><span data-stu-id="00c67-127">-Top</span></span>
<span data-ttu-id="00c67-128">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="00c67-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="00c67-129">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="00c67-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00c67-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c67-130">CommonParameters</span></span>
<span data-ttu-id="00c67-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00c67-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c67-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00c67-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c67-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00c67-133">INPUTS</span></span>

## <span data-ttu-id="00c67-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00c67-134">OUTPUTS</span></span>

### <span data-ttu-id="00c67-135">Microsoft. AzureStack. Management. Update. admin. Models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="00c67-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="00c67-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00c67-136">NOTES</span></span>

## <span data-ttu-id="00c67-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00c67-137">RELATED LINKS</span></span>
