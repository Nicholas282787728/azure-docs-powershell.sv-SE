---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmosdisk
schema: 2.0.0
ms.openlocfilehash: 8185b1072a6964941a4c6c837806d2df13f1cf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929453"
---
# <span data-ttu-id="2f0ae-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="2f0ae-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="2f0ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0ae-103">Anger operativ systemets disk egenskaper på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f0ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f0ae-104">SYNTAX</span></span>

### <span data-ttu-id="2f0ae-105">DefaultParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2f0ae-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f0ae-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="2f0ae-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f0ae-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f0ae-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f0ae-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="2f0ae-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f0ae-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f0ae-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f0ae-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f0ae-110">DESCRIPTION</span></span>
<span data-ttu-id="2f0ae-111">Cmdleten **set-AzureRmVMOSDisk** anger operativ systemets disk egenskaper på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="2f0ae-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f0ae-112">EXAMPLES</span></span>

### <span data-ttu-id="2f0ae-113">Exempel 1: Ange egenskaper på en virtuell dator från Platform image</span><span class="sxs-lookup"><span data-stu-id="2f0ae-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="2f0ae-114">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet13 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="2f0ae-115">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2f0ae-116">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2f0ae-117">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="2f0ae-118">Med kommandot slut anges egenskaperna på den virtuella datorn i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="2f0ae-119">Exempel 2: anger egenskaper på en virtuell dator från den allmänna användar bilden</span><span class="sxs-lookup"><span data-stu-id="2f0ae-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="2f0ae-120">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet13 i resurs gruppen som heter ResourceGroup11 och lagrar objektet i $AvailabilitySet variabeln.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="2f0ae-121">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2f0ae-122">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2f0ae-123">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="2f0ae-124">Med kommandot slut anges egenskaperna på den virtuella datorn i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="2f0ae-125">Exempel 3: anger egenskaper på en virtuell dator från specialiserad användar bild</span><span class="sxs-lookup"><span data-stu-id="2f0ae-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="2f0ae-126">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet13 i resurs gruppen som heter ResourceGroup11 och lagrar objektet i $AvailabilitySet variabeln.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="2f0ae-127">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det i $VirtualMachine variabeln.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2f0ae-128">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2f0ae-129">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="2f0ae-130">Med kommandot slut anges egenskaperna på den virtuella datorn i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="2f0ae-131">Exempel 4: Ange disk krypterings inställningar på en virtuell dators operativ system disk</span><span class="sxs-lookup"><span data-stu-id="2f0ae-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="2f0ae-132">I det här exemplet anges disk krypterings inställningar på en virtuell dators hård disk.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="2f0ae-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f0ae-133">PARAMETERS</span></span>

### <span data-ttu-id="2f0ae-134">-Cachning</span><span class="sxs-lookup"><span data-stu-id="2f0ae-134">-Caching</span></span>
<span data-ttu-id="2f0ae-135">Anger operativ system diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="2f0ae-136">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="2f0ae-136">Valid values are:</span></span> 

- <span data-ttu-id="2f0ae-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2f0ae-137">ReadOnly</span></span>
- <span data-ttu-id="2f0ae-138">Läs</span><span class="sxs-lookup"><span data-stu-id="2f0ae-138">ReadWrite</span></span>

<span data-ttu-id="2f0ae-139">Standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="2f0ae-140">Om du ändrar värdet för cachelagring kan den virtuella datorn startas om.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="2f0ae-141">Den här inställningen påverkar diskens prestanda.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-141">This setting affects the performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-142">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="2f0ae-142">-CreateOption</span></span>
<span data-ttu-id="2f0ae-143">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller en användar bild, eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="2f0ae-144">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="2f0ae-144">Valid values are:</span></span> 

- <span data-ttu-id="2f0ae-145">Anteckning.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-145">Attach.</span></span>
<span data-ttu-id="2f0ae-146">Ange det här alternativet om du vill skapa en virtuell dator från en specialiserad disk.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="2f0ae-147">Ange inte parametern *SourceImageUri* när du anger det här alternativet.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="2f0ae-148">Använd istället Set-AzureRmVMSourceImage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-148">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="2f0ae-149">Du måste också använda parametrarna *Windows* eller *Linux* för att ange vilken typ av operativ system som används på VHD: n för azure2.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="2f0ae-150">Parametern *VhdUri* räcker för att berätta för azure2-plattformen platsen för den disk som ska bifogas.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="2f0ae-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-151">FromImage.</span></span>
<span data-ttu-id="2f0ae-152">Ange det här alternativet om du vill skapa en virtuell dator från en plattforms bild eller en generaliserad användar bild.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="2f0ae-153">Om det är en generaliserad användar bild måste du också ange parametern *SourceImageUri* och parametrarna *Windows* eller *Linux* för att berätta för Azure Platform platsen och typen av operativ system diskens VHD i stället för att använda cmdleten **set-AzureRmVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="2f0ae-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="2f0ae-154">Om det rör sig om en plattforms bild är *VhdUri* -parametern tillräckligt.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="2f0ae-155">Tomt.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0ae-156">-DefaultProfile</span></span>
<span data-ttu-id="2f0ae-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f0ae-158">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="2f0ae-158">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="2f0ae-159">Anger platsen för disk krypterings tangenten.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-159">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-160">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2f0ae-160">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="2f0ae-161">Anger resurs-ID för det huvud valv som innehåller disk krypterings knappen.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-161">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="2f0ae-162">-DiskSizeInGB</span></span>
<span data-ttu-id="2f0ae-163">Anger storleken i GB på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-163">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-164">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="2f0ae-164">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="2f0ae-165">Anger platsen för Key Encryption Key.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-165">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-166">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2f0ae-166">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="2f0ae-167">Anger resurs-ID för det huvud valv som innehåller Key Encryption.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-167">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="2f0ae-168">-Linux</span></span>
<span data-ttu-id="2f0ae-169">Anger att operativ systemet på användar bilden är Linux.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-169">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="2f0ae-170">Ange den här parametern för installation av en användar bild baserad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-170">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-171">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="2f0ae-171">-ManagedDiskId</span></span>
<span data-ttu-id="2f0ae-172">Anger ID för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-172">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-173">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f0ae-173">-Name</span></span>
<span data-ttu-id="2f0ae-174">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-174">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-175">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="2f0ae-175">-SourceImageUri</span></span>
<span data-ttu-id="2f0ae-176">Anger URI för VHD för användar avbildnings scenarier.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-176">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2f0ae-177">-StorageAccountType</span></span>
<span data-ttu-id="2f0ae-178">Anger lagrings konto typen för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-178">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-179">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="2f0ae-179">-VhdUri</span></span>
<span data-ttu-id="2f0ae-180">Anger URI (Uniform Resource Identifier) för en virtuell hård disk (VHD).</span><span class="sxs-lookup"><span data-stu-id="2f0ae-180">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="2f0ae-181">För en bildbaserad virtuell dator anger den här parametern den VHD-fil som ska skapas när en plattforms bild eller användar bild anges.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-181">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="2f0ae-182">Det här är den plats där den binära Large Object (BLOB) kopieras för att starta den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-182">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="2f0ae-183">För ett diskbaserade start scenario anger den här parametern den VHD-fil som den virtuella datorn använder direkt för att starta.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-183">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-184">-VM</span><span class="sxs-lookup"><span data-stu-id="2f0ae-184">-VM</span></span>
<span data-ttu-id="2f0ae-185">Anger det lokala virtuella dator objekt som du kan ange disk egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-185">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="2f0ae-186">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-186">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-187">-Windows</span><span class="sxs-lookup"><span data-stu-id="2f0ae-187">-Windows</span></span>
<span data-ttu-id="2f0ae-188">Anger att operativ systemet på användarens bild är Windows.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-188">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0ae-189">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="2f0ae-189">-WriteAccelerator</span></span>
<span data-ttu-id="2f0ae-190">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="2f0ae-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0ae-191">CommonParameters</span></span>
<span data-ttu-id="2f0ae-192">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0ae-193">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f0ae-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0ae-194">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f0ae-194">INPUTS</span></span>

### <span data-ttu-id="2f0ae-195">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2f0ae-195">PSVirtualMachine</span></span>
<span data-ttu-id="2f0ae-196">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2f0ae-196">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="2f0ae-197">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f0ae-197">OUTPUTS</span></span>

### <span data-ttu-id="2f0ae-198">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2f0ae-198">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2f0ae-199">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f0ae-199">NOTES</span></span>

## <span data-ttu-id="2f0ae-200">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f0ae-200">RELATED LINKS</span></span>

[<span data-ttu-id="2f0ae-201">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2f0ae-201">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="2f0ae-202">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2f0ae-202">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="2f0ae-203">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="2f0ae-203">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


