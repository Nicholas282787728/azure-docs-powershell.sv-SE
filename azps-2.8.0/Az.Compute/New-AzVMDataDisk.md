---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: d7ce0b96c4ab286e21c253d701ec6d21c385ac56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745081"
---
# <span data-ttu-id="52c6d-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="52c6d-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="52c6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="52c6d-103">Skapar ett lokalt data disk objekt för en virtuell dator eller en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="52c6d-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="52c6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52c6d-104">SYNTAX</span></span>

### <span data-ttu-id="52c6d-105">NormalDiskParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="52c6d-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52c6d-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="52c6d-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52c6d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52c6d-107">DESCRIPTION</span></span>
<span data-ttu-id="52c6d-108">Cmdleten **New-AzVMDataDisk** skapar ett lokalt data disk objekt för en virtuell dator eller en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="52c6d-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="52c6d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52c6d-109">EXAMPLES</span></span>

### <span data-ttu-id="52c6d-110">Exempel 1: lägga till en hanterad datadisk till en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="52c6d-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="52c6d-111">Det första kommandot får en befintlig hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="52c6d-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="52c6d-112">Med nästa kommando skapas ett data disk objekt med den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="52c6d-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="52c6d-113">Nästa kommando hämtar en befintlig VMSS-VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="52c6d-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="52c6d-114">Det sista kommandot uppdaterar den VMSS virtuella datorn genom att lägga till en ny data skiva.</span><span class="sxs-lookup"><span data-stu-id="52c6d-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="52c6d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52c6d-115">PARAMETERS</span></span>

### <span data-ttu-id="52c6d-116">-Cachning</span><span class="sxs-lookup"><span data-stu-id="52c6d-116">-Caching</span></span>
<span data-ttu-id="52c6d-117">Cachelagring av data disk för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="52c6d-117">The virtual machine data disk's caching.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c6d-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="52c6d-118">-CreateOption</span></span>
<span data-ttu-id="52c6d-119">Skapa ett alternativ för data disk för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="52c6d-119">The virtual machine data disk's create option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c6d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c6d-120">-DefaultProfile</span></span>
<span data-ttu-id="52c6d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52c6d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c6d-122">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="52c6d-122">-DiskSizeInGB</span></span>
<span data-ttu-id="52c6d-123">Data diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="52c6d-123">The virtual machine data disk's size in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c6d-124">-LUN</span><span class="sxs-lookup"><span data-stu-id="52c6d-124">-Lun</span></span>
<span data-ttu-id="52c6d-125">LUN för den virtuella datorns data disk.</span><span class="sxs-lookup"><span data-stu-id="52c6d-125">The virtual machine data disk's Lun.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c6d-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="52c6d-126">-ManagedDiskId</span></span>
<span data-ttu-id="52c6d-127">Den virtuella datorns hanterade disk-ID.</span><span class="sxs-lookup"><span data-stu-id="52c6d-127">The virtual machine managed disk's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c6d-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="52c6d-128">-Name</span></span>
<span data-ttu-id="52c6d-129">Namnet på den virtuella datorns data disk.</span><span class="sxs-lookup"><span data-stu-id="52c6d-129">The virtual machine data disk's name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c6d-130">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="52c6d-130">-SourceImageUri</span></span>
<span data-ttu-id="52c6d-131">OS-webbplatsens URI för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="52c6d-131">The virtual machine OS disk's source image Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c6d-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="52c6d-132">-StorageAccountType</span></span>
<span data-ttu-id="52c6d-133">Den virtuella datorns kontotyp.</span><span class="sxs-lookup"><span data-stu-id="52c6d-133">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c6d-134">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="52c6d-134">-VhdUri</span></span>
<span data-ttu-id="52c6d-135">VHD URI för virtuell dator data disk.</span><span class="sxs-lookup"><span data-stu-id="52c6d-135">The virtual machine data disk's Vhd Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c6d-136">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="52c6d-136">-WriteAccelerator</span></span>
<span data-ttu-id="52c6d-137">Anger om WriteAccelerator ska aktive ras eller inaktive ras på en hanterad data disk.</span><span class="sxs-lookup"><span data-stu-id="52c6d-137">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c6d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c6d-138">CommonParameters</span></span>
<span data-ttu-id="52c6d-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52c6d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c6d-140">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52c6d-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c6d-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52c6d-141">INPUTS</span></span>

### <span data-ttu-id="52c6d-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="52c6d-142">System.Int32</span></span>

### <span data-ttu-id="52c6d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="52c6d-143">System.String</span></span>

### <span data-ttu-id="52c6d-144">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="52c6d-144">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="52c6d-145">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52c6d-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="52c6d-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52c6d-146">OUTPUTS</span></span>

### <span data-ttu-id="52c6d-147">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="52c6d-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="52c6d-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52c6d-148">NOTES</span></span>

## <span data-ttu-id="52c6d-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52c6d-149">RELATED LINKS</span></span>
