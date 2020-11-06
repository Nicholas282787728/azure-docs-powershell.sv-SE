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
ms.locfileid: "93571463"
---
# <span data-ttu-id="0abf8-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="0abf8-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="0abf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0abf8-102">SYNOPSIS</span></span>
<span data-ttu-id="0abf8-103">Returnerar en lista över alla Fabric-fildelningar på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="0abf8-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="0abf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0abf8-104">SYNTAX</span></span>

### <span data-ttu-id="0abf8-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="0abf8-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0abf8-106">Lära</span><span class="sxs-lookup"><span data-stu-id="0abf8-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0abf8-107">ID</span><span class="sxs-lookup"><span data-stu-id="0abf8-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0abf8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0abf8-108">DESCRIPTION</span></span>
<span data-ttu-id="0abf8-109">Returnerar en lista över alla Fabric-fildelningar på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="0abf8-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="0abf8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0abf8-110">EXAMPLES</span></span>

### <span data-ttu-id="0abf8-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0abf8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="0abf8-112">Returnerar en lista över alla fil resurser.</span><span class="sxs-lookup"><span data-stu-id="0abf8-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="0abf8-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0abf8-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="0abf8-114">Returnerar en fil resurs baserad på namn.</span><span class="sxs-lookup"><span data-stu-id="0abf8-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="0abf8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0abf8-115">PARAMETERS</span></span>

### <span data-ttu-id="0abf8-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="0abf8-116">-Filter</span></span>
<span data-ttu-id="0abf8-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="0abf8-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="0abf8-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="0abf8-118">-Location</span></span>
<span data-ttu-id="0abf8-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="0abf8-119">Location of the resource.</span></span>

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

### <span data-ttu-id="0abf8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0abf8-120">-Name</span></span>
<span data-ttu-id="0abf8-121">Namn på Fabric File Share.</span><span class="sxs-lookup"><span data-stu-id="0abf8-121">Fabric file share name.</span></span>

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

### <span data-ttu-id="0abf8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0abf8-122">-ResourceGroupName</span></span>
<span data-ttu-id="0abf8-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="0abf8-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0abf8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0abf8-124">-ResourceId</span></span>
<span data-ttu-id="0abf8-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="0abf8-125">The resource id.</span></span>

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

### <span data-ttu-id="0abf8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0abf8-126">CommonParameters</span></span>
<span data-ttu-id="0abf8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0abf8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0abf8-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0abf8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0abf8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0abf8-129">INPUTS</span></span>

## <span data-ttu-id="0abf8-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0abf8-130">OUTPUTS</span></span>

### <span data-ttu-id="0abf8-131">Microsoft. AzureStack. Management. Fabric. admin. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="0abf8-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="0abf8-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0abf8-132">NOTES</span></span>

## <span data-ttu-id="0abf8-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0abf8-133">RELATED LINKS</span></span>

