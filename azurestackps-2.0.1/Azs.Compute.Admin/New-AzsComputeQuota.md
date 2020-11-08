---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093097"
---
# <span data-ttu-id="05aac-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="05aac-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="05aac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05aac-102">SYNOPSIS</span></span>
<span data-ttu-id="05aac-103">Skapar eller uppdaterar en beräknings kvot med de tillhandahållna kvot parametrarna.</span><span class="sxs-lookup"><span data-stu-id="05aac-103">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="05aac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05aac-104">SYNTAX</span></span>

### <span data-ttu-id="05aac-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="05aac-105">CreateExpanded (Default)</span></span>
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="05aac-106">Göra</span><span class="sxs-lookup"><span data-stu-id="05aac-106">Create</span></span>
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="05aac-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05aac-107">DESCRIPTION</span></span>
<span data-ttu-id="05aac-108">Skapar eller uppdaterar en beräknings kvot med de tillhandahållna kvot parametrarna.</span><span class="sxs-lookup"><span data-stu-id="05aac-108">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="05aac-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05aac-109">EXAMPLES</span></span>

### <span data-ttu-id="05aac-110">Exempel 1: skapa en beräknings kvot med standard parametrar</span><span class="sxs-lookup"><span data-stu-id="05aac-110">Example 1: Create a Compute Quota with Default Parameters</span></span>
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="05aac-111">Alla parametrar som inte är angivna kommer att anges som standard parameter och visas ovan.</span><span class="sxs-lookup"><span data-stu-id="05aac-111">Any parameters that are not specified will be set to their default parameter, shown above.</span></span>

### <span data-ttu-id="05aac-112">Exempel 2: skapa en beräknings kvot med anpassade parametrar</span><span class="sxs-lookup"><span data-stu-id="05aac-112">Example 2: Create a Compute Quota with Custom Parameters</span></span>
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

<span data-ttu-id="05aac-113">Anpassa kvoten med parametrar.</span><span class="sxs-lookup"><span data-stu-id="05aac-113">Customize Quota with parameters.</span></span> <span data-ttu-id="05aac-114">Inga parametrar har angetts.</span><span class="sxs-lookup"><span data-stu-id="05aac-114">Any parameters not specified will have default value.</span></span>

## <span data-ttu-id="05aac-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05aac-115">PARAMETERS</span></span>

### <span data-ttu-id="05aac-116">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="05aac-116">-AvailabilitySetCount</span></span>
<span data-ttu-id="05aac-117">Maximalt antal tillåtna tillgänglighets uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="05aac-117">Maximum number of availability sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-118">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="05aac-118">-CoresCount</span></span>
<span data-ttu-id="05aac-119">Maximalt antal tillåtna kärnor.</span><span class="sxs-lookup"><span data-stu-id="05aac-119">Maximum number of cores allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05aac-120">-DefaultProfile</span></span>
<span data-ttu-id="05aac-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05aac-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="05aac-122">-Location</span></span>
<span data-ttu-id="05aac-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="05aac-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-124">-Location1</span><span class="sxs-lookup"><span data-stu-id="05aac-124">-Location1</span></span>
<span data-ttu-id="05aac-125">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="05aac-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="05aac-126">-Name</span></span>
<span data-ttu-id="05aac-127">Namn på kvoten.</span><span class="sxs-lookup"><span data-stu-id="05aac-127">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-128">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="05aac-128">-NewQuota</span></span>
<span data-ttu-id="05aac-129">Lagrar kvot information som används för att styra resursallokeringen.</span><span class="sxs-lookup"><span data-stu-id="05aac-129">Holds Compute quota information used to control resource allocation.</span></span>
<span data-ttu-id="05aac-130">För att konstruera kan du läsa avsnittet anteckningar för NEWQUOTA-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="05aac-130">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-131">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="05aac-131">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="05aac-132">Maximalt antal hanterade diskar och stillbilder av typen Premium tillåts.</span><span class="sxs-lookup"><span data-stu-id="05aac-132">Maximum number of managed disks and snapshots of type premium allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-133">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="05aac-133">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="05aac-134">Maximalt antal hanterade diskar och stillbilder av typen standard tillåts.</span><span class="sxs-lookup"><span data-stu-id="05aac-134">Maximum number of managed disks and snapshots of type standard allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05aac-135">-SubscriptionId</span></span>
<span data-ttu-id="05aac-136">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="05aac-136">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="05aac-137">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="05aac-137">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-138">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="05aac-138">-VirtualMachineCount</span></span>
<span data-ttu-id="05aac-139">Maximalt antal virtuella datorer tillåts.</span><span class="sxs-lookup"><span data-stu-id="05aac-139">Maximum number of virtual machines allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-140">-VMScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="05aac-140">-VMScaleSetCount</span></span>
<span data-ttu-id="05aac-141">Maximalt antal skalnings uppsättningar tillåts.</span><span class="sxs-lookup"><span data-stu-id="05aac-141">Maximum number of scale sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05aac-142">-Confirm</span></span>
<span data-ttu-id="05aac-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05aac-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05aac-144">-WhatIf</span></span>
<span data-ttu-id="05aac-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05aac-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05aac-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05aac-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05aac-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05aac-147">CommonParameters</span></span>
<span data-ttu-id="05aac-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05aac-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05aac-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05aac-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05aac-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05aac-150">INPUTS</span></span>

### <span data-ttu-id="05aac-151">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="05aac-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="05aac-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05aac-152">OUTPUTS</span></span>

### <span data-ttu-id="05aac-153">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="05aac-153">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="05aac-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05aac-154">NOTES</span></span>

<span data-ttu-id="05aac-155">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="05aac-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05aac-156">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="05aac-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="05aac-157">NEWQUOTA <IQuota> : lagrar kvot information som används för att styra resursallokeringen.</span><span class="sxs-lookup"><span data-stu-id="05aac-157">NEWQUOTA <IQuota>: Holds Compute quota information used to control resource allocation.</span></span>
  - <span data-ttu-id="05aac-158">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="05aac-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="05aac-159">`[AvailabilitySetCount <Int32?>]`: Maximalt antal tillåtna tillgänglighets uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="05aac-159">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="05aac-160">`[CoresLimit <Int32?>]`: Högsta antal tillåtna kärnor.</span><span class="sxs-lookup"><span data-stu-id="05aac-160">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="05aac-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximalt antal hanterade diskar och ögonblicks bilder av typen Premium är tillåtna.</span><span class="sxs-lookup"><span data-stu-id="05aac-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="05aac-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximalt antal hanterade diskar och ögonblicks bilder av typen Standard är tillåtna.</span><span class="sxs-lookup"><span data-stu-id="05aac-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="05aac-163">`[VMScaleSetCount <Int32?>]`: Maximalt antal skalnings uppsättningar tillåts.</span><span class="sxs-lookup"><span data-stu-id="05aac-163">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="05aac-164">`[VirtualMachineCount <Int32?>]`: Maximalt antal virtuella datorer tillåts.</span><span class="sxs-lookup"><span data-stu-id="05aac-164">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="05aac-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05aac-165">RELATED LINKS</span></span>

