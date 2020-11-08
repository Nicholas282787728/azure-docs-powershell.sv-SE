---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 7f67b8b6ff287a98fc505cb63c3a6eda90f46ef7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089168"
---
# <span data-ttu-id="dc090-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="dc090-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="dc090-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc090-102">SYNOPSIS</span></span>
<span data-ttu-id="dc090-103">Skapar ett lokalt data disk objekt för en virtuell dator eller en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="dc090-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="dc090-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc090-104">SYNTAX</span></span>

### <span data-ttu-id="dc090-105">NormalDiskParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="dc090-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc090-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="dc090-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc090-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc090-107">DESCRIPTION</span></span>
<span data-ttu-id="dc090-108">Cmdleten **New-AzVMDataDisk** skapar ett lokalt data disk objekt för en virtuell dator eller en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="dc090-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="dc090-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc090-109">EXAMPLES</span></span>

### <span data-ttu-id="dc090-110">Exempel 1: lägga till en hanterad datadisk till en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="dc090-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="dc090-111">Det första kommandot får en befintlig hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="dc090-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="dc090-112">Med nästa kommando skapas ett data disk objekt med den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="dc090-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="dc090-113">Nästa kommando hämtar en befintlig VMSS-VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="dc090-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="dc090-114">Det sista kommandot uppdaterar den VMSS virtuella datorn genom att lägga till en ny data skiva.</span><span class="sxs-lookup"><span data-stu-id="dc090-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="dc090-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc090-115">PARAMETERS</span></span>

### <span data-ttu-id="dc090-116">-Cachning</span><span class="sxs-lookup"><span data-stu-id="dc090-116">-Caching</span></span>
<span data-ttu-id="dc090-117">Cachelagring av data disk för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dc090-117">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="dc090-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="dc090-118">-CreateOption</span></span>
<span data-ttu-id="dc090-119">Skapa ett alternativ för data disk för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dc090-119">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="dc090-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc090-120">-DefaultProfile</span></span>
<span data-ttu-id="dc090-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc090-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc090-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="dc090-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="dc090-123">Den virtuella datorns ID för hanterade disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="dc090-123">The virtual machine managed disk encryption set's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc090-124">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="dc090-124">-DiskSizeInGB</span></span>
<span data-ttu-id="dc090-125">Data diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="dc090-125">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="dc090-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="dc090-126">-Lun</span></span>
<span data-ttu-id="dc090-127">LUN för den virtuella datorns data disk.</span><span class="sxs-lookup"><span data-stu-id="dc090-127">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="dc090-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="dc090-128">-ManagedDiskId</span></span>
<span data-ttu-id="dc090-129">Den virtuella datorns hanterade disk-ID.</span><span class="sxs-lookup"><span data-stu-id="dc090-129">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="dc090-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc090-130">-Name</span></span>
<span data-ttu-id="dc090-131">Namnet på den virtuella datorns data disk.</span><span class="sxs-lookup"><span data-stu-id="dc090-131">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="dc090-132">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="dc090-132">-SourceImageUri</span></span>
<span data-ttu-id="dc090-133">OS-webbplatsens URI för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dc090-133">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="dc090-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="dc090-134">-StorageAccountType</span></span>
<span data-ttu-id="dc090-135">Den virtuella datorns kontotyp.</span><span class="sxs-lookup"><span data-stu-id="dc090-135">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="dc090-136">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="dc090-136">-VhdUri</span></span>
<span data-ttu-id="dc090-137">VHD URI för virtuell dator data disk.</span><span class="sxs-lookup"><span data-stu-id="dc090-137">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="dc090-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="dc090-138">-WriteAccelerator</span></span>
<span data-ttu-id="dc090-139">Anger om WriteAccelerator ska aktive ras eller inaktive ras på en hanterad data disk.</span><span class="sxs-lookup"><span data-stu-id="dc090-139">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="dc090-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc090-140">CommonParameters</span></span>
<span data-ttu-id="dc090-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc090-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc090-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc090-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc090-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc090-143">INPUTS</span></span>

### <span data-ttu-id="dc090-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dc090-144">System.Int32</span></span>

### <span data-ttu-id="dc090-145">System. String</span><span class="sxs-lookup"><span data-stu-id="dc090-145">System.String</span></span>

### <span data-ttu-id="dc090-146">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="dc090-146">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="dc090-147">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dc090-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dc090-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc090-148">OUTPUTS</span></span>

### <span data-ttu-id="dc090-149">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="dc090-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="dc090-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc090-150">NOTES</span></span>

## <span data-ttu-id="dc090-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc090-151">RELATED LINKS</span></span>
