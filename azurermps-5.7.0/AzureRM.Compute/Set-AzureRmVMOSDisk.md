---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
ms.openlocfilehash: dfcd408e3afa7988b06a1e020d76844c48d990b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574336"
---
# <span data-ttu-id="f1f05-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="f1f05-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="f1f05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1f05-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f05-103">Anger operativ systemets disk egenskaper på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f1f05-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1f05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1f05-104">SYNTAX</span></span>

### <span data-ttu-id="f1f05-105">DefaultParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f1f05-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes>
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1f05-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="f1f05-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1f05-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1f05-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

### <span data-ttu-id="f1f05-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="f1f05-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1f05-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1f05-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

## <span data-ttu-id="f1f05-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1f05-110">DESCRIPTION</span></span>
<span data-ttu-id="f1f05-111">Cmdleten **set-AzureRmVMOSDisk** anger operativ systemets disk egenskaper på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f1f05-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="f1f05-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1f05-112">EXAMPLES</span></span>

### <span data-ttu-id="f1f05-113">Exempel 1: Ange egenskaper på en virtuell dator från Platform image</span><span class="sxs-lookup"><span data-stu-id="f1f05-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="f1f05-114">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet13 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="f1f05-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="f1f05-115">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="f1f05-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f1f05-116">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="f1f05-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="f1f05-117">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f1f05-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="f1f05-118">Med kommandot slut anges egenskaperna på den virtuella datorn i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f1f05-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="f1f05-119">Exempel 2: anger egenskaper på en virtuell dator från den allmänna användar bilden</span><span class="sxs-lookup"><span data-stu-id="f1f05-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="f1f05-120">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet13 i resurs gruppen som heter ResourceGroup11 och lagrar objektet i $AvailabilitySet variabeln.</span><span class="sxs-lookup"><span data-stu-id="f1f05-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="f1f05-121">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.</span><span class="sxs-lookup"><span data-stu-id="f1f05-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f1f05-122">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="f1f05-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="f1f05-123">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f1f05-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="f1f05-124">Med kommandot slut anges egenskaperna på den virtuella datorn i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f1f05-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="f1f05-125">Exempel 3: anger egenskaper på en virtuell dator från specialiserad användar bild</span><span class="sxs-lookup"><span data-stu-id="f1f05-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="f1f05-126">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet13 i resurs gruppen som heter ResourceGroup11 och lagrar objektet i $AvailabilitySet variabeln.</span><span class="sxs-lookup"><span data-stu-id="f1f05-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="f1f05-127">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.</span><span class="sxs-lookup"><span data-stu-id="f1f05-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f1f05-128">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="f1f05-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="f1f05-129">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f1f05-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="f1f05-130">Med kommandot slut anges egenskaperna på den virtuella datorn i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f1f05-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="f1f05-131">Exempel 4: Ange disk krypterings inställningar på en virtuell dators operativ system disk</span><span class="sxs-lookup"><span data-stu-id="f1f05-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="f1f05-132">I det här exemplet anges disk krypterings inställningar på en virtuell dators hård disk.</span><span class="sxs-lookup"><span data-stu-id="f1f05-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="f1f05-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1f05-133">PARAMETERS</span></span>

### <span data-ttu-id="f1f05-134">-Cachning</span><span class="sxs-lookup"><span data-stu-id="f1f05-134">-Caching</span></span>
<span data-ttu-id="f1f05-135">Anger operativ system diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="f1f05-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="f1f05-136">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="f1f05-136">Valid values are:</span></span> 

- <span data-ttu-id="f1f05-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f1f05-137">ReadOnly</span></span>
- <span data-ttu-id="f1f05-138">Läs</span><span class="sxs-lookup"><span data-stu-id="f1f05-138">ReadWrite</span></span>

<span data-ttu-id="f1f05-139">Standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="f1f05-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="f1f05-140">Om du ändrar värdet för cachelagring kan den virtuella datorn startas om.</span><span class="sxs-lookup"><span data-stu-id="f1f05-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="f1f05-141">Den här inställningen påverkar diskens prestanda.</span><span class="sxs-lookup"><span data-stu-id="f1f05-141">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="f1f05-142">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="f1f05-142">-CreateOption</span></span>
<span data-ttu-id="f1f05-143">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller en användar bild, eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="f1f05-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="f1f05-144">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="f1f05-144">Valid values are:</span></span> 

- <span data-ttu-id="f1f05-145">Anteckning.</span><span class="sxs-lookup"><span data-stu-id="f1f05-145">Attach.</span></span>
<span data-ttu-id="f1f05-146">Ange det här alternativet om du vill skapa en virtuell dator från en specialiserad disk.</span><span class="sxs-lookup"><span data-stu-id="f1f05-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="f1f05-147">Ange inte parametern *SourceImageUri* när du anger det här alternativet.</span><span class="sxs-lookup"><span data-stu-id="f1f05-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="f1f05-148">Använd istället Set-AzureRmVMSourceImage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1f05-148">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="f1f05-149">Du måste också använda parametrarna *Windows* eller *Linux* för att ange vilken typ av operativ system som används på VHD: n för azure2.</span><span class="sxs-lookup"><span data-stu-id="f1f05-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="f1f05-150">Parametern *VhdUri* räcker för att berätta för azure2-plattformen platsen för den disk som ska bifogas.</span><span class="sxs-lookup"><span data-stu-id="f1f05-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="f1f05-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="f1f05-151">FromImage.</span></span>
<span data-ttu-id="f1f05-152">Ange det här alternativet om du vill skapa en virtuell dator från en plattforms bild eller en generaliserad användar bild.</span><span class="sxs-lookup"><span data-stu-id="f1f05-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="f1f05-153">Om det är en generaliserad användar bild måste du också ange parametern *SourceImageUri* och parametrarna *Windows* eller *Linux* för att berätta för Azure Platform platsen och typen av operativ system diskens VHD i stället för att använda cmdleten **set-AzureRmVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="f1f05-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="f1f05-154">Om det rör sig om en plattforms bild är *VhdUri* -parametern tillräckligt.</span><span class="sxs-lookup"><span data-stu-id="f1f05-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="f1f05-155">Tomt.</span><span class="sxs-lookup"><span data-stu-id="f1f05-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-156">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="f1f05-156">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="f1f05-157">Anger platsen för disk krypterings tangenten.</span><span class="sxs-lookup"><span data-stu-id="f1f05-157">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-158">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="f1f05-158">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="f1f05-159">Anger resurs-ID för det huvud valv som innehåller disk krypterings knappen.</span><span class="sxs-lookup"><span data-stu-id="f1f05-159">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-160">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="f1f05-160">-DiskSizeInGB</span></span>
<span data-ttu-id="f1f05-161">Anger storleken i GB på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="f1f05-161">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-162">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="f1f05-162">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="f1f05-163">Anger platsen för Key Encryption Key.</span><span class="sxs-lookup"><span data-stu-id="f1f05-163">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-164">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="f1f05-164">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="f1f05-165">Anger resurs-ID för det huvud valv som innehåller Key Encryption.</span><span class="sxs-lookup"><span data-stu-id="f1f05-165">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="f1f05-166">-Linux</span></span>
<span data-ttu-id="f1f05-167">Anger att operativ systemet på användar bilden är Linux.</span><span class="sxs-lookup"><span data-stu-id="f1f05-167">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="f1f05-168">Ange den här parametern för installation av en användar bild baserad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f1f05-168">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="f1f05-169">-ManagedDiskId</span></span>
<span data-ttu-id="f1f05-170">Anger ID för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="f1f05-170">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-171">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1f05-171">-Name</span></span>
<span data-ttu-id="f1f05-172">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="f1f05-172">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="f1f05-173">-SourceImageUri</span></span>
<span data-ttu-id="f1f05-174">Anger URI för VHD för användar avbildnings scenarier.</span><span class="sxs-lookup"><span data-stu-id="f1f05-174">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f1f05-175">-StorageAccountType</span></span>
<span data-ttu-id="f1f05-176">Anger lagrings konto typen för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="f1f05-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="f1f05-177">-VhdUri</span></span>
<span data-ttu-id="f1f05-178">Anger URI (Uniform Resource Identifier) för en virtuell hård disk (VHD).</span><span class="sxs-lookup"><span data-stu-id="f1f05-178">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="f1f05-179">För en bildbaserad virtuell dator anger den här parametern den VHD-fil som ska skapas när en plattforms bild eller användar bild anges.</span><span class="sxs-lookup"><span data-stu-id="f1f05-179">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="f1f05-180">Det här är den plats där den binära Large Object (BLOB) kopieras för att starta den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f1f05-180">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="f1f05-181">För ett diskbaserade start scenario anger den här parametern den VHD-fil som den virtuella datorn använder direkt för att starta.</span><span class="sxs-lookup"><span data-stu-id="f1f05-181">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-182">-VM</span><span class="sxs-lookup"><span data-stu-id="f1f05-182">-VM</span></span>
<span data-ttu-id="f1f05-183">Anger det lokala virtuella dator objekt som du kan ange disk egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="f1f05-183">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="f1f05-184">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="f1f05-184">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="f1f05-185">-Windows</span><span class="sxs-lookup"><span data-stu-id="f1f05-185">-Windows</span></span>
<span data-ttu-id="f1f05-186">Anger att operativ systemet på användarens bild är Windows.</span><span class="sxs-lookup"><span data-stu-id="f1f05-186">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f05-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f05-187">CommonParameters</span></span>
<span data-ttu-id="f1f05-188">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f05-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f05-189">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f05-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f05-190">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1f05-190">INPUTS</span></span>

### <span data-ttu-id="f1f05-191">Ingen</span><span class="sxs-lookup"><span data-stu-id="f1f05-191">None</span></span>
<span data-ttu-id="f1f05-192">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f1f05-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1f05-193">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1f05-193">OUTPUTS</span></span>

## <span data-ttu-id="f1f05-194">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1f05-194">NOTES</span></span>

## <span data-ttu-id="f1f05-195">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1f05-195">RELATED LINKS</span></span>

[<span data-ttu-id="f1f05-196">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f1f05-196">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="f1f05-197">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f1f05-197">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="f1f05-198">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="f1f05-198">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


