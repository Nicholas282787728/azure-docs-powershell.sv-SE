---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: c3fd190fb033a685bcb0d5087c544298681e47c5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093096"
---
# <span data-ttu-id="4a51c-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="4a51c-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="4a51c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a51c-102">SYNOPSIS</span></span>


## <span data-ttu-id="4a51c-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a51c-103">SYNTAX</span></span>

### <span data-ttu-id="4a51c-104">Volym (standard)</span><span class="sxs-lookup"><span data-stu-id="4a51c-104">Volume (Default)</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetScaleUnit <String> -TargetVolumeLabel <String> -Disks <IDisk[]>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4a51c-105">Resurserna</span><span class="sxs-lookup"><span data-stu-id="4a51c-105">Share</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetShare <String> -Disks <IDisk[]> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a51c-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a51c-106">DESCRIPTION</span></span>


## <span data-ttu-id="4a51c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a51c-107">EXAMPLES</span></span>

### <span data-ttu-id="4a51c-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="4a51c-108">Example 1:</span></span>
```powershell
PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

CreationTime : 2/26/2020 10:56:32 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestJob1
Location     : redmond
MigrationId  : TestJob1
Name         : redmond/TestJob1
StartTime    : 
Status       : Pending
Subtask      : {53ee3665-00e4-4c69-a067-524058905ead, d551734f-0370-4851-9704-c7cec80b34c5}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_2
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="4a51c-109">Skapa ett diskallokering för att migrera diskar till mål skalan och volymen.</span><span class="sxs-lookup"><span data-stu-id="4a51c-109">Create a disk migration job to migrate disks to the target scale unit and volume.</span></span>

### <span data-ttu-id="4a51c-110">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="4a51c-110">Example 2:</span></span> 
```powershell
PS C:\> PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob2 -TargetShare \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3 -Disks $disks
WARNING: TargetShare parameter will be deprecated in a future release, please use Volume instead.

CreationTime : 2/26/2020 11:02:48 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob2
Location     : redmond
MigrationId  : TestJob2
Name         : redmond/TestJob2
StartTime    : 
Status       : Pending
Subtask      : {0cfd8d29-1ca4-42db-a490-9198814abc50, 89c9b15e-47c6-4321-a390-611fc190cfad}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

```

<span data-ttu-id="4a51c-111">Skapa ett diskallokering för att migrera diskar till mål resursen.</span><span class="sxs-lookup"><span data-stu-id="4a51c-111">Create a disk migration job to migrate disks to the target share.</span></span>

## <span data-ttu-id="4a51c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a51c-112">PARAMETERS</span></span>

### <span data-ttu-id="4a51c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a51c-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="4a51c-114">-Diskar</span><span class="sxs-lookup"><span data-stu-id="4a51c-114">-Disks</span></span>
<span data-ttu-id="4a51c-115">Om du vill skapa läser du avsnittet anteckningar för diskar och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4a51c-115">To construct, see NOTES section for DISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4a51c-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="4a51c-116">-Location</span></span>


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

### <span data-ttu-id="4a51c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a51c-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a51c-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a51c-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="4a51c-119">-TargetScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4a51c-119">-TargetScaleUnit</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a51c-120">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="4a51c-120">-TargetShare</span></span>


```yaml
Type: System.String
Parameter Sets: Share
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a51c-121">-TargetVolumeLabel</span><span class="sxs-lookup"><span data-stu-id="4a51c-121">-TargetVolumeLabel</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a51c-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a51c-122">-Confirm</span></span>
<span data-ttu-id="4a51c-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a51c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a51c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a51c-124">-WhatIf</span></span>
<span data-ttu-id="4a51c-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a51c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a51c-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4a51c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a51c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a51c-127">CommonParameters</span></span>
<span data-ttu-id="4a51c-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a51c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a51c-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a51c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a51c-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a51c-130">INPUTS</span></span>

### <span data-ttu-id="4a51c-131">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180730Preview. IDisk []</span><span class="sxs-lookup"><span data-stu-id="4a51c-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]</span></span>

## <span data-ttu-id="4a51c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a51c-132">OUTPUTS</span></span>

### <span data-ttu-id="4a51c-133">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="4a51c-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



### <span data-ttu-id="4a51c-134">Start-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="4a51c-134">Start-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="4a51c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a51c-135">NOTES</span></span>

<span data-ttu-id="4a51c-136">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="4a51c-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a51c-137">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a51c-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4a51c-138">DISKAR <IDisk [] >:</span><span class="sxs-lookup"><span data-stu-id="4a51c-138">DISKS <IDisk[]>:</span></span> 
  - <span data-ttu-id="4a51c-139">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="4a51c-139">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4a51c-140">`[DiskId <String>]`: Disk-ID.</span><span class="sxs-lookup"><span data-stu-id="4a51c-140">`[DiskId <String>]`: The disk id.</span></span>
  - <span data-ttu-id="4a51c-141">`[SharePath <String>]`: Disk resurs Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="4a51c-141">`[SharePath <String>]`: The disk share path.</span></span>
  - <span data-ttu-id="4a51c-142">`[Status <DiskState?>]`: Diskens status.</span><span class="sxs-lookup"><span data-stu-id="4a51c-142">`[Status <DiskState?>]`: The disk status.</span></span>

## <span data-ttu-id="4a51c-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a51c-143">RELATED LINKS</span></span>

