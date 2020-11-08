---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100165"
---
# <span data-ttu-id="bde22-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="bde22-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="bde22-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bde22-102">SYNOPSIS</span></span>
<span data-ttu-id="bde22-103">Hämta listan med uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="bde22-103">Get the list of update locations.</span></span>

## <span data-ttu-id="bde22-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bde22-104">SYNTAX</span></span>

### <span data-ttu-id="bde22-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="bde22-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bde22-106">Lära</span><span class="sxs-lookup"><span data-stu-id="bde22-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bde22-107">ID</span><span class="sxs-lookup"><span data-stu-id="bde22-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bde22-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bde22-108">DESCRIPTION</span></span>
<span data-ttu-id="bde22-109">Hämta listan med uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="bde22-109">Get the list of update locations.</span></span> <span data-ttu-id="bde22-110">Platserna som returneras kan användas för att hämta tillgängliga uppdateringar på en viss plats med Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="bde22-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="bde22-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bde22-111">EXAMPLES</span></span>

### <span data-ttu-id="bde22-112">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="bde22-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="bde22-113">Hämta listan med uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="bde22-113">Get the list of update locations.</span></span>

## <span data-ttu-id="bde22-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bde22-114">PARAMETERS</span></span>

### <span data-ttu-id="bde22-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="bde22-115">-Location</span></span>
<span data-ttu-id="bde22-116">Namn på platsen.</span><span class="sxs-lookup"><span data-stu-id="bde22-116">Name of the Location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde22-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bde22-117">-ResourceGroupName</span></span>
<span data-ttu-id="bde22-118">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="bde22-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="bde22-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bde22-119">-ResourceId</span></span>
<span data-ttu-id="bde22-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="bde22-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde22-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde22-121">CommonParameters</span></span>
<span data-ttu-id="bde22-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bde22-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde22-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bde22-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde22-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bde22-124">INPUTS</span></span>

## <span data-ttu-id="bde22-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bde22-125">OUTPUTS</span></span>

### <span data-ttu-id="bde22-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="bde22-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="bde22-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bde22-127">NOTES</span></span>

## <span data-ttu-id="bde22-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bde22-128">RELATED LINKS</span></span>
