---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87bab7bc266a77d9459bb0a3166d09f2b7d6c7de
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100170"
---
# <span data-ttu-id="dcbf6-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="dcbf6-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="dcbf6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dcbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbf6-103">Hämta listan med tillgängliga uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-103">Get the list of available updates.</span></span>

## <span data-ttu-id="dcbf6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dcbf6-104">SYNTAX</span></span>

### <span data-ttu-id="dcbf6-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="dcbf6-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcbf6-106">Lära</span><span class="sxs-lookup"><span data-stu-id="dcbf6-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="dcbf6-107">ID</span><span class="sxs-lookup"><span data-stu-id="dcbf6-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="dcbf6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dcbf6-108">DESCRIPTION</span></span>
<span data-ttu-id="dcbf6-109">Hämta listan med tillgängliga uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-109">Get the list of available updates.</span></span> <span data-ttu-id="dcbf6-110">Uppdateringar som returneras från denna modul kan vara piped till ' Install-AzsUpdate ', om tillämpligt.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="dcbf6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dcbf6-111">EXAMPLES</span></span>

### <span data-ttu-id="dcbf6-112">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="dcbf6-112">EXAMPLE 1</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="dcbf6-113">Hämta listan med tillgängliga uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-113">Get the list of available updates.</span></span>

### <span data-ttu-id="dcbf6-114">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="dcbf6-114">EXAMPLE 2</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="dcbf6-115">Hämta den specifika uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-115">Get the specific update.</span></span>

## <span data-ttu-id="dcbf6-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dcbf6-116">PARAMETERS</span></span>

### <span data-ttu-id="dcbf6-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="dcbf6-117">-Name</span></span>
<span data-ttu-id="dcbf6-118">Uppdateringens namn.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-118">Name of the update.</span></span>

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

### <span data-ttu-id="dcbf6-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="dcbf6-119">-Location</span></span>
<span data-ttu-id="dcbf6-120">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-120">The name of the update location.</span></span>

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

### <span data-ttu-id="dcbf6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcbf6-121">-ResourceGroupName</span></span>
<span data-ttu-id="dcbf6-122">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="dcbf6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcbf6-123">-ResourceId</span></span>
<span data-ttu-id="dcbf6-124">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-124">The resource id.</span></span>

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

### <span data-ttu-id="dcbf6-125">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="dcbf6-125">-Skip</span></span>
<span data-ttu-id="dcbf6-126">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="dcbf6-127">-Överst</span><span class="sxs-lookup"><span data-stu-id="dcbf6-127">-Top</span></span>
<span data-ttu-id="dcbf6-128">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="dcbf6-129">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="dcbf6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbf6-130">CommonParameters</span></span>
<span data-ttu-id="dcbf6-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcbf6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbf6-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcbf6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbf6-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dcbf6-133">INPUTS</span></span>

## <span data-ttu-id="dcbf6-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dcbf6-134">OUTPUTS</span></span>

### <span data-ttu-id="dcbf6-135">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="dcbf6-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="dcbf6-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dcbf6-136">NOTES</span></span>

## <span data-ttu-id="dcbf6-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dcbf6-137">RELATED LINKS</span></span>
