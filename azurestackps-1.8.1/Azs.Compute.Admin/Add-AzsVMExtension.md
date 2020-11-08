---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0390c3f55c444b4a0e37e25c93536b60d10bc7b1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921694"
---
# <span data-ttu-id="0e029-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0e029-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="0e029-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e029-102">SYNOPSIS</span></span>
<span data-ttu-id="0e029-103">Skapa en ny tilläggs bild för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0e029-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="0e029-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e029-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e029-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e029-105">DESCRIPTION</span></span>
<span data-ttu-id="0e029-106">Skapa en tilläggs bild för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0e029-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="0e029-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e029-107">EXAMPLES</span></span>

### <span data-ttu-id="0e029-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0e029-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="0e029-109">Lägga till ett nytt plattforms bild tillägg.</span><span class="sxs-lookup"><span data-stu-id="0e029-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="0e029-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e029-110">PARAMETERS</span></span>

### <span data-ttu-id="0e029-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e029-111">-AsJob</span></span>
<span data-ttu-id="0e029-112">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="0e029-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0e029-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="0e029-113">-ComputeRole</span></span>
<span data-ttu-id="0e029-114">Typen av roll, IaaS eller PaaS, stöder det här tillägget.</span><span class="sxs-lookup"><span data-stu-id="0e029-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

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

### <span data-ttu-id="0e029-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0e029-115">-Force</span></span>
<span data-ttu-id="0e029-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0e029-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0e029-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="0e029-117">-IsSystemExtension</span></span>
<span data-ttu-id="0e029-118">Anger om fil namns tillägget är för systemet.</span><span class="sxs-lookup"><span data-stu-id="0e029-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="0e029-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="0e029-119">-Location</span></span>
<span data-ttu-id="0e029-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="0e029-120">Location of the resource.</span></span>

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

### <span data-ttu-id="0e029-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0e029-121">-Publisher</span></span>
<span data-ttu-id="0e029-122">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="0e029-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="0e029-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="0e029-123">-SourceBlob</span></span>
<span data-ttu-id="0e029-124">URI till paket för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0e029-124">URI to virtual machine extension package.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e029-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="0e029-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="0e029-126">True om det har stöd för flera tillägg.</span><span class="sxs-lookup"><span data-stu-id="0e029-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="0e029-127">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0e029-127">-Type</span></span>
<span data-ttu-id="0e029-128">Typ av tillägg.</span><span class="sxs-lookup"><span data-stu-id="0e029-128">Type of extension.</span></span>

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

### <span data-ttu-id="0e029-129">-Version</span><span class="sxs-lookup"><span data-stu-id="0e029-129">-Version</span></span>
<span data-ttu-id="0e029-130">Versionen av dator bild tillägget för vritual.</span><span class="sxs-lookup"><span data-stu-id="0e029-130">The version of the vritual machine image extension.</span></span>

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

### <span data-ttu-id="0e029-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="0e029-131">-VmOsType</span></span>
<span data-ttu-id="0e029-132">Typ av operativ system för virtuell dator som behövs för att distribuera tilläggs hanteraren.</span><span class="sxs-lookup"><span data-stu-id="0e029-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="0e029-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="0e029-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="0e029-134">Värde som anger om tillägget är aktiverat för stöd för virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="0e029-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="0e029-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e029-135">-Confirm</span></span>
<span data-ttu-id="0e029-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e029-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e029-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e029-137">-WhatIf</span></span>
<span data-ttu-id="0e029-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e029-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e029-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e029-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e029-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e029-140">CommonParameters</span></span>
<span data-ttu-id="0e029-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e029-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e029-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e029-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e029-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e029-143">INPUTS</span></span>

## <span data-ttu-id="0e029-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e029-144">OUTPUTS</span></span>

### <span data-ttu-id="0e029-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="0e029-145">VmExtensionObject</span></span>

## <span data-ttu-id="0e029-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e029-146">NOTES</span></span>

## <span data-ttu-id="0e029-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e029-147">RELATED LINKS</span></span>
