---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821495581589eff356cd0d88fc98311b5f566d61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099866"
---
# <span data-ttu-id="96669-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="96669-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="96669-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96669-102">SYNOPSIS</span></span>
<span data-ttu-id="96669-103">Returnerar en lista över alla instanser av program varu belastning på en plats.</span><span class="sxs-lookup"><span data-stu-id="96669-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="96669-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96669-104">SYNTAX</span></span>

### <span data-ttu-id="96669-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="96669-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="96669-106">Lära</span><span class="sxs-lookup"><span data-stu-id="96669-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="96669-107">ID</span><span class="sxs-lookup"><span data-stu-id="96669-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="96669-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96669-108">DESCRIPTION</span></span>
<span data-ttu-id="96669-109">Returnerar en lista över alla instanser av program varu belastning på en plats.</span><span class="sxs-lookup"><span data-stu-id="96669-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="96669-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96669-110">EXAMPLES</span></span>

### <span data-ttu-id="96669-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="96669-111">EXAMPLE 1</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="96669-112">Skaffa alla multiplexor-instanser för belastningsutjämnare för program vara.</span><span class="sxs-lookup"><span data-stu-id="96669-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="96669-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="96669-113">EXAMPLE 2</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="96669-114">Skaffa en specifik multiplexor för multiplexor för belastningsutjämnare på en plats med ett namn.</span><span class="sxs-lookup"><span data-stu-id="96669-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="96669-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96669-115">PARAMETERS</span></span>

### <span data-ttu-id="96669-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="96669-116">-Name</span></span>
<span data-ttu-id="96669-117">Namn på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="96669-117">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="96669-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="96669-118">-Location</span></span>
<span data-ttu-id="96669-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="96669-119">Location of the resource.</span></span>

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

### <span data-ttu-id="96669-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96669-120">-ResourceGroupName</span></span>
<span data-ttu-id="96669-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="96669-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="96669-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96669-122">-ResourceId</span></span>
<span data-ttu-id="96669-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="96669-123">The resource id.</span></span>

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

### <span data-ttu-id="96669-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="96669-124">-Filter</span></span>
<span data-ttu-id="96669-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="96669-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="96669-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="96669-126">-Skip</span></span>
<span data-ttu-id="96669-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="96669-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="96669-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="96669-128">-Top</span></span>
<span data-ttu-id="96669-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="96669-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="96669-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="96669-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="96669-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96669-131">CommonParameters</span></span>
<span data-ttu-id="96669-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96669-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96669-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96669-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96669-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96669-134">INPUTS</span></span>

## <span data-ttu-id="96669-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96669-135">OUTPUTS</span></span>

### <span data-ttu-id="96669-136">Microsoft. AzureStack. Management. Fabric. admin. Models. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="96669-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="96669-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96669-137">NOTES</span></span>

## <span data-ttu-id="96669-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96669-138">RELATED LINKS</span></span>