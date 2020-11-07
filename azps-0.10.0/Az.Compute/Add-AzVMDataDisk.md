---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 4c7e59b847ec1ae1d95c5a884c8979d12d193084
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923065"
---
# <span data-ttu-id="d3c6b-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d3c6b-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="d3c6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c6b-103">Lägger till en datadisk till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="d3c6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3c6b-104">SYNTAX</span></span>

```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3c6b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3c6b-105">DESCRIPTION</span></span>
<span data-ttu-id="d3c6b-106">Cmdleten **Add-AzVMDataDisk** lägger till en datadisk till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-106">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="d3c6b-107">Du kan lägga till en datadisk när du skapar en virtuell dator eller lägga till en data disk till en befintlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="d3c6b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3c6b-108">EXAMPLES</span></span>

### <span data-ttu-id="d3c6b-109">Exempel 1: lägga till data diskar på en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="d3c6b-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="d3c6b-110">Det första kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d3c6b-111">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="d3c6b-112">Nästa tre kommandon tilldelar sökvägar till tre data diskar till $DataDiskVhdUri 01-$DataDiskVhdUri 02-och $DataDiskVhdUri 03-variabler.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="d3c6b-113">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="d3c6b-114">De tre sista kommandona lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d3c6b-115">Kommandot anger namn och plats för disken och andra egenskaper för disken.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="d3c6b-116">URI: n för varje disk lagras i $DataDiskVhdUri 01 $DataDiskVhdUri 02 och $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="d3c6b-117">Exempel 2: lägga till en datadisk till en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="d3c6b-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="d3c6b-118">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="d3c6b-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="d3c6b-119">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="d3c6b-120">Det andra kommandot lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="d3c6b-121">Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="d3c6b-122">Exempel 3: lägga till en datadisk till en ny virtuell dator från en generaliserad användar bild</span><span class="sxs-lookup"><span data-stu-id="d3c6b-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="d3c6b-123">Det första kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d3c6b-124">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="d3c6b-125">Nästa två kommandon tilldelar sökvägar för data-och data diskarna till $DataImageUri och $DataDiskUri variabler.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="d3c6b-126">Den här metoden används för att förbättra läsbarheten för följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="d3c6b-127">De sista kommandona lägger till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d3c6b-128">Kommandot anger namn och plats för disken och andra egenskaper för disken.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="d3c6b-129">Exempel 4: lägga till data diskar till en ny virtuell dator från en specialiserad användar bild</span><span class="sxs-lookup"><span data-stu-id="d3c6b-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="d3c6b-130">Det första kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d3c6b-131">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="d3c6b-132">Med nästa kommando kopplas sökvägar till den $DataDiskUri variabeln.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="d3c6b-133">Den här metoden används för att förbättra läsbarheten för följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="d3c6b-134">Med kommandot sista lägger du till en datadisk till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d3c6b-135">Kommandot anger namn och plats för disken och andra egenskaper för disken.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="d3c6b-136">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3c6b-136">PARAMETERS</span></span>

### <span data-ttu-id="d3c6b-137">-Cachning</span><span class="sxs-lookup"><span data-stu-id="d3c6b-137">-Caching</span></span>
<span data-ttu-id="d3c6b-138">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="d3c6b-139">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d3c6b-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d3c6b-140">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d3c6b-140">ReadOnly</span></span>
- <span data-ttu-id="d3c6b-141">Läs</span><span class="sxs-lookup"><span data-stu-id="d3c6b-141">ReadWrite</span></span>
- <span data-ttu-id="d3c6b-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="d3c6b-142">None</span></span>

<span data-ttu-id="d3c6b-143">Standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="d3c6b-144">Om du ändrar det här värdet startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="d3c6b-145">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-146">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="d3c6b-146">-CreateOption</span></span>
<span data-ttu-id="d3c6b-147">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="d3c6b-148">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d3c6b-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d3c6b-149">Anteckning.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-149">Attach.</span></span>
<span data-ttu-id="d3c6b-150">Ange det här alternativet om du vill skapa en virtuell dator från en specialiserad disk.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="d3c6b-151">Ange inte parametern *SourceImageUri* när du anger det här alternativet.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="d3c6b-152">*VhdUri* är allt som behövs för att det ska bli så att Azure Platform anger platsen för den virtuella hård disken (VHD) som ska kopplas till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="d3c6b-153">Tomt.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-153">Empty.</span></span>
<span data-ttu-id="d3c6b-154">Ange detta för att skapa en tom data disk.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="d3c6b-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-155">FromImage.</span></span>
<span data-ttu-id="d3c6b-156">Ange det här alternativet om du vill skapa en virtuell dator från en allmän bild eller disk.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="d3c6b-157">När du anger det här alternativet måste du ange parametern *SourceImageUri* även för att berätta för Azure Platform platsen för den virtuella hård disk som ska bifogas som en data skiva.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="d3c6b-158">Parametern *VhdUri* används som den plats där data diskens VHD lagras när den används av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c6b-159">-DefaultProfile</span></span>
<span data-ttu-id="d3c6b-160">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-161">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="d3c6b-161">-DiskSizeInGB</span></span>
<span data-ttu-id="d3c6b-162">Anger storleken i GB på en tom disk som ska kopplas till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-162">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-163">-LUN</span><span class="sxs-lookup"><span data-stu-id="d3c6b-163">-Lun</span></span>
<span data-ttu-id="d3c6b-164">Anger LUN (Logical Unit Number) för en data disk.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-164">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-165">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="d3c6b-165">-ManagedDiskId</span></span>
<span data-ttu-id="d3c6b-166">Anger ID för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-166">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-167">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3c6b-167">-Name</span></span>
<span data-ttu-id="d3c6b-168">Anger namnet på den datadisk som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-168">Specifies the name of the data disk to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-169">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="d3c6b-169">-SourceImageUri</span></span>
<span data-ttu-id="d3c6b-170">Anger källans URI för disken som cmdleten kopplas till.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-170">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-171">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d3c6b-171">-StorageAccountType</span></span>
<span data-ttu-id="d3c6b-172">Anger lagrings konto typen för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-172">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-173">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="d3c6b-173">-VhdUri</span></span>
<span data-ttu-id="d3c6b-174">Anger URI (Uniform Resource Identifier) för den virtuella hård disk (VHD)-filen som ska skapas när en plattforms bild eller användar bild används.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-174">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="d3c6b-175">Denna cmdlet kopierar det binära Large Object (BLOB) till den här platsen.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-175">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="d3c6b-176">Det här är den plats där den virtuella datorn startas.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-176">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-177">-VM</span><span class="sxs-lookup"><span data-stu-id="d3c6b-177">-VM</span></span>
<span data-ttu-id="d3c6b-178">Anger det lokala virtuella dator objekt där en data disk ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-178">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="d3c6b-179">Du kan använda cmdleten **Get-AzVM** för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-179">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="d3c6b-180">Du kan använda cmdleten **New-AzVMConfig** för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-180">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-181">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d3c6b-181">-WriteAccelerator</span></span>
<span data-ttu-id="d3c6b-182">Anger om WriteAccelerator ska aktive ras eller inaktive ras på data disken.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-182">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c6b-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c6b-183">CommonParameters</span></span>
<span data-ttu-id="d3c6b-184">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3c6b-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c6b-185">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c6b-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c6b-186">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3c6b-186">INPUTS</span></span>

### <span data-ttu-id="d3c6b-187">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d3c6b-187">PSVirtualMachine</span></span>
<span data-ttu-id="d3c6b-188">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d3c6b-188">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d3c6b-189">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3c6b-189">OUTPUTS</span></span>

### <span data-ttu-id="d3c6b-190">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d3c6b-190">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d3c6b-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3c6b-191">NOTES</span></span>

## <span data-ttu-id="d3c6b-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3c6b-192">RELATED LINKS</span></span>

[<span data-ttu-id="d3c6b-193">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d3c6b-193">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="d3c6b-194">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d3c6b-194">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d3c6b-195">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d3c6b-195">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
