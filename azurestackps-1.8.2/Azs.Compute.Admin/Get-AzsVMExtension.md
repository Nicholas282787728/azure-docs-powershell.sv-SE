---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7eac7b9d23914aa909a111958d64cc9d4247d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099861"
---
# <span data-ttu-id="0d9c0-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0d9c0-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="0d9c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d9c0-102">SYNOPSIS</span></span>
<span data-ttu-id="0d9c0-103">Returnerar befintliga bild tillägg för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="0d9c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d9c0-104">SYNTAX</span></span>

### <span data-ttu-id="0d9c0-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="0d9c0-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d9c0-106">Lära</span><span class="sxs-lookup"><span data-stu-id="0d9c0-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d9c0-107">ID</span><span class="sxs-lookup"><span data-stu-id="0d9c0-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0d9c0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d9c0-108">DESCRIPTION</span></span>
<span data-ttu-id="0d9c0-109">Returnerar bild tillägg för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="0d9c0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d9c0-110">EXAMPLES</span></span>

### <span data-ttu-id="0d9c0-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0d9c0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="0d9c0-112">Hämta alla virtuella dator tillägg på en plats.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="0d9c0-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0d9c0-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="0d9c0-114">Hämta specifikt virtuellt dator tillägg.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-114">Get specific VM extension.</span></span>

## <span data-ttu-id="0d9c0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d9c0-115">PARAMETERS</span></span>

### <span data-ttu-id="0d9c0-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="0d9c0-116">-Location</span></span>
<span data-ttu-id="0d9c0-117">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-117">Location of the resource.</span></span>

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

### <span data-ttu-id="0d9c0-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0d9c0-118">-Publisher</span></span>
<span data-ttu-id="0d9c0-119">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="0d9c0-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d9c0-120">-ResourceId</span></span>
<span data-ttu-id="0d9c0-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-121">The resource id.</span></span>

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

### <span data-ttu-id="0d9c0-122">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0d9c0-122">-Type</span></span>
<span data-ttu-id="0d9c0-123">Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-123">Type of extension.</span></span>

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

### <span data-ttu-id="0d9c0-124">-Version</span><span class="sxs-lookup"><span data-stu-id="0d9c0-124">-Version</span></span>
<span data-ttu-id="0d9c0-125">Den virtuella datorns versions tillägg.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="0d9c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d9c0-126">CommonParameters</span></span>
<span data-ttu-id="0d9c0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d9c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d9c0-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d9c0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d9c0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d9c0-129">INPUTS</span></span>

## <span data-ttu-id="0d9c0-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d9c0-130">OUTPUTS</span></span>

### <span data-ttu-id="0d9c0-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="0d9c0-131">VmExtensionObject</span></span>

## <span data-ttu-id="0d9c0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d9c0-132">NOTES</span></span>

## <span data-ttu-id="0d9c0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d9c0-133">RELATED LINKS</span></span>

