---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 268a306597fe3760e8abc7e31f980da078bf2bc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572211"
---
# <span data-ttu-id="468b4-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="468b4-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="468b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="468b4-102">SYNOPSIS</span></span>
<span data-ttu-id="468b4-103">Hämta listan med uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="468b4-103">Get the list of update runs.</span></span>

## <span data-ttu-id="468b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="468b4-104">SYNTAX</span></span>

### <span data-ttu-id="468b4-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="468b4-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="468b4-106">Lära</span><span class="sxs-lookup"><span data-stu-id="468b4-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="468b4-107">ID</span><span class="sxs-lookup"><span data-stu-id="468b4-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="468b4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="468b4-108">DESCRIPTION</span></span>
<span data-ttu-id="468b4-109">Hämta listan med uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="468b4-109">Get the list of update runs.</span></span> <span data-ttu-id="468b4-110">Förekomster av UpdateRun-objekt som returnerats kan vara piped att starta om-AzsUpdateRun när så är tillämpligt.</span><span class="sxs-lookup"><span data-stu-id="468b4-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="468b4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="468b4-111">EXAMPLES</span></span>

### <span data-ttu-id="468b4-112">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="468b4-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="468b4-113">Få en lista över alla försök att tillämpa en viss uppdatering.</span><span class="sxs-lookup"><span data-stu-id="468b4-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="468b4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="468b4-114">PARAMETERS</span></span>

### <span data-ttu-id="468b4-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="468b4-115">-Location</span></span>
<span data-ttu-id="468b4-116">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="468b4-116">The name of the update location.</span></span>

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

### <span data-ttu-id="468b4-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="468b4-117">-Name</span></span>
<span data-ttu-id="468b4-118">Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="468b4-118">Update run identifier.</span></span>

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

### <span data-ttu-id="468b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="468b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="468b4-120">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="468b4-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="468b4-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="468b4-121">-ResourceId</span></span>
<span data-ttu-id="468b4-122">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="468b4-122">The resource id.</span></span>

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

### <span data-ttu-id="468b4-123">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="468b4-123">-Skip</span></span>
<span data-ttu-id="468b4-124">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="468b4-124">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="468b4-125">-Överst</span><span class="sxs-lookup"><span data-stu-id="468b4-125">-Top</span></span>
<span data-ttu-id="468b4-126">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="468b4-126">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="468b4-127">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="468b4-127">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="468b4-128">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="468b4-128">-UpdateName</span></span>
<span data-ttu-id="468b4-129">Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="468b4-129">Name of the update.</span></span>

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

### <span data-ttu-id="468b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468b4-130">CommonParameters</span></span>
<span data-ttu-id="468b4-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="468b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468b4-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="468b4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468b4-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="468b4-133">INPUTS</span></span>

## <span data-ttu-id="468b4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="468b4-134">OUTPUTS</span></span>

### <span data-ttu-id="468b4-135">Microsoft. AzureStack. Management. Update. admin. Models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="468b4-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="468b4-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="468b4-136">NOTES</span></span>

## <span data-ttu-id="468b4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="468b4-137">RELATED LINKS</span></span>

