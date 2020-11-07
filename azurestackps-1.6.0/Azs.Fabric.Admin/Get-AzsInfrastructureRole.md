---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dac95eced72f70d3471019136d302fcdfe95f86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93755002"
---
# <span data-ttu-id="02554-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="02554-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="02554-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02554-102">SYNOPSIS</span></span>
<span data-ttu-id="02554-103">Returnerar en lista över alla infrastruktur roller på en plats.</span><span class="sxs-lookup"><span data-stu-id="02554-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="02554-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02554-104">SYNTAX</span></span>

### <span data-ttu-id="02554-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="02554-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="02554-106">Lära</span><span class="sxs-lookup"><span data-stu-id="02554-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="02554-107">ID</span><span class="sxs-lookup"><span data-stu-id="02554-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="02554-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02554-108">DESCRIPTION</span></span>
<span data-ttu-id="02554-109">Returnerar en lista över alla infrastruktur roller på en plats.</span><span class="sxs-lookup"><span data-stu-id="02554-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="02554-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02554-110">EXAMPLES</span></span>

### <span data-ttu-id="02554-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="02554-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="02554-112">Få en lista över alla infrastruktur roller.</span><span class="sxs-lookup"><span data-stu-id="02554-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="02554-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="02554-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="02554-114">Skaffa en infrastruktur roll baserat på namnet.</span><span class="sxs-lookup"><span data-stu-id="02554-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="02554-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02554-115">PARAMETERS</span></span>

### <span data-ttu-id="02554-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="02554-116">-Filter</span></span>
<span data-ttu-id="02554-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="02554-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="02554-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="02554-118">-Location</span></span>
<span data-ttu-id="02554-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="02554-119">Location of the resource.</span></span>

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

### <span data-ttu-id="02554-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="02554-120">-Name</span></span>
<span data-ttu-id="02554-121">Namn på infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="02554-121">Infrastructure role name.</span></span>

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

### <span data-ttu-id="02554-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02554-122">-ResourceGroupName</span></span>
<span data-ttu-id="02554-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="02554-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="02554-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02554-124">-ResourceId</span></span>
<span data-ttu-id="02554-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="02554-125">The resource id.</span></span>

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

### <span data-ttu-id="02554-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="02554-126">-Skip</span></span>
<span data-ttu-id="02554-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="02554-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="02554-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="02554-128">-Top</span></span>
<span data-ttu-id="02554-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="02554-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="02554-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="02554-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="02554-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02554-131">CommonParameters</span></span>
<span data-ttu-id="02554-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02554-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02554-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02554-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02554-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02554-134">INPUTS</span></span>

## <span data-ttu-id="02554-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02554-135">OUTPUTS</span></span>

### <span data-ttu-id="02554-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="02554-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="02554-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02554-137">NOTES</span></span>

## <span data-ttu-id="02554-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02554-138">RELATED LINKS</span></span>

