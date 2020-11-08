---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ec1f3e70752a5386cd5dad78d867da68091b96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920665"
---
# <span data-ttu-id="fc610-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="fc610-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="fc610-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc610-102">SYNOPSIS</span></span>
<span data-ttu-id="fc610-103">Lägga till en plattform för virtuell dator från en given bild konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fc610-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="fc610-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc610-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc610-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc610-105">DESCRIPTION</span></span>
<span data-ttu-id="fc610-106">Lägg till en plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="fc610-106">Add a platform image.</span></span>

## <span data-ttu-id="fc610-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc610-107">EXAMPLES</span></span>

### <span data-ttu-id="fc610-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fc610-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="fc610-109">Lägg till en ny plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="fc610-109">Add a new platform image.</span></span>

## <span data-ttu-id="fc610-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc610-110">PARAMETERS</span></span>

### <span data-ttu-id="fc610-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc610-111">-AsJob</span></span>
<span data-ttu-id="fc610-112">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="fc610-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="fc610-113">-BillingPartNumber</span></span>
<span data-ttu-id="fc610-114">Artikel numret används för att debitera program varu kostnaderna.</span><span class="sxs-lookup"><span data-stu-id="fc610-114">The part number is used to bill for software costs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-115">-DataDisks</span><span class="sxs-lookup"><span data-stu-id="fc610-115">-DataDisks</span></span>
<span data-ttu-id="fc610-116">Data diskar som används av plattforms bilden.</span><span class="sxs-lookup"><span data-stu-id="fc610-116">Data disks used by the platform image.</span></span>

```yaml
Type: DataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fc610-117">-Force</span></span>
<span data-ttu-id="fc610-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="fc610-118">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="fc610-119">-Location</span></span>
<span data-ttu-id="fc610-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="fc610-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-121">-Ge</span><span class="sxs-lookup"><span data-stu-id="fc610-121">-Offer</span></span>
<span data-ttu-id="fc610-122">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="fc610-122">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="fc610-123">-OsType</span></span>
<span data-ttu-id="fc610-124">Typ av operativ system.</span><span class="sxs-lookup"><span data-stu-id="fc610-124">Operating system type.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="fc610-125">-OsUri</span></span>
<span data-ttu-id="fc610-126">Diskens plats.</span><span class="sxs-lookup"><span data-stu-id="fc610-126">Location of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fc610-127">-Publisher</span></span>
<span data-ttu-id="fc610-128">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="fc610-128">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="fc610-129">-Sku</span></span>
<span data-ttu-id="fc610-130">Namn på SKU.</span><span class="sxs-lookup"><span data-stu-id="fc610-130">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-131">-Version</span><span class="sxs-lookup"><span data-stu-id="fc610-131">-Version</span></span>
<span data-ttu-id="fc610-132">Versionen av Platform image för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="fc610-132">The version of the virtual machine platform image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fc610-133">-Confirm</span></span>
<span data-ttu-id="fc610-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fc610-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc610-135">-WhatIf</span></span>
<span data-ttu-id="fc610-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fc610-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc610-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fc610-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc610-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc610-138">CommonParameters</span></span>
<span data-ttu-id="fc610-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc610-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc610-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc610-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc610-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc610-141">INPUTS</span></span>

## <span data-ttu-id="fc610-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc610-142">OUTPUTS</span></span>

### <span data-ttu-id="fc610-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="fc610-143">PlatformImageObject</span></span>

## <span data-ttu-id="fc610-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc610-144">NOTES</span></span>

## <span data-ttu-id="fc610-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc610-145">RELATED LINKS</span></span>
