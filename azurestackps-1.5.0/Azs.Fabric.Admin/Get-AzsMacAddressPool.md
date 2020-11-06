---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5c686faa457d83ab0ddffb932b20ab5fcd168ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572320"
---
# <span data-ttu-id="146db-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="146db-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="146db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="146db-102">SYNOPSIS</span></span>
<span data-ttu-id="146db-103">Returnerar en lista över alla MAC-adresspooler på en plats.</span><span class="sxs-lookup"><span data-stu-id="146db-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="146db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="146db-104">SYNTAX</span></span>

### <span data-ttu-id="146db-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="146db-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="146db-106">Lära</span><span class="sxs-lookup"><span data-stu-id="146db-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="146db-107">ID</span><span class="sxs-lookup"><span data-stu-id="146db-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="146db-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="146db-108">DESCRIPTION</span></span>
<span data-ttu-id="146db-109">Returnerar en lista över alla MAC-adresspooler på en plats.</span><span class="sxs-lookup"><span data-stu-id="146db-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="146db-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="146db-110">EXAMPLES</span></span>

### <span data-ttu-id="146db-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="146db-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="146db-112">Hämta alla MAC-adresspooler på en plats.</span><span class="sxs-lookup"><span data-stu-id="146db-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="146db-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="146db-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="146db-114">Skaffa en MAC-adresspool på en plats baserad på namn.</span><span class="sxs-lookup"><span data-stu-id="146db-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="146db-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="146db-115">PARAMETERS</span></span>

### <span data-ttu-id="146db-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="146db-116">-Filter</span></span>
<span data-ttu-id="146db-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="146db-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="146db-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="146db-118">-Location</span></span>
<span data-ttu-id="146db-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="146db-119">Location of the resource.</span></span>

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

### <span data-ttu-id="146db-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="146db-120">-Name</span></span>
<span data-ttu-id="146db-121">Namn på MAC-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="146db-121">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="146db-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="146db-122">-ResourceGroupName</span></span>
<span data-ttu-id="146db-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="146db-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="146db-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="146db-124">-ResourceId</span></span>
<span data-ttu-id="146db-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="146db-125">The resource id.</span></span>

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

### <span data-ttu-id="146db-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="146db-126">-Skip</span></span>
<span data-ttu-id="146db-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="146db-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="146db-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="146db-128">-Top</span></span>
<span data-ttu-id="146db-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="146db-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="146db-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="146db-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="146db-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="146db-131">CommonParameters</span></span>
<span data-ttu-id="146db-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="146db-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="146db-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="146db-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="146db-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="146db-134">INPUTS</span></span>

## <span data-ttu-id="146db-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="146db-135">OUTPUTS</span></span>

### <span data-ttu-id="146db-136">Microsoft. AzureStack. Management. Fabric. admin. Models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="146db-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="146db-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="146db-137">NOTES</span></span>

## <span data-ttu-id="146db-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="146db-138">RELATED LINKS</span></span>

