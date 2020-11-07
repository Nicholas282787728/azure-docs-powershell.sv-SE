---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925429"
---
# <span data-ttu-id="00ca8-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="00ca8-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="00ca8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00ca8-102">SYNOPSIS</span></span>


## <span data-ttu-id="00ca8-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00ca8-103">SYNTAX</span></span>

### <span data-ttu-id="00ca8-104">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="00ca8-104">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="00ca8-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="00ca8-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="00ca8-106">UpdateExpanded</span><span class="sxs-lookup"><span data-stu-id="00ca8-106">UpdateExpanded</span></span>
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## <span data-ttu-id="00ca8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00ca8-107">DESCRIPTION</span></span>
<span data-ttu-id="00ca8-108">Uppdatera en beräknings kvot</span><span class="sxs-lookup"><span data-stu-id="00ca8-108">Update a Compute Quota</span></span>

## <span data-ttu-id="00ca8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00ca8-109">EXAMPLES</span></span>

### <span data-ttu-id="00ca8-110">Exempel 1: Ange egenskaper för en befintlig Beräknad kvot</span><span class="sxs-lookup"><span data-stu-id="00ca8-110">Example 1: Set Properties on an Existing Compute Quota</span></span>
```powershell
PS C:\> $myComputeQuota = Get-AzsComputeQuota -Name MyComputeQuota

PS C:\> $myComputeQuota.CoresLimit = 99; 

PS C:\> Set-AzsComputeQuota -NewQuota $myComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 99
Id                                 : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/northwest/quotas/MyComputeQuota
Location                           : northwest
Name                               : MyComputeQuota
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="00ca8-111">Ange parametrarna som anges på kommando raden.</span><span class="sxs-lookup"><span data-stu-id="00ca8-111">Set the parameters specified on the command line.</span></span>
<span data-ttu-id="00ca8-112">Alla parametrar som inte är inställda blir standardvärden 0</span><span class="sxs-lookup"><span data-stu-id="00ca8-112">Any parameters not set will default to 0</span></span>

## <span data-ttu-id="00ca8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00ca8-113">PARAMETERS</span></span>

### <span data-ttu-id="00ca8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ca8-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="00ca8-115">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="00ca8-115">-NewQuota</span></span>
<span data-ttu-id="00ca8-116">För att konstruera kan du läsa avsnittet anteckningar för NEWQUOTA-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="00ca8-116">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="00ca8-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00ca8-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="00ca8-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="00ca8-118">-Confirm</span></span>
<span data-ttu-id="00ca8-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="00ca8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00ca8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00ca8-120">-WhatIf</span></span>
<span data-ttu-id="00ca8-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="00ca8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00ca8-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="00ca8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00ca8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ca8-123">CommonParameters</span></span>
<span data-ttu-id="00ca8-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ca8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ca8-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00ca8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ca8-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00ca8-126">INPUTS</span></span>

### <span data-ttu-id="00ca8-127">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="00ca8-127">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="00ca8-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00ca8-128">OUTPUTS</span></span>

### <span data-ttu-id="00ca8-129">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="00ca8-129">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="00ca8-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00ca8-130">NOTES</span></span>

<span data-ttu-id="00ca8-131">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="00ca8-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00ca8-132">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="00ca8-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="00ca8-133">NEWQUOTA <IQuota> :</span><span class="sxs-lookup"><span data-stu-id="00ca8-133">NEWQUOTA <IQuota>:</span></span> 
  - <span data-ttu-id="00ca8-134">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="00ca8-134">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="00ca8-135">`[AvailabilitySetCount <Int32?>]`: Maximalt antal tillåtna tillgänglighets uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="00ca8-135">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="00ca8-136">`[CoresLimit <Int32?>]`: Högsta antal tillåtna kärnor.</span><span class="sxs-lookup"><span data-stu-id="00ca8-136">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="00ca8-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximalt antal hanterade diskar och ögonblicks bilder av typen Premium är tillåtna.</span><span class="sxs-lookup"><span data-stu-id="00ca8-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="00ca8-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximalt antal hanterade diskar och ögonblicks bilder av typen Standard är tillåtna.</span><span class="sxs-lookup"><span data-stu-id="00ca8-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="00ca8-139">`[VMScaleSetCount <Int32?>]`: Maximalt antal skalnings uppsättningar tillåts.</span><span class="sxs-lookup"><span data-stu-id="00ca8-139">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="00ca8-140">`[VirtualMachineCount <Int32?>]`: Maximalt antal virtuella datorer tillåts.</span><span class="sxs-lookup"><span data-stu-id="00ca8-140">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="00ca8-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00ca8-141">RELATED LINKS</span></span>

