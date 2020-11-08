---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099946"
---
# <span data-ttu-id="398a1-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="398a1-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="398a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="398a1-102">SYNOPSIS</span></span>


## <span data-ttu-id="398a1-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="398a1-103">SYNTAX</span></span>

### <span data-ttu-id="398a1-104">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="398a1-104">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="398a1-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="398a1-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="398a1-106">UpdateExpanded</span><span class="sxs-lookup"><span data-stu-id="398a1-106">UpdateExpanded</span></span>
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## <span data-ttu-id="398a1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="398a1-107">DESCRIPTION</span></span>
<span data-ttu-id="398a1-108">Uppdatera en beräknings kvot</span><span class="sxs-lookup"><span data-stu-id="398a1-108">Update a Compute Quota</span></span>

## <span data-ttu-id="398a1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="398a1-109">EXAMPLES</span></span>

### <span data-ttu-id="398a1-110">Exempel 1: Ange egenskaper för en befintlig Beräknad kvot</span><span class="sxs-lookup"><span data-stu-id="398a1-110">Example 1: Set Properties on an Existing Compute Quota</span></span>
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

<span data-ttu-id="398a1-111">Ange parametrarna som anges på kommando raden.</span><span class="sxs-lookup"><span data-stu-id="398a1-111">Set the parameters specified on the command line.</span></span>
<span data-ttu-id="398a1-112">Alla parametrar som inte är inställda blir standardvärden 0</span><span class="sxs-lookup"><span data-stu-id="398a1-112">Any parameters not set will default to 0</span></span>

## <span data-ttu-id="398a1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="398a1-113">PARAMETERS</span></span>

### <span data-ttu-id="398a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="398a1-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="398a1-115">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="398a1-115">-NewQuota</span></span>
<span data-ttu-id="398a1-116">För att konstruera kan du läsa avsnittet anteckningar för NEWQUOTA-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="398a1-116">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

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

### <span data-ttu-id="398a1-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="398a1-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="398a1-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="398a1-118">-Confirm</span></span>
<span data-ttu-id="398a1-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="398a1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="398a1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="398a1-120">-WhatIf</span></span>
<span data-ttu-id="398a1-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="398a1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="398a1-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="398a1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="398a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="398a1-123">CommonParameters</span></span>
<span data-ttu-id="398a1-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="398a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="398a1-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="398a1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="398a1-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="398a1-126">INPUTS</span></span>

### <span data-ttu-id="398a1-127">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="398a1-127">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="398a1-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="398a1-128">OUTPUTS</span></span>

### <span data-ttu-id="398a1-129">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="398a1-129">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="398a1-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="398a1-130">NOTES</span></span>

<span data-ttu-id="398a1-131">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="398a1-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="398a1-132">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="398a1-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="398a1-133">NEWQUOTA <IQuota> :</span><span class="sxs-lookup"><span data-stu-id="398a1-133">NEWQUOTA <IQuota>:</span></span> 
  - <span data-ttu-id="398a1-134">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="398a1-134">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="398a1-135">`[AvailabilitySetCount <Int32?>]`: Maximalt antal tillåtna tillgänglighets uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="398a1-135">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="398a1-136">`[CoresLimit <Int32?>]`: Högsta antal tillåtna kärnor.</span><span class="sxs-lookup"><span data-stu-id="398a1-136">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="398a1-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximalt antal hanterade diskar och ögonblicks bilder av typen Premium är tillåtna.</span><span class="sxs-lookup"><span data-stu-id="398a1-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="398a1-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximalt antal hanterade diskar och ögonblicks bilder av typen Standard är tillåtna.</span><span class="sxs-lookup"><span data-stu-id="398a1-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="398a1-139">`[VMScaleSetCount <Int32?>]`: Maximalt antal skalnings uppsättningar tillåts.</span><span class="sxs-lookup"><span data-stu-id="398a1-139">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="398a1-140">`[VirtualMachineCount <Int32?>]`: Maximalt antal virtuella datorer tillåts.</span><span class="sxs-lookup"><span data-stu-id="398a1-140">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="398a1-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="398a1-141">RELATED LINKS</span></span>

