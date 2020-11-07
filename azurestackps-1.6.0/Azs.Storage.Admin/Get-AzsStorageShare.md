---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cc6e2adff73e4b7c81a401bb98e9ab625005ae3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754967"
---
# <span data-ttu-id="8c999-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="8c999-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="8c999-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c999-102">SYNOPSIS</span></span>
<span data-ttu-id="8c999-103">Returnerar en lista med lagrings resurser.</span><span class="sxs-lookup"><span data-stu-id="8c999-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="8c999-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c999-104">SYNTAX</span></span>

### <span data-ttu-id="8c999-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8c999-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c999-106">Lära</span><span class="sxs-lookup"><span data-stu-id="8c999-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c999-107">ID</span><span class="sxs-lookup"><span data-stu-id="8c999-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8c999-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c999-108">DESCRIPTION</span></span>
<span data-ttu-id="8c999-109">Returnerar en lista med lagrings resurser.</span><span class="sxs-lookup"><span data-stu-id="8c999-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="8c999-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c999-110">EXAMPLES</span></span>

### <span data-ttu-id="8c999-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8c999-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="8c999-112">Hämta listan med lagrings resurser.</span><span class="sxs-lookup"><span data-stu-id="8c999-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="8c999-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c999-113">PARAMETERS</span></span>

### <span data-ttu-id="8c999-114">-FarmName</span><span class="sxs-lookup"><span data-stu-id="8c999-114">-FarmName</span></span>
<span data-ttu-id="8c999-115">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="8c999-115">Farm Id.</span></span>

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

### <span data-ttu-id="8c999-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="8c999-116">-Name</span></span>
<span data-ttu-id="8c999-117">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="8c999-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c999-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c999-118">-ResourceGroupName</span></span>
<span data-ttu-id="8c999-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="8c999-119">Resource group name.</span></span>

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

### <span data-ttu-id="8c999-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c999-120">-ResourceId</span></span>
<span data-ttu-id="8c999-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="8c999-121">The resource id.</span></span>

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

### <span data-ttu-id="8c999-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c999-122">CommonParameters</span></span>
<span data-ttu-id="8c999-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c999-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c999-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c999-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c999-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c999-125">INPUTS</span></span>

## <span data-ttu-id="8c999-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c999-126">OUTPUTS</span></span>

### <span data-ttu-id="8c999-127">Microsoft. AzureStack. Management. Storage. admin. Models. share</span><span class="sxs-lookup"><span data-stu-id="8c999-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="8c999-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c999-128">NOTES</span></span>

## <span data-ttu-id="8c999-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c999-129">RELATED LINKS</span></span>
