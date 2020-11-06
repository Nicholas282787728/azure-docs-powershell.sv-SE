---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f81cf1ed28b822a0686d1db71541585023f1e57b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571335"
---
# <span data-ttu-id="8eb34-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="8eb34-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="8eb34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8eb34-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb34-103">Returnerar befintliga bild tillägg för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8eb34-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="8eb34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8eb34-104">SYNTAX</span></span>

### <span data-ttu-id="8eb34-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8eb34-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="8eb34-106">Lära</span><span class="sxs-lookup"><span data-stu-id="8eb34-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8eb34-107">ID</span><span class="sxs-lookup"><span data-stu-id="8eb34-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8eb34-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8eb34-108">DESCRIPTION</span></span>
<span data-ttu-id="8eb34-109">Returnerar bild tillägg för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8eb34-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="8eb34-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8eb34-110">EXAMPLES</span></span>

### <span data-ttu-id="8eb34-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8eb34-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="8eb34-112">Hämta alla virtuella dator tillägg på en plats.</span><span class="sxs-lookup"><span data-stu-id="8eb34-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="8eb34-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8eb34-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="8eb34-114">Hämta specifikt virtuellt dator tillägg.</span><span class="sxs-lookup"><span data-stu-id="8eb34-114">Get specific VM extension.</span></span>

## <span data-ttu-id="8eb34-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8eb34-115">PARAMETERS</span></span>

### <span data-ttu-id="8eb34-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="8eb34-116">-Location</span></span>
<span data-ttu-id="8eb34-117">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="8eb34-117">Location of the resource.</span></span>

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

### <span data-ttu-id="8eb34-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8eb34-118">-Publisher</span></span>
<span data-ttu-id="8eb34-119">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="8eb34-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="8eb34-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eb34-120">-ResourceId</span></span>
<span data-ttu-id="8eb34-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="8eb34-121">The resource id.</span></span>

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

### <span data-ttu-id="8eb34-122">– Skriv</span><span class="sxs-lookup"><span data-stu-id="8eb34-122">-Type</span></span>
<span data-ttu-id="8eb34-123">Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="8eb34-123">Type of extension.</span></span>

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

### <span data-ttu-id="8eb34-124">-Version</span><span class="sxs-lookup"><span data-stu-id="8eb34-124">-Version</span></span>
<span data-ttu-id="8eb34-125">Den virtuella datorns versions tillägg.</span><span class="sxs-lookup"><span data-stu-id="8eb34-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="8eb34-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb34-126">CommonParameters</span></span>
<span data-ttu-id="8eb34-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eb34-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb34-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb34-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb34-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8eb34-129">INPUTS</span></span>

## <span data-ttu-id="8eb34-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8eb34-130">OUTPUTS</span></span>

### <span data-ttu-id="8eb34-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="8eb34-131">VmExtensionObject</span></span>

## <span data-ttu-id="8eb34-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8eb34-132">NOTES</span></span>

## <span data-ttu-id="8eb34-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8eb34-133">RELATED LINKS</span></span>

