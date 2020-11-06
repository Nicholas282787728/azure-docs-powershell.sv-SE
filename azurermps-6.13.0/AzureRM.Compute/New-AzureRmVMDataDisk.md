---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMDataDisk.md
ms.openlocfilehash: 6eb86e0c2ddb8c5e3a46cf10f98bcea52ba03dd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580260"
---
# <span data-ttu-id="60d40-101">New-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="60d40-101">New-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="60d40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60d40-102">SYNOPSIS</span></span>
<span data-ttu-id="60d40-103">Skapar ett lokalt data disk objekt för en virtuell dator eller en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="60d40-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60d40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60d40-104">SYNTAX</span></span>

### <span data-ttu-id="60d40-105">NormalDiskParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="60d40-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzureRmVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60d40-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="60d40-106">ManagedDiskParameterSetName</span></span>
```
New-AzureRmVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60d40-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60d40-107">DESCRIPTION</span></span>
<span data-ttu-id="60d40-108">Cmdleten **New-AzureRmVMDataDisk** skapar ett lokalt data disk objekt för en virtuell dator eller en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="60d40-108">The **New-AzureRmVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="60d40-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60d40-109">EXAMPLES</span></span>

### <span data-ttu-id="60d40-110">Exempel 1: lägga till en hanterad datadisk till en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="60d40-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzureRmVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="60d40-111">Det första kommandot får en befintlig hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="60d40-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="60d40-112">Med nästa kommando skapas ett data disk objekt med den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="60d40-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="60d40-113">Nästa kommando hämtar en befintlig VMSS-VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="60d40-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="60d40-114">Det sista kommandot uppdaterar den VMSS virtuella datorn genom att lägga till en ny data skiva.</span><span class="sxs-lookup"><span data-stu-id="60d40-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="60d40-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60d40-115">PARAMETERS</span></span>

### <span data-ttu-id="60d40-116">-Cachning</span><span class="sxs-lookup"><span data-stu-id="60d40-116">-Caching</span></span>
<span data-ttu-id="60d40-117">Cachelagring av data disk för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="60d40-117">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="60d40-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="60d40-118">-CreateOption</span></span>
<span data-ttu-id="60d40-119">Skapa ett alternativ för data disk för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="60d40-119">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="60d40-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d40-120">-DefaultProfile</span></span>
<span data-ttu-id="60d40-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60d40-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60d40-122">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="60d40-122">-DiskSizeInGB</span></span>
<span data-ttu-id="60d40-123">Data diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="60d40-123">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="60d40-124">-LUN</span><span class="sxs-lookup"><span data-stu-id="60d40-124">-Lun</span></span>
<span data-ttu-id="60d40-125">LUN för den virtuella datorns data disk.</span><span class="sxs-lookup"><span data-stu-id="60d40-125">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="60d40-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="60d40-126">-ManagedDiskId</span></span>
<span data-ttu-id="60d40-127">Den virtuella datorns hanterade disk-ID.</span><span class="sxs-lookup"><span data-stu-id="60d40-127">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="60d40-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="60d40-128">-Name</span></span>
<span data-ttu-id="60d40-129">Namnet på den virtuella datorns data disk.</span><span class="sxs-lookup"><span data-stu-id="60d40-129">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="60d40-130">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="60d40-130">-SourceImageUri</span></span>
<span data-ttu-id="60d40-131">OS-webbplatsens URI för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="60d40-131">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="60d40-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="60d40-132">-StorageAccountType</span></span>
<span data-ttu-id="60d40-133">Den virtuella datorns kontotyp.</span><span class="sxs-lookup"><span data-stu-id="60d40-133">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="60d40-134">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="60d40-134">-VhdUri</span></span>
<span data-ttu-id="60d40-135">VHD URI för virtuell dator data disk.</span><span class="sxs-lookup"><span data-stu-id="60d40-135">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="60d40-136">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="60d40-136">-WriteAccelerator</span></span>
<span data-ttu-id="60d40-137">Anger om WriteAccelerator ska aktive ras eller inaktive ras på en hanterad data disk.</span><span class="sxs-lookup"><span data-stu-id="60d40-137">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="60d40-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d40-138">CommonParameters</span></span>
<span data-ttu-id="60d40-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60d40-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d40-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60d40-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d40-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60d40-141">INPUTS</span></span>

### <span data-ttu-id="60d40-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="60d40-142">System.Int32</span></span>

### <span data-ttu-id="60d40-143">System. String</span><span class="sxs-lookup"><span data-stu-id="60d40-143">System.String</span></span>

### <span data-ttu-id="60d40-144">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="60d40-144">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="60d40-145">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="60d40-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="60d40-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60d40-146">OUTPUTS</span></span>

### <span data-ttu-id="60d40-147">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="60d40-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="60d40-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60d40-148">NOTES</span></span>

## <span data-ttu-id="60d40-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60d40-149">RELATED LINKS</span></span>
