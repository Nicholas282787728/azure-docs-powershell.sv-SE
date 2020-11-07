---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86b9e7574344e1b4724648ce55fa2e36aed6591b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921215"
---
# <span data-ttu-id="74a1b-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="74a1b-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="74a1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="74a1b-103">Returnerar en lista över alla Fabric-fildelningar på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="74a1b-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="74a1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74a1b-104">SYNTAX</span></span>

### <span data-ttu-id="74a1b-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="74a1b-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="74a1b-106">Lära</span><span class="sxs-lookup"><span data-stu-id="74a1b-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="74a1b-107">ID</span><span class="sxs-lookup"><span data-stu-id="74a1b-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="74a1b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74a1b-108">DESCRIPTION</span></span>
<span data-ttu-id="74a1b-109">Returnerar en lista över alla Fabric-fildelningar på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="74a1b-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="74a1b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74a1b-110">EXAMPLES</span></span>

### <span data-ttu-id="74a1b-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="74a1b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="74a1b-112">Returnerar en lista över alla fil resurser.</span><span class="sxs-lookup"><span data-stu-id="74a1b-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="74a1b-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="74a1b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="74a1b-114">Returnerar en fil resurs baserad på namn.</span><span class="sxs-lookup"><span data-stu-id="74a1b-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="74a1b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74a1b-115">PARAMETERS</span></span>

### <span data-ttu-id="74a1b-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="74a1b-116">-Filter</span></span>
<span data-ttu-id="74a1b-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="74a1b-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="74a1b-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="74a1b-118">-Location</span></span>
<span data-ttu-id="74a1b-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="74a1b-119">Location of the resource.</span></span>

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

### <span data-ttu-id="74a1b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="74a1b-120">-Name</span></span>
<span data-ttu-id="74a1b-121">Namn på Fabric File Share.</span><span class="sxs-lookup"><span data-stu-id="74a1b-121">Fabric file share name.</span></span>

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

### <span data-ttu-id="74a1b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a1b-122">-ResourceGroupName</span></span>
<span data-ttu-id="74a1b-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="74a1b-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="74a1b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74a1b-124">-ResourceId</span></span>
<span data-ttu-id="74a1b-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="74a1b-125">The resource id.</span></span>

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

### <span data-ttu-id="74a1b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a1b-126">CommonParameters</span></span>
<span data-ttu-id="74a1b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74a1b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a1b-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74a1b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a1b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74a1b-129">INPUTS</span></span>

## <span data-ttu-id="74a1b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74a1b-130">OUTPUTS</span></span>

### <span data-ttu-id="74a1b-131">Microsoft. AzureStack. Management. Fabric. admin. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="74a1b-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="74a1b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74a1b-132">NOTES</span></span>

## <span data-ttu-id="74a1b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74a1b-133">RELATED LINKS</span></span>

