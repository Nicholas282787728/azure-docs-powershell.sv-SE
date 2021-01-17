---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405864"
---
# <span data-ttu-id="e5777-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e5777-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="e5777-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5777-102">SYNOPSIS</span></span>
<span data-ttu-id="e5777-103">Lägger till en datadisk till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e5777-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="e5777-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5777-104">SYNTAX</span></span>

### <span data-ttu-id="e5777-105">VmNormalDiskParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="e5777-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5777-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e5777-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5777-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5777-107">DESCRIPTION</span></span>
<span data-ttu-id="e5777-108">Cmdleten **Add-AzVMDataDisk** lägger till en datadisk till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e5777-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="e5777-109">Du kan lägga till en datadisk när du skapar en virtuell dator eller lägga till en data disk till en befintlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e5777-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="e5777-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5777-110">EXAMPLES</span></span>

### <span data-ttu-id="e5777-111">Exempel 1: lägga till data diskar på en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="e5777-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="e5777-112">Det första kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="e5777-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e5777-113">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="e5777-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e5777-114">Nästa tre kommandon tilldelar sökvägar till tre data diskar till $DataDiskVhdUri 01-$DataDiskVhdUri 02-och $DataDiskVhdUri 03-variabler.</span><span class="sxs-lookup"><span data-stu-id="e5777-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="e5777-115">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="e5777-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="e5777-116">De tre sista kommandona lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e5777-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e5777-117">Kommandot anger namn och plats för disken och andra egenskaper för disken.</span><span class="sxs-lookup"><span data-stu-id="e5777-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="e5777-118">URI: n för varje disk lagras i $DataDiskVhdUri 01 $DataDiskVhdUri 02 och $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="e5777-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="e5777-119">Exempel 2: lägga till en datadisk till en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="e5777-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="e5777-120">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="e5777-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="e5777-121">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="e5777-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e5777-122">Det andra kommandot lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e5777-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e5777-123">Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e5777-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="e5777-124">Exempel 3: lägga till en datadisk till en ny virtuell dator från en generaliserad användar bild</span><span class="sxs-lookup"><span data-stu-id="e5777-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="e5777-125">Det första kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.</span><span class="sxs-lookup"><span data-stu-id="e5777-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e5777-126">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="e5777-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e5777-127">Nästa två kommandon tilldelar sökvägar för data-och data diskarna till $DataImageUri och $DataDiskUri variabler.</span><span class="sxs-lookup"><span data-stu-id="e5777-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="e5777-128">Den här metoden används för att förbättra läsbarheten för följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="e5777-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="e5777-129">De sista kommandona lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e5777-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e5777-130">Kommandot anger namn och plats för disken och andra egenskaper för disken.</span><span class="sxs-lookup"><span data-stu-id="e5777-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="e5777-131">Exempel 4: lägga till data diskar till en ny virtuell dator från en specialiserad användar bild</span><span class="sxs-lookup"><span data-stu-id="e5777-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="e5777-132">Det första kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.</span><span class="sxs-lookup"><span data-stu-id="e5777-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e5777-133">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="e5777-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e5777-134">Med nästa kommando kopplas sökvägar till den $DataDiskUri variabeln.</span><span class="sxs-lookup"><span data-stu-id="e5777-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="e5777-135">Den här metoden används för att förbättra läsbarheten för följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="e5777-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="e5777-136">Med kommandot sista lägger du till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e5777-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e5777-137">Kommandot anger namn och plats för disken och andra egenskaper för disken.</span><span class="sxs-lookup"><span data-stu-id="e5777-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="e5777-138">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5777-138">PARAMETERS</span></span>

### <span data-ttu-id="e5777-139">-Cachning</span><span class="sxs-lookup"><span data-stu-id="e5777-139">-Caching</span></span>
<span data-ttu-id="e5777-140">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="e5777-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="e5777-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e5777-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5777-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e5777-142">ReadOnly</span></span>
- <span data-ttu-id="e5777-143">Läs</span><span class="sxs-lookup"><span data-stu-id="e5777-143">ReadWrite</span></span>
- <span data-ttu-id="e5777-144">Ingen standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="e5777-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="e5777-145">Om du ändrar det här värdet startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="e5777-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="e5777-146">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="e5777-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="e5777-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e5777-147">-CreateOption</span></span>
<span data-ttu-id="e5777-148">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="e5777-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="e5777-149">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e5777-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5777-150">Anteckning.</span><span class="sxs-lookup"><span data-stu-id="e5777-150">Attach.</span></span>
<span data-ttu-id="e5777-151">Ange det här alternativet om du vill skapa en virtuell dator från en specialiserad disk.</span><span class="sxs-lookup"><span data-stu-id="e5777-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="e5777-152">Ange inte parametern *SourceImageUri* när du anger det här alternativet.</span><span class="sxs-lookup"><span data-stu-id="e5777-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="e5777-153">*VhdUri* är allt som behövs för att det ska bli så att Azure Platform anger platsen för den virtuella hård disken (VHD) som ska kopplas till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e5777-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="e5777-154">Tomt.</span><span class="sxs-lookup"><span data-stu-id="e5777-154">Empty.</span></span>
<span data-ttu-id="e5777-155">Ange detta för att skapa en tom data disk.</span><span class="sxs-lookup"><span data-stu-id="e5777-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="e5777-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="e5777-156">FromImage.</span></span>
<span data-ttu-id="e5777-157">Ange det här alternativet om du vill skapa en virtuell dator från en allmän bild eller disk.</span><span class="sxs-lookup"><span data-stu-id="e5777-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="e5777-158">När du anger det här alternativet måste du ange parametern *SourceImageUri* även för att berätta för Azure Platform platsen för den virtuella hård disk som ska bifogas som en data skiva.</span><span class="sxs-lookup"><span data-stu-id="e5777-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="e5777-159">Parametern *VhdUri* används som den plats där data diskens VHD lagras när den används av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e5777-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="e5777-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5777-160">-DefaultProfile</span></span>
<span data-ttu-id="e5777-161">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5777-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5777-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e5777-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e5777-163">Anger resurs-ID för kund hanterad disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e5777-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="e5777-164">Detta kan endast anges för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="e5777-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="e5777-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e5777-165">-DiskSizeInGB</span></span>
<span data-ttu-id="e5777-166">Anger storleken i GB på en tom disk som ska kopplas till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e5777-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="e5777-167">-LUN</span><span class="sxs-lookup"><span data-stu-id="e5777-167">-Lun</span></span>
<span data-ttu-id="e5777-168">Anger LUN (Logical Unit Number) för en data disk.</span><span class="sxs-lookup"><span data-stu-id="e5777-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="e5777-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="e5777-169">-ManagedDiskId</span></span>
<span data-ttu-id="e5777-170">Anger ID för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="e5777-170">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="e5777-171">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5777-171">-Name</span></span>
<span data-ttu-id="e5777-172">Anger namnet på den datadisk som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="e5777-172">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5777-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="e5777-173">-SourceImageUri</span></span>
<span data-ttu-id="e5777-174">Anger källans URI för disken som cmdleten kopplas till.</span><span class="sxs-lookup"><span data-stu-id="e5777-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="e5777-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e5777-175">-StorageAccountType</span></span>
<span data-ttu-id="e5777-176">Anger lagrings konto typen för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="e5777-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5777-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="e5777-177">-VhdUri</span></span>
<span data-ttu-id="e5777-178">Anger URI (Uniform Resource Identifier) för den virtuella hård disk (VHD)-filen som ska skapas när en plattforms bild eller användar bild används.</span><span class="sxs-lookup"><span data-stu-id="e5777-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="e5777-179">Denna cmdlet kopierar det binära Large Object (BLOB) till den här platsen.</span><span class="sxs-lookup"><span data-stu-id="e5777-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="e5777-180">Det här är den plats där den virtuella datorn startas.</span><span class="sxs-lookup"><span data-stu-id="e5777-180">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="e5777-181">-VM</span><span class="sxs-lookup"><span data-stu-id="e5777-181">-VM</span></span>
<span data-ttu-id="e5777-182">Anger det lokala virtuella dator objekt där en data disk ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="e5777-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="e5777-183">Du kan använda cmdleten **Get-AzVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="e5777-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="e5777-184">Du kan använda cmdleten **New-AzVMConfig** för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="e5777-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5777-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e5777-185">-WriteAccelerator</span></span>
<span data-ttu-id="e5777-186">Anger om WriteAccelerator ska aktive ras eller inaktive ras på en hanterad data disk.</span><span class="sxs-lookup"><span data-stu-id="e5777-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5777-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5777-187">CommonParameters</span></span>
<span data-ttu-id="e5777-188">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5777-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5777-189">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5777-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5777-190">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5777-190">INPUTS</span></span>

### <span data-ttu-id="e5777-191">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e5777-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e5777-192">System. String</span><span class="sxs-lookup"><span data-stu-id="e5777-192">System.String</span></span>

### <span data-ttu-id="e5777-193">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="e5777-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="e5777-194">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e5777-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e5777-195">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5777-195">OUTPUTS</span></span>

### <span data-ttu-id="e5777-196">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e5777-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e5777-197">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e5777-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="e5777-198">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5777-198">NOTES</span></span>

## <span data-ttu-id="e5777-199">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5777-199">RELATED LINKS</span></span>

[<span data-ttu-id="e5777-200">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e5777-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="e5777-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e5777-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e5777-202">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e5777-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
