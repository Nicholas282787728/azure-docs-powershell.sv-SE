---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87bab7bc266a77d9459bb0a3166d09f2b7d6c7de
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921298"
---
# <span data-ttu-id="af99d-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="af99d-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="af99d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af99d-102">SYNOPSIS</span></span>
<span data-ttu-id="af99d-103">Hämta listan med tillgängliga uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="af99d-103">Get the list of available updates.</span></span>

## <span data-ttu-id="af99d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af99d-104">SYNTAX</span></span>

### <span data-ttu-id="af99d-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="af99d-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="af99d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="af99d-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="af99d-107">ID</span><span class="sxs-lookup"><span data-stu-id="af99d-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="af99d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af99d-108">DESCRIPTION</span></span>
<span data-ttu-id="af99d-109">Hämta listan med tillgängliga uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="af99d-109">Get the list of available updates.</span></span> <span data-ttu-id="af99d-110">Uppdateringar som returneras från denna modul kan vara piped till ' Install-AzsUpdate ', om tillämpligt.</span><span class="sxs-lookup"><span data-stu-id="af99d-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="af99d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af99d-111">EXAMPLES</span></span>

### <span data-ttu-id="af99d-112">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="af99d-112">EXAMPLE 1</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="af99d-113">Hämta listan med tillgängliga uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="af99d-113">Get the list of available updates.</span></span>

### <span data-ttu-id="af99d-114">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="af99d-114">EXAMPLE 2</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="af99d-115">Hämta den specifika uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="af99d-115">Get the specific update.</span></span>

## <span data-ttu-id="af99d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af99d-116">PARAMETERS</span></span>

### <span data-ttu-id="af99d-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="af99d-117">-Name</span></span>
<span data-ttu-id="af99d-118">Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="af99d-118">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Update

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af99d-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="af99d-119">-Location</span></span>
<span data-ttu-id="af99d-120">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="af99d-120">The name of the update location.</span></span>

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

### <span data-ttu-id="af99d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af99d-121">-ResourceGroupName</span></span>
<span data-ttu-id="af99d-122">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="af99d-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="af99d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af99d-123">-ResourceId</span></span>
<span data-ttu-id="af99d-124">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="af99d-124">The resource id.</span></span>

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

### <span data-ttu-id="af99d-125">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="af99d-125">-Skip</span></span>
<span data-ttu-id="af99d-126">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="af99d-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="af99d-127">-Överst</span><span class="sxs-lookup"><span data-stu-id="af99d-127">-Top</span></span>
<span data-ttu-id="af99d-128">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="af99d-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="af99d-129">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="af99d-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="af99d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af99d-130">CommonParameters</span></span>
<span data-ttu-id="af99d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af99d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af99d-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af99d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af99d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af99d-133">INPUTS</span></span>

## <span data-ttu-id="af99d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af99d-134">OUTPUTS</span></span>

### <span data-ttu-id="af99d-135">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="af99d-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="af99d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af99d-136">NOTES</span></span>

## <span data-ttu-id="af99d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af99d-137">RELATED LINKS</span></span>
