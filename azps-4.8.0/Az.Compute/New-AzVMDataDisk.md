---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 4eefa5a0a22b3db0e7ab10085729e1040dbd4e71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102350"
---
# <span data-ttu-id="49d59-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="49d59-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="49d59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49d59-102">SYNOPSIS</span></span>
<span data-ttu-id="49d59-103">Skapar ett lokalt data disk objekt för en virtuell dator eller en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="49d59-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="49d59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49d59-104">SYNTAX</span></span>

### <span data-ttu-id="49d59-105">NormalDiskParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="49d59-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49d59-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="49d59-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49d59-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49d59-107">DESCRIPTION</span></span>
<span data-ttu-id="49d59-108">Cmdleten **New-AzVMDataDisk** skapar ett lokalt data disk objekt för en virtuell dator eller en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="49d59-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="49d59-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49d59-109">EXAMPLES</span></span>

### <span data-ttu-id="49d59-110">Exempel 1: lägga till en hanterad datadisk till en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="49d59-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="49d59-111">Det första kommandot får en befintlig hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="49d59-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="49d59-112">Med nästa kommando skapas ett data disk objekt med den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="49d59-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="49d59-113">Nästa kommando hämtar en befintlig VMSS-VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="49d59-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="49d59-114">Det sista kommandot uppdaterar den VMSS virtuella datorn genom att lägga till en ny data skiva.</span><span class="sxs-lookup"><span data-stu-id="49d59-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="49d59-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="49d59-115">Example 2</span></span>

<span data-ttu-id="49d59-116">Skapar ett lokalt data disk objekt för en virtuell dator eller en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="49d59-116">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span> <span data-ttu-id="49d59-117">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="49d59-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVMDataDisk -Caching None -CreateOption Attach -DiskSizeInGB 1 -Lun 2 -Name 'AgentPool01'
```

## <span data-ttu-id="49d59-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49d59-118">PARAMETERS</span></span>

### <span data-ttu-id="49d59-119">-Cachning</span><span class="sxs-lookup"><span data-stu-id="49d59-119">-Caching</span></span>
<span data-ttu-id="49d59-120">Cachelagring av data disk för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="49d59-120">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="49d59-121">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="49d59-121">-CreateOption</span></span>
<span data-ttu-id="49d59-122">Skapa ett alternativ för data disk för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="49d59-122">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="49d59-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d59-123">-DefaultProfile</span></span>
<span data-ttu-id="49d59-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49d59-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49d59-125">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="49d59-125">-DiskEncryptionSetId</span></span>
<span data-ttu-id="49d59-126">Den virtuella datorns ID för hanterade disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="49d59-126">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="49d59-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="49d59-127">-DiskSizeInGB</span></span>
<span data-ttu-id="49d59-128">Data diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="49d59-128">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="49d59-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="49d59-129">-Lun</span></span>
<span data-ttu-id="49d59-130">LUN för den virtuella datorns data disk.</span><span class="sxs-lookup"><span data-stu-id="49d59-130">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="49d59-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="49d59-131">-ManagedDiskId</span></span>
<span data-ttu-id="49d59-132">Den virtuella datorns hanterade disk-ID.</span><span class="sxs-lookup"><span data-stu-id="49d59-132">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="49d59-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="49d59-133">-Name</span></span>
<span data-ttu-id="49d59-134">Namnet på den virtuella datorns data disk.</span><span class="sxs-lookup"><span data-stu-id="49d59-134">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="49d59-135">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="49d59-135">-SourceImageUri</span></span>
<span data-ttu-id="49d59-136">OS-webbplatsens URI för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="49d59-136">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="49d59-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="49d59-137">-StorageAccountType</span></span>
<span data-ttu-id="49d59-138">Den virtuella datorns kontotyp.</span><span class="sxs-lookup"><span data-stu-id="49d59-138">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="49d59-139">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="49d59-139">-VhdUri</span></span>
<span data-ttu-id="49d59-140">VHD URI för virtuell dator data disk.</span><span class="sxs-lookup"><span data-stu-id="49d59-140">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="49d59-141">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="49d59-141">-WriteAccelerator</span></span>
<span data-ttu-id="49d59-142">Anger om WriteAccelerator ska aktive ras eller inaktive ras på en hanterad data disk.</span><span class="sxs-lookup"><span data-stu-id="49d59-142">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="49d59-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d59-143">CommonParameters</span></span>
<span data-ttu-id="49d59-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49d59-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d59-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49d59-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d59-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49d59-146">INPUTS</span></span>

### <span data-ttu-id="49d59-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="49d59-147">System.Int32</span></span>

### <span data-ttu-id="49d59-148">System. String</span><span class="sxs-lookup"><span data-stu-id="49d59-148">System.String</span></span>

### <span data-ttu-id="49d59-149">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="49d59-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="49d59-150">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="49d59-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="49d59-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49d59-151">OUTPUTS</span></span>

### <span data-ttu-id="49d59-152">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="49d59-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="49d59-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49d59-153">NOTES</span></span>

## <span data-ttu-id="49d59-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49d59-154">RELATED LINKS</span></span>
