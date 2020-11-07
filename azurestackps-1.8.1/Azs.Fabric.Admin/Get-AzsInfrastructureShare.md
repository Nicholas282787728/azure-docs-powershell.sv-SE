---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921708"
---
# <span data-ttu-id="a2749-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="a2749-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="a2749-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2749-102">SYNOPSIS</span></span>
<span data-ttu-id="a2749-103">Returnerar en lista över alla Fabric-fildelningar på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="a2749-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="a2749-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2749-104">SYNTAX</span></span>

### <span data-ttu-id="a2749-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="a2749-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2749-106">Lära</span><span class="sxs-lookup"><span data-stu-id="a2749-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2749-107">ID</span><span class="sxs-lookup"><span data-stu-id="a2749-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a2749-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2749-108">DESCRIPTION</span></span>
<span data-ttu-id="a2749-109">Returnerar en lista över alla Fabric-fildelningar på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="a2749-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="a2749-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2749-110">EXAMPLES</span></span>

### <span data-ttu-id="a2749-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="a2749-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="a2749-112">Returnerar en lista över alla fil resurser.</span><span class="sxs-lookup"><span data-stu-id="a2749-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="a2749-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="a2749-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="a2749-114">Returnerar en fil resurs baserad på namn.</span><span class="sxs-lookup"><span data-stu-id="a2749-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="a2749-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2749-115">PARAMETERS</span></span>

### <span data-ttu-id="a2749-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a2749-116">-Name</span></span>
<span data-ttu-id="a2749-117">Namn på Fabric File Share.</span><span class="sxs-lookup"><span data-stu-id="a2749-117">Fabric file share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2749-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="a2749-118">-Location</span></span>
<span data-ttu-id="a2749-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="a2749-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a2749-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2749-120">-ResourceGroupName</span></span>
<span data-ttu-id="a2749-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="a2749-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a2749-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2749-122">-ResourceId</span></span>
<span data-ttu-id="a2749-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a2749-123">The resource id.</span></span>

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

### <span data-ttu-id="a2749-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="a2749-124">-Filter</span></span>
<span data-ttu-id="a2749-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="a2749-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2749-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2749-126">CommonParameters</span></span>
<span data-ttu-id="a2749-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2749-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2749-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2749-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2749-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2749-129">INPUTS</span></span>

## <span data-ttu-id="a2749-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2749-130">OUTPUTS</span></span>

### <span data-ttu-id="a2749-131">Microsoft. AzureStack. Management. Fabric. admin. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="a2749-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="a2749-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2749-132">NOTES</span></span>

## <span data-ttu-id="a2749-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2749-133">RELATED LINKS</span></span>
