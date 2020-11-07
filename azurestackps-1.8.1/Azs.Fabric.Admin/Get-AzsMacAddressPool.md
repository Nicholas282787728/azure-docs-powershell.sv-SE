---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e22024b1b246a60104db0832860ed0aff699ff5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921702"
---
# <span data-ttu-id="e8858-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="e8858-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="e8858-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8858-102">SYNOPSIS</span></span>
<span data-ttu-id="e8858-103">Returnerar en lista över alla MAC-adresspooler på en plats.</span><span class="sxs-lookup"><span data-stu-id="e8858-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="e8858-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8858-104">SYNTAX</span></span>

### <span data-ttu-id="e8858-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="e8858-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e8858-106">Lära</span><span class="sxs-lookup"><span data-stu-id="e8858-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e8858-107">ID</span><span class="sxs-lookup"><span data-stu-id="e8858-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e8858-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8858-108">DESCRIPTION</span></span>
<span data-ttu-id="e8858-109">Returnerar en lista över alla MAC-adresspooler på en plats.</span><span class="sxs-lookup"><span data-stu-id="e8858-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="e8858-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8858-110">EXAMPLES</span></span>

### <span data-ttu-id="e8858-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="e8858-111">EXAMPLE 1</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="e8858-112">Hämta alla MAC-adresspooler på en plats.</span><span class="sxs-lookup"><span data-stu-id="e8858-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="e8858-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="e8858-113">EXAMPLE 2</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="e8858-114">Skaffa en MAC-adresspool på en plats baserad på namn.</span><span class="sxs-lookup"><span data-stu-id="e8858-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="e8858-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8858-115">PARAMETERS</span></span>

### <span data-ttu-id="e8858-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e8858-116">-Name</span></span>
<span data-ttu-id="e8858-117">Namn på MAC-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="e8858-117">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="e8858-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="e8858-118">-Location</span></span>
<span data-ttu-id="e8858-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="e8858-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e8858-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8858-120">-ResourceGroupName</span></span>
<span data-ttu-id="e8858-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="e8858-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e8858-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8858-122">-ResourceId</span></span>
<span data-ttu-id="e8858-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e8858-123">The resource id.</span></span>

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

### <span data-ttu-id="e8858-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="e8858-124">-Filter</span></span>
<span data-ttu-id="e8858-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="e8858-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="e8858-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="e8858-126">-Skip</span></span>
<span data-ttu-id="e8858-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="e8858-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e8858-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="e8858-128">-Top</span></span>
<span data-ttu-id="e8858-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="e8858-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e8858-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="e8858-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e8858-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8858-131">CommonParameters</span></span>
<span data-ttu-id="e8858-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8858-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8858-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8858-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8858-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8858-134">INPUTS</span></span>

## <span data-ttu-id="e8858-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8858-135">OUTPUTS</span></span>

### <span data-ttu-id="e8858-136">Microsoft. AzureStack. Management. Fabric. admin. Models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="e8858-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="e8858-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8858-137">NOTES</span></span>

## <span data-ttu-id="e8858-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8858-138">RELATED LINKS</span></span>
