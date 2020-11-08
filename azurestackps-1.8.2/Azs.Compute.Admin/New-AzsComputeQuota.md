---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffd2667f8c07c5b0594abe38f6cee5d40ce91a49
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100021"
---
# <span data-ttu-id="b8239-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b8239-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="b8239-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8239-102">SYNOPSIS</span></span>
<span data-ttu-id="b8239-103">Skapa en ny Beräknad kvot som används för att begränsa beräknings resurserna.</span><span class="sxs-lookup"><span data-stu-id="b8239-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="b8239-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8239-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8239-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8239-105">DESCRIPTION</span></span>
<span data-ttu-id="b8239-106">Skapa en ny Beräknad kvot.</span><span class="sxs-lookup"><span data-stu-id="b8239-106">Create a new compute quota.</span></span>

## <span data-ttu-id="b8239-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8239-107">EXAMPLES</span></span>

### <span data-ttu-id="b8239-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8239-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="b8239-109">Skapa en ny Beräknad kvot.</span><span class="sxs-lookup"><span data-stu-id="b8239-109">Create a new compute quota.</span></span>

## <span data-ttu-id="b8239-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8239-110">PARAMETERS</span></span>

### <span data-ttu-id="b8239-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="b8239-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="b8239-112">Antal tillgänglighets uppsättningar som tillåts.</span><span class="sxs-lookup"><span data-stu-id="b8239-112">Number  of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8239-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="b8239-113">-CoresCount</span></span>
<span data-ttu-id="b8239-114">Antal kärnor som tillåts.</span><span class="sxs-lookup"><span data-stu-id="b8239-114">Number  of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: 3
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8239-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="b8239-115">-Location</span></span>
<span data-ttu-id="b8239-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="b8239-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8239-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8239-117">-Name</span></span>
<span data-ttu-id="b8239-118">Namn på kvoten.</span><span class="sxs-lookup"><span data-stu-id="b8239-118">Name of the quota.</span></span>

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

### <span data-ttu-id="b8239-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="b8239-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="b8239-120">Storlek för vanliga hanterade diskar och stillbilder.</span><span class="sxs-lookup"><span data-stu-id="b8239-120">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8239-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="b8239-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="b8239-122">Storlek för vanliga hanterade diskar och stillbilder.</span><span class="sxs-lookup"><span data-stu-id="b8239-122">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8239-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="b8239-123">-VirtualMachineCount</span></span>
<span data-ttu-id="b8239-124">Antal virtuella datorer som tillåts.</span><span class="sxs-lookup"><span data-stu-id="b8239-124">Number  of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8239-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="b8239-125">-VmScaleSetCount</span></span>
<span data-ttu-id="b8239-126">Antal skalnings uppsättningar som tillåts.</span><span class="sxs-lookup"><span data-stu-id="b8239-126">Number  of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8239-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8239-127">-Confirm</span></span>
<span data-ttu-id="b8239-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8239-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8239-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8239-129">-WhatIf</span></span>
<span data-ttu-id="b8239-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8239-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8239-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8239-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8239-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8239-132">CommonParameters</span></span>
<span data-ttu-id="b8239-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8239-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8239-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8239-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8239-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8239-135">INPUTS</span></span>

## <span data-ttu-id="b8239-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8239-136">OUTPUTS</span></span>

### <span data-ttu-id="b8239-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="b8239-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="b8239-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8239-138">NOTES</span></span>

## <span data-ttu-id="b8239-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8239-139">RELATED LINKS</span></span>
