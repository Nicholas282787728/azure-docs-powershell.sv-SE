---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527027"
---
# <span data-ttu-id="d642b-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d642b-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="d642b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d642b-102">SYNOPSIS</span></span>
<span data-ttu-id="d642b-103">Lägger till en datadisk till en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="d642b-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="d642b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d642b-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d642b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d642b-105">DESCRIPTION</span></span>
<span data-ttu-id="d642b-106">Cmdleten **Add-AzVmssVMDataDisk** lägger till en datadisk till en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="d642b-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="d642b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d642b-107">EXAMPLES</span></span>

### <span data-ttu-id="d642b-108">Exempel 1: lägga till en hanterad datadisk till en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="d642b-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="d642b-109">Det första kommandot får en befintlig hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="d642b-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="d642b-110">Nästa kommando hämtar en befintlig VMSS-VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="d642b-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="d642b-111">Nästa kommando lägger till den hanterade disken till den lokala VMSS VM i $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="d642b-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="d642b-112">Det sista kommandot uppdaterar den VMSS virtuella dator med tillagd data skiva.</span><span class="sxs-lookup"><span data-stu-id="d642b-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="d642b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d642b-113">PARAMETERS</span></span>

### <span data-ttu-id="d642b-114">-Cachning</span><span class="sxs-lookup"><span data-stu-id="d642b-114">-Caching</span></span>
<span data-ttu-id="d642b-115">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="d642b-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="d642b-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d642b-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d642b-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d642b-117">ReadOnly</span></span>
- <span data-ttu-id="d642b-118">Läs</span><span class="sxs-lookup"><span data-stu-id="d642b-118">ReadWrite</span></span>
- <span data-ttu-id="d642b-119">Ingen standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="d642b-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="d642b-120">Om du ändrar det här värdet startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="d642b-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="d642b-121">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="d642b-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="d642b-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="d642b-122">-CreateOption</span></span>
<span data-ttu-id="d642b-123">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="d642b-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="d642b-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d642b-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d642b-125">Anteckning.</span><span class="sxs-lookup"><span data-stu-id="d642b-125">Attach.</span></span>
<span data-ttu-id="d642b-126">Ange det här alternativet om du vill skapa en virtuell dator från en specialiserad disk.</span><span class="sxs-lookup"><span data-stu-id="d642b-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="d642b-127">Ange inte parametern *SourceImageUri* när du anger det här alternativet.</span><span class="sxs-lookup"><span data-stu-id="d642b-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="d642b-128">*VhdUri* är allt som behövs för att det ska bli så att Azure Platform anger platsen för den virtuella hård disken (VHD) som ska kopplas till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d642b-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="d642b-129">Tomt.</span><span class="sxs-lookup"><span data-stu-id="d642b-129">Empty.</span></span>
<span data-ttu-id="d642b-130">Ange detta för att skapa en tom data disk.</span><span class="sxs-lookup"><span data-stu-id="d642b-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="d642b-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="d642b-131">FromImage.</span></span>
<span data-ttu-id="d642b-132">Ange det här alternativet om du vill skapa en virtuell dator från en allmän bild eller disk.</span><span class="sxs-lookup"><span data-stu-id="d642b-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="d642b-133">När du anger det här alternativet måste du ange parametern *SourceImageUri* även för att berätta för Azure Platform platsen för den virtuella hård disk som ska bifogas som en data skiva.</span><span class="sxs-lookup"><span data-stu-id="d642b-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="d642b-134">Parametern *VhdUri* används som den plats där data diskens VHD lagras när den används av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d642b-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d642b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d642b-135">-DefaultProfile</span></span>
<span data-ttu-id="d642b-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d642b-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d642b-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="d642b-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="d642b-138">Anger resurs-ID för kund hanterad disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="d642b-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="d642b-139">Detta kan endast anges för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="d642b-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="d642b-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="d642b-140">-DiskSizeInGB</span></span>
<span data-ttu-id="d642b-141">Anger storleken i GB på en tom disk som ska kopplas till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d642b-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d642b-142">-LUN</span><span class="sxs-lookup"><span data-stu-id="d642b-142">-Lun</span></span>
<span data-ttu-id="d642b-143">Anger LUN (Logical Unit Number) för en data disk.</span><span class="sxs-lookup"><span data-stu-id="d642b-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d642b-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="d642b-144">-ManagedDiskId</span></span>
<span data-ttu-id="d642b-145">Anger ID för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="d642b-145">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d642b-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d642b-146">-StorageAccountType</span></span>
<span data-ttu-id="d642b-147">Anger lagrings konto typen för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="d642b-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="d642b-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="d642b-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="d642b-149">Anger den lokala virtuella datorns skala ange det virtuella dator objekt där du vill lägga till en data disk.</span><span class="sxs-lookup"><span data-stu-id="d642b-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="d642b-150">Du kan använda cmdleten **Get-AzVmssVM** för att erhålla en virtuell dators skala ange virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="d642b-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d642b-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d642b-151">-WriteAccelerator</span></span>
<span data-ttu-id="d642b-152">Anger om WriteAccelerator ska aktive ras eller inaktive ras på en hanterad data disk.</span><span class="sxs-lookup"><span data-stu-id="d642b-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d642b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d642b-153">CommonParameters</span></span>
<span data-ttu-id="d642b-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d642b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d642b-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d642b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d642b-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d642b-156">INPUTS</span></span>

### <span data-ttu-id="d642b-157">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="d642b-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="d642b-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d642b-158">System.Int32</span></span>

### <span data-ttu-id="d642b-159">System. String</span><span class="sxs-lookup"><span data-stu-id="d642b-159">System.String</span></span>

### <span data-ttu-id="d642b-160">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="d642b-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="d642b-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d642b-161">OUTPUTS</span></span>

### <span data-ttu-id="d642b-162">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="d642b-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="d642b-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d642b-163">NOTES</span></span>

## <span data-ttu-id="d642b-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d642b-164">RELATED LINKS</span></span>
