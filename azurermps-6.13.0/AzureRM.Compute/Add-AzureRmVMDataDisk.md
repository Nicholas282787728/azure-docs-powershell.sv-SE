---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: de0f5fd2583f1622e750e71299a5753444feed1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580831"
---
# <span data-ttu-id="b0750-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b0750-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="b0750-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0750-102">SYNOPSIS</span></span>
<span data-ttu-id="b0750-103">Lägger till en datadisk till en virtuell dator eller en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="b0750-103">Adds a data disk to a virtual machine or a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0750-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0750-104">SYNTAX</span></span>

### <span data-ttu-id="b0750-105">VmNormalDiskParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="b0750-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String>
 [[-SourceImageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0750-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b0750-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0750-107">VmScaleSetVMParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b0750-107">VmScaleSetVMParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [-ManagedDiskId] <String>
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0750-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0750-108">DESCRIPTION</span></span>
<span data-ttu-id="b0750-109">Cmdleten **Add-AzureRmVMDataDisk** lägger till en datadisk till en virtuell dator eller en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="b0750-109">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine or a Vmss VM.</span></span>
<span data-ttu-id="b0750-110">Du kan lägga till en datadisk när du skapar en virtuell dator eller lägga till en data disk till en befintlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b0750-110">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="b0750-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0750-111">EXAMPLES</span></span>

### <span data-ttu-id="b0750-112">Exempel 1: lägga till data diskar på en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="b0750-112">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="b0750-113">Det första kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="b0750-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b0750-114">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="b0750-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b0750-115">Nästa tre kommandon tilldelar sökvägar till tre data diskar till $DataDiskVhdUri 01-$DataDiskVhdUri 02-och $DataDiskVhdUri 03-variabler.</span><span class="sxs-lookup"><span data-stu-id="b0750-115">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="b0750-116">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="b0750-116">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="b0750-117">De tre sista kommandona lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b0750-117">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b0750-118">Kommandot anger namn och plats för disken och andra egenskaper för disken.</span><span class="sxs-lookup"><span data-stu-id="b0750-118">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="b0750-119">URI: n för varje disk lagras i $DataDiskVhdUri 01 $DataDiskVhdUri 02 och $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="b0750-119">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="b0750-120">Exempel 2: lägga till en datadisk till en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="b0750-120">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="b0750-121">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="b0750-121">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="b0750-122">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="b0750-122">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b0750-123">Det andra kommandot lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b0750-123">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b0750-124">Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b0750-124">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="b0750-125">Exempel 3: lägga till en datadisk till en ny virtuell dator från en generaliserad användar bild</span><span class="sxs-lookup"><span data-stu-id="b0750-125">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="b0750-126">Det första kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.</span><span class="sxs-lookup"><span data-stu-id="b0750-126">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b0750-127">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="b0750-127">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b0750-128">Nästa två kommandon tilldelar sökvägar för data-och data diskarna till $DataImageUri och $DataDiskUri variabler.</span><span class="sxs-lookup"><span data-stu-id="b0750-128">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="b0750-129">Den här metoden används för att förbättra läsbarheten för följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="b0750-129">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="b0750-130">De sista kommandona lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b0750-130">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b0750-131">Kommandot anger namn och plats för disken och andra egenskaper för disken.</span><span class="sxs-lookup"><span data-stu-id="b0750-131">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="b0750-132">Exempel 4: lägga till data diskar till en ny virtuell dator från en specialiserad användar bild</span><span class="sxs-lookup"><span data-stu-id="b0750-132">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="b0750-133">Det första kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.</span><span class="sxs-lookup"><span data-stu-id="b0750-133">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b0750-134">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="b0750-134">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b0750-135">Med nästa kommando kopplas sökvägar till den $DataDiskUri variabeln.</span><span class="sxs-lookup"><span data-stu-id="b0750-135">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="b0750-136">Den här metoden används för att förbättra läsbarheten för följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="b0750-136">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="b0750-137">Med kommandot sista lägger du till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b0750-137">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b0750-138">Kommandot anger namn och plats för disken och andra egenskaper för disken.</span><span class="sxs-lookup"><span data-stu-id="b0750-138">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

### <span data-ttu-id="b0750-139">Exempel 5: lägga till en hanterad datadisk till en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="b0750-139">Example 5: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="b0750-140">Det första kommandot får en befintlig hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="b0750-140">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="b0750-141">Nästa kommando hämtar en befintlig VMSS-VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="b0750-141">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="b0750-142">Nästa kommando lägger till den hanterade disken till den lokala VMSS VM i $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="b0750-142">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="b0750-143">Det sista kommandot uppdaterar den VMSS virtuella dator med tillagd data skiva.</span><span class="sxs-lookup"><span data-stu-id="b0750-143">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="b0750-144">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0750-144">PARAMETERS</span></span>

### <span data-ttu-id="b0750-145">-Cachning</span><span class="sxs-lookup"><span data-stu-id="b0750-145">-Caching</span></span>
<span data-ttu-id="b0750-146">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="b0750-146">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="b0750-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b0750-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b0750-148">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b0750-148">ReadOnly</span></span>
- <span data-ttu-id="b0750-149">Läs</span><span class="sxs-lookup"><span data-stu-id="b0750-149">ReadWrite</span></span>
- <span data-ttu-id="b0750-150">Ingen standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="b0750-150">None The default value is ReadWrite.</span></span>
<span data-ttu-id="b0750-151">Om du ändrar det här värdet startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="b0750-151">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="b0750-152">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="b0750-152">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-153">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="b0750-153">-CreateOption</span></span>
<span data-ttu-id="b0750-154">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="b0750-154">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="b0750-155">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b0750-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b0750-156">Anteckning.</span><span class="sxs-lookup"><span data-stu-id="b0750-156">Attach.</span></span>
<span data-ttu-id="b0750-157">Ange det här alternativet om du vill skapa en virtuell dator från en specialiserad disk.</span><span class="sxs-lookup"><span data-stu-id="b0750-157">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="b0750-158">Ange inte parametern *SourceImageUri* när du anger det här alternativet.</span><span class="sxs-lookup"><span data-stu-id="b0750-158">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="b0750-159">*VhdUri* är allt som behövs för att det ska bli så att Azure Platform anger platsen för den virtuella hård disken (VHD) som ska kopplas till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b0750-159">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="b0750-160">Tomt.</span><span class="sxs-lookup"><span data-stu-id="b0750-160">Empty.</span></span>
<span data-ttu-id="b0750-161">Ange detta för att skapa en tom data disk.</span><span class="sxs-lookup"><span data-stu-id="b0750-161">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="b0750-162">FromImage.</span><span class="sxs-lookup"><span data-stu-id="b0750-162">FromImage.</span></span>
<span data-ttu-id="b0750-163">Ange det här alternativet om du vill skapa en virtuell dator från en allmän bild eller disk.</span><span class="sxs-lookup"><span data-stu-id="b0750-163">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="b0750-164">När du anger det här alternativet måste du ange parametern *SourceImageUri* även för att berätta för Azure Platform platsen för den virtuella hård disk som ska bifogas som en data skiva.</span><span class="sxs-lookup"><span data-stu-id="b0750-164">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="b0750-165">Parametern *VhdUri* används som den plats där data diskens VHD lagras när den används av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b0750-165">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0750-166">-DefaultProfile</span></span>
<span data-ttu-id="b0750-167">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0750-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0750-168">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="b0750-168">-DiskSizeInGB</span></span>
<span data-ttu-id="b0750-169">Anger storleken i GB på en tom disk som ska kopplas till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b0750-169">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-170">-LUN</span><span class="sxs-lookup"><span data-stu-id="b0750-170">-Lun</span></span>
<span data-ttu-id="b0750-171">Anger LUN (Logical Unit Number) för en data disk.</span><span class="sxs-lookup"><span data-stu-id="b0750-171">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="b0750-172">-ManagedDiskId</span></span>
<span data-ttu-id="b0750-173">Anger ID för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="b0750-173">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-174">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0750-174">-Name</span></span>
<span data-ttu-id="b0750-175">Anger namnet på den datadisk som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="b0750-175">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="b0750-176">-SourceImageUri</span></span>
<span data-ttu-id="b0750-177">Anger källans URI för disken som cmdleten kopplas till.</span><span class="sxs-lookup"><span data-stu-id="b0750-177">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b0750-178">-StorageAccountType</span></span>
<span data-ttu-id="b0750-179">Anger lagrings konto typen för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="b0750-179">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="b0750-180">-VhdUri</span></span>
<span data-ttu-id="b0750-181">Anger URI (Uniform Resource Identifier) för den virtuella hård disk (VHD)-filen som ska skapas när en plattforms bild eller användar bild används.</span><span class="sxs-lookup"><span data-stu-id="b0750-181">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="b0750-182">Denna cmdlet kopierar det binära Large Object (BLOB) till den här platsen.</span><span class="sxs-lookup"><span data-stu-id="b0750-182">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="b0750-183">Det här är den plats där den virtuella datorn startas.</span><span class="sxs-lookup"><span data-stu-id="b0750-183">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-184">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="b0750-184">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="b0750-185">Anger den lokala virtuella datorns skala ange det virtuella dator objekt där du vill lägga till en data disk.</span><span class="sxs-lookup"><span data-stu-id="b0750-185">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="b0750-186">Du kan använda cmdleten **Get-AzureRmVmssVM** för att erhålla en virtuell dators skala ange virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="b0750-186">You can use the **Get-AzureRmVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-187">-VM</span><span class="sxs-lookup"><span data-stu-id="b0750-187">-VM</span></span>
<span data-ttu-id="b0750-188">Anger det lokala virtuella dator objekt där en data disk ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="b0750-188">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="b0750-189">Du kan använda cmdleten **Get-AzureRmVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="b0750-189">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="b0750-190">Du kan använda cmdleten **New-AzureRmVMConfig** för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="b0750-190">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-191">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b0750-191">-WriteAccelerator</span></span>
<span data-ttu-id="b0750-192">Anger om WriteAccelerator ska aktive ras eller inaktive ras på en hanterad data disk.</span><span class="sxs-lookup"><span data-stu-id="b0750-192">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0750-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0750-193">CommonParameters</span></span>
<span data-ttu-id="b0750-194">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0750-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0750-195">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0750-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0750-196">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0750-196">INPUTS</span></span>

### <span data-ttu-id="b0750-197">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b0750-197">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b0750-198">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="b0750-198">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="b0750-199">System. String</span><span class="sxs-lookup"><span data-stu-id="b0750-199">System.String</span></span>

### <span data-ttu-id="b0750-200">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="b0750-200">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="b0750-201">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b0750-201">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b0750-202">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0750-202">OUTPUTS</span></span>

### <span data-ttu-id="b0750-203">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b0750-203">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b0750-204">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="b0750-204">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="b0750-205">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0750-205">NOTES</span></span>

## <span data-ttu-id="b0750-206">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0750-206">RELATED LINKS</span></span>

[<span data-ttu-id="b0750-207">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b0750-207">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="b0750-208">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b0750-208">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b0750-209">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="b0750-209">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
