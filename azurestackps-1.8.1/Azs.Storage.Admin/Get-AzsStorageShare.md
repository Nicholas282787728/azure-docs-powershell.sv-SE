---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f8c9192100536a04b664f981a9df9e1508a1f87
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921760"
---
# <span data-ttu-id="2a883-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="2a883-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="2a883-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a883-102">SYNOPSIS</span></span>
<span data-ttu-id="2a883-103">Returnerar en lista med lagrings resurser.</span><span class="sxs-lookup"><span data-stu-id="2a883-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="2a883-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a883-104">SYNTAX</span></span>

### <span data-ttu-id="2a883-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="2a883-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2a883-106">Lära</span><span class="sxs-lookup"><span data-stu-id="2a883-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -ShareName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2a883-107">ID</span><span class="sxs-lookup"><span data-stu-id="2a883-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2a883-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a883-108">DESCRIPTION</span></span>
<span data-ttu-id="2a883-109">Returnerar en lista med lagrings resurser.</span><span class="sxs-lookup"><span data-stu-id="2a883-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="2a883-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a883-110">EXAMPLES</span></span>

### <span data-ttu-id="2a883-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="2a883-111">EXAMPLE 1</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="2a883-112">Hämta listan med lagrings resurser.</span><span class="sxs-lookup"><span data-stu-id="2a883-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="2a883-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a883-113">PARAMETERS</span></span>

### <span data-ttu-id="2a883-114">-FarmName</span><span class="sxs-lookup"><span data-stu-id="2a883-114">-FarmName</span></span>
<span data-ttu-id="2a883-115">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="2a883-115">Farm Id.</span></span>

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

### <span data-ttu-id="2a883-116">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2a883-116">-ShareName</span></span>
<span data-ttu-id="2a883-117">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="2a883-117">Share name.</span></span>

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

### <span data-ttu-id="2a883-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a883-118">-ResourceGroupName</span></span>
<span data-ttu-id="2a883-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2a883-119">Resource group name.</span></span>

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

### <span data-ttu-id="2a883-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a883-120">-ResourceId</span></span>
<span data-ttu-id="2a883-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2a883-121">The resource id.</span></span>

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

### <span data-ttu-id="2a883-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a883-122">CommonParameters</span></span>
<span data-ttu-id="2a883-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a883-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a883-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a883-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a883-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a883-125">INPUTS</span></span>

## <span data-ttu-id="2a883-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a883-126">OUTPUTS</span></span>

### <span data-ttu-id="2a883-127">Microsoft. AzureStack. Management. Storage. admin. Models. share</span><span class="sxs-lookup"><span data-stu-id="2a883-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="2a883-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a883-128">NOTES</span></span>

## <span data-ttu-id="2a883-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a883-129">RELATED LINKS</span></span>
