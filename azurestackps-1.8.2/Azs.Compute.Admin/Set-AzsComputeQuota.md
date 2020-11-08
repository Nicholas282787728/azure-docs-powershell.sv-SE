---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8da912ed9751231a44c34b27df36abc62d55c4ab
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100014"
---
# <span data-ttu-id="0752e-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="0752e-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="0752e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0752e-102">SYNOPSIS</span></span>
<span data-ttu-id="0752e-103">Uppdatera en befintlig Beräknad kvot med de tillhandahållna parametrarna.</span><span class="sxs-lookup"><span data-stu-id="0752e-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="0752e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0752e-104">SYNTAX</span></span>

### <span data-ttu-id="0752e-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="0752e-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0752e-106">ID</span><span class="sxs-lookup"><span data-stu-id="0752e-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0752e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0752e-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0752e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0752e-108">DESCRIPTION</span></span>
<span data-ttu-id="0752e-109">Uppdatera en befintlig Beräknad kvot.</span><span class="sxs-lookup"><span data-stu-id="0752e-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="0752e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0752e-110">EXAMPLES</span></span>

### <span data-ttu-id="0752e-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0752e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="0752e-112">Uppdatera en beräknings kvot.</span><span class="sxs-lookup"><span data-stu-id="0752e-112">Update a compute quota.</span></span>

## <span data-ttu-id="0752e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0752e-113">PARAMETERS</span></span>

### <span data-ttu-id="0752e-114">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="0752e-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="0752e-115">Antal tillgänglighets uppsättningar som tillåts.</span><span class="sxs-lookup"><span data-stu-id="0752e-115">Number of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752e-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="0752e-116">-CoresCount</span></span>
<span data-ttu-id="0752e-117">Antal kärnor som tillåts.</span><span class="sxs-lookup"><span data-stu-id="0752e-117">Number of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0752e-118">-InputObject</span></span>
<span data-ttu-id="0752e-119">Eventuellt ändrad Beräknad kvot returnerad get-AzsComputeQuota.</span><span class="sxs-lookup"><span data-stu-id="0752e-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

```yaml
Type: ComputeQuotaObject
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0752e-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="0752e-120">-Location</span></span>
<span data-ttu-id="0752e-121">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="0752e-121">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0752e-122">-Name</span></span>
<span data-ttu-id="0752e-123">Namnet på kvoten.</span><span class="sxs-lookup"><span data-stu-id="0752e-123">The name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752e-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="0752e-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="0752e-125">Storlek för vanliga hanterade diskar och stillbilder.</span><span class="sxs-lookup"><span data-stu-id="0752e-125">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0752e-126">-ResourceId</span></span>
<span data-ttu-id="0752e-127">ID för Compute-kvoten.</span><span class="sxs-lookup"><span data-stu-id="0752e-127">The ARM compute quota id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0752e-128">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="0752e-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="0752e-129">Storlek för vanliga hanterade diskar och stillbilder.</span><span class="sxs-lookup"><span data-stu-id="0752e-129">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752e-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="0752e-130">-VirtualMachineCount</span></span>
<span data-ttu-id="0752e-131">Antal virtuella datorer som tillåts.</span><span class="sxs-lookup"><span data-stu-id="0752e-131">Number of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752e-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="0752e-132">-VmScaleSetCount</span></span>
<span data-ttu-id="0752e-133">Antal skalnings uppsättningar som tillåts.</span><span class="sxs-lookup"><span data-stu-id="0752e-133">Number of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752e-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0752e-134">-Confirm</span></span>
<span data-ttu-id="0752e-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0752e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0752e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0752e-136">-WhatIf</span></span>
<span data-ttu-id="0752e-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0752e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0752e-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0752e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0752e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0752e-139">CommonParameters</span></span>
<span data-ttu-id="0752e-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0752e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0752e-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0752e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0752e-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0752e-142">INPUTS</span></span>

## <span data-ttu-id="0752e-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0752e-143">OUTPUTS</span></span>

### <span data-ttu-id="0752e-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="0752e-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="0752e-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0752e-145">NOTES</span></span>

## <span data-ttu-id="0752e-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0752e-146">RELATED LINKS</span></span>

