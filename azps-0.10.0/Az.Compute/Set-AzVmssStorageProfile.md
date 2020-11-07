---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: d19c039a5038c9327ea35a4f0b385e5472b748a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924750"
---
# <span data-ttu-id="a3bb5-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="a3bb5-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="a3bb5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="a3bb5-103">Anger lagrings profil egenskaper för VMSS.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="a3bb5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3bb5-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-ManagedDisk <StorageAccountTypes>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3bb5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3bb5-105">DESCRIPTION</span></span>
<span data-ttu-id="a3bb5-106">Cmdleten **set-AzVmssStorageProfile** anger lagrings profil egenskaperna för den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a3bb5-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a3bb5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3bb5-107">EXAMPLES</span></span>

### <span data-ttu-id="a3bb5-108">Exempel 1: Ange lagrings profil egenskaper för VMSS</span><span class="sxs-lookup"><span data-stu-id="a3bb5-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="a3bb5-109">Det här kommandot anger lagrings profil egenskaperna för VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="a3bb5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3bb5-110">PARAMETERS</span></span>

### <span data-ttu-id="a3bb5-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="a3bb5-111">-DataDisk</span></span>
<span data-ttu-id="a3bb5-112">Anger data diskens objekt.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-112">Specifies the data disk object.</span></span>

```yaml
Type: VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3bb5-113">-DefaultProfile</span></span>
<span data-ttu-id="a3bb5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3bb5-115">-Image</span><span class="sxs-lookup"><span data-stu-id="a3bb5-115">-Image</span></span>
<span data-ttu-id="a3bb5-116">Anger BLOB URI för användar avbildningen.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="a3bb5-117">VMSS skapar en operativ Systems disk i samma behållare som användar bilden.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="a3bb5-118">-ImageReferenceId</span></span>
<span data-ttu-id="a3bb5-119">Anger bild referens-ID.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-119">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="a3bb5-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="a3bb5-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="a3bb5-121">Anger typen av virtuell dator avbildning (VMImage).</span><span class="sxs-lookup"><span data-stu-id="a3bb5-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="a3bb5-122">För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-122">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="a3bb5-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="a3bb5-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="a3bb5-124">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="a3bb5-125">Använd Get-AzVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-125">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="a3bb5-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="a3bb5-126">-ImageReferenceSku</span></span>
<span data-ttu-id="a3bb5-127">Anger VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="a3bb5-128">För att få SKU: er, Använd Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-128">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="a3bb5-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="a3bb5-130">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="a3bb5-131">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a3bb5-132">-ManagedDisk</span></span>
<span data-ttu-id="a3bb5-133">Anger den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-133">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="a3bb5-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="a3bb5-134">-OsDiskCaching</span></span>
<span data-ttu-id="a3bb5-135">Anger operativ system diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="a3bb5-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a3bb5-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a3bb5-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a3bb5-137">ReadOnly</span></span>
- <span data-ttu-id="a3bb5-138">Läs</span><span class="sxs-lookup"><span data-stu-id="a3bb5-138">ReadWrite</span></span>

<span data-ttu-id="a3bb5-139">Standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="a3bb5-140">Om du ändrar värdet för cachelagring startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="a3bb5-141">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-141">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="a3bb5-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="a3bb5-143">Anger hur den här cmdleten skapar de VMSS virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="a3bb5-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a3bb5-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a3bb5-145">Bifoga: det här värdet används när du använder en specialiserad disk för att skapa den VMSS virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="a3bb5-146">FromImage: det här värdet används när du använder en bild för att skapa den virtuella VMSS-datorn.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="a3bb5-147">Om du använder en plattforms bild kan du även använda parametern *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="a3bb5-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="a3bb5-148">-OsDiskName</span></span>
<span data-ttu-id="a3bb5-149">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-149">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="a3bb5-150">-OsDiskOsType</span></span>
<span data-ttu-id="a3bb5-151">Anger operativ systemet på disken.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="a3bb5-152">Detta krävs endast för användar bild scenarier och inte för en plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-152">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-153">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="a3bb5-153">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="a3bb5-154">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-154">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="a3bb5-155">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="a3bb5-155">-VhdContainer</span></span>
<span data-ttu-id="a3bb5-156">Anger de URL-adresser som används för att lagra operativ system diskar för VMSS.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-156">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-157">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a3bb5-157">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a3bb5-158">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-158">Specifies the VMSS object.</span></span>
<span data-ttu-id="a3bb5-159">Använd New-AzVmssConfig-objektet för att få ett objekt.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-159">To obtain the object, use the New-AzVmssConfig object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3bb5-160">-Confirm</span></span>
<span data-ttu-id="a3bb5-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3bb5-162">-WhatIf</span></span>
<span data-ttu-id="a3bb5-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3bb5-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-164">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3bb5-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3bb5-165">CommonParameters</span></span>
<span data-ttu-id="a3bb5-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3bb5-167">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3bb5-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3bb5-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3bb5-168">INPUTS</span></span>

###  
<span data-ttu-id="a3bb5-169">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a3bb5-169">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a3bb5-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3bb5-170">OUTPUTS</span></span>

### <span data-ttu-id="a3bb5-171">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a3bb5-171">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a3bb5-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3bb5-172">NOTES</span></span>

## <span data-ttu-id="a3bb5-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3bb5-173">RELATED LINKS</span></span>

[<span data-ttu-id="a3bb5-174">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a3bb5-174">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="a3bb5-175">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a3bb5-175">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a3bb5-176">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a3bb5-176">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="a3bb5-177">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a3bb5-177">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


