---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 44156d29d352adb83fe10fa898af2f655bfd4456
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754446"
---
# <span data-ttu-id="d0663-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d0663-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="d0663-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0663-102">SYNOPSIS</span></span>
<span data-ttu-id="d0663-103">Anger lagrings profil egenskaper för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d0663-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="d0663-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0663-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0663-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0663-105">DESCRIPTION</span></span>
<span data-ttu-id="d0663-106">Cmdleten **set-AzVmssStorageProfile** anger lagrings profil egenskaperna för den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d0663-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d0663-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0663-107">EXAMPLES</span></span>

### <span data-ttu-id="d0663-108">Exempel 1: Ange lagrings profil egenskaper för VMSS</span><span class="sxs-lookup"><span data-stu-id="d0663-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="d0663-109">Det här kommandot anger lagrings profil egenskaperna för VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="d0663-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="d0663-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0663-110">PARAMETERS</span></span>

### <span data-ttu-id="d0663-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="d0663-111">-DataDisk</span></span>
<span data-ttu-id="d0663-112">Anger data diskens objekt.</span><span class="sxs-lookup"><span data-stu-id="d0663-112">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0663-113">-DefaultProfile</span></span>
<span data-ttu-id="d0663-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0663-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0663-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="d0663-115">-DiffDiskSetting</span></span>
<span data-ttu-id="d0663-116">Anger differentiering disk inställningar för operativ system disk.</span><span class="sxs-lookup"><span data-stu-id="d0663-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="d0663-117">-Image</span><span class="sxs-lookup"><span data-stu-id="d0663-117">-Image</span></span>
<span data-ttu-id="d0663-118">Anger BLOB URI för användar avbildningen.</span><span class="sxs-lookup"><span data-stu-id="d0663-118">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="d0663-119">VMSS skapar en operativ Systems disk i samma behållare som användar bilden.</span><span class="sxs-lookup"><span data-stu-id="d0663-119">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-120">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="d0663-120">-ImageReferenceId</span></span>
<span data-ttu-id="d0663-121">Anger bild referens-ID.</span><span class="sxs-lookup"><span data-stu-id="d0663-121">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="d0663-122">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="d0663-122">-ImageReferenceOffer</span></span>
<span data-ttu-id="d0663-123">Anger typen av virtuell dator avbildning (VMImage).</span><span class="sxs-lookup"><span data-stu-id="d0663-123">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="d0663-124">För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="d0663-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-125">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="d0663-125">-ImageReferencePublisher</span></span>
<span data-ttu-id="d0663-126">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="d0663-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="d0663-127">Använd Get-AzVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="d0663-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="d0663-128">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="d0663-128">-ImageReferenceSku</span></span>
<span data-ttu-id="d0663-129">Anger VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="d0663-129">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="d0663-130">För att få SKU: er, Använd Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0663-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-131">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="d0663-131">-ImageReferenceVersion</span></span>
<span data-ttu-id="d0663-132">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="d0663-132">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="d0663-133">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="d0663-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-134">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="d0663-134">-ManagedDisk</span></span>
<span data-ttu-id="d0663-135">Anger den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="d0663-135">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="d0663-136">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="d0663-136">-OsDiskCaching</span></span>
<span data-ttu-id="d0663-137">Anger operativ system diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="d0663-137">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="d0663-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d0663-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d0663-139">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d0663-139">ReadOnly</span></span>
- <span data-ttu-id="d0663-140">ReadWrite standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="d0663-140">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="d0663-141">Om du ändrar värdet för cachelagring startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="d0663-141">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="d0663-142">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="d0663-142">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-143">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="d0663-143">-OsDiskCreateOption</span></span>
<span data-ttu-id="d0663-144">Anger hur den här cmdleten skapar de VMSS virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="d0663-144">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="d0663-145">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d0663-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d0663-146">Bifoga: det här värdet används när du använder en specialiserad disk för att skapa den VMSS virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d0663-146">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="d0663-147">FromImage: det här värdet används när du använder en bild för att skapa den virtuella VMSS-datorn.</span><span class="sxs-lookup"><span data-stu-id="d0663-147">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="d0663-148">Om du använder en plattforms bild kan du även använda parametern *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="d0663-148">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-149">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="d0663-149">-OsDiskName</span></span>
<span data-ttu-id="d0663-150">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="d0663-150">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-151">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="d0663-151">-OsDiskOsType</span></span>
<span data-ttu-id="d0663-152">Anger operativ systemet på disken.</span><span class="sxs-lookup"><span data-stu-id="d0663-152">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="d0663-153">Detta krävs endast för användar bild scenarier och inte för en plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="d0663-153">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-154">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d0663-154">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="d0663-155">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="d0663-155">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="d0663-156">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="d0663-156">-VhdContainer</span></span>
<span data-ttu-id="d0663-157">Anger de URL-adresser som används för att lagra operativ system diskar för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d0663-157">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-158">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d0663-158">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d0663-159">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="d0663-159">Specifies the VMSS object.</span></span>
<span data-ttu-id="d0663-160">Använd New-AzVmssConfig-objektet för att få ett objekt.</span><span class="sxs-lookup"><span data-stu-id="d0663-160">To obtain the object, use the New-AzVmssConfig object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0663-161">-Confirm</span></span>
<span data-ttu-id="d0663-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0663-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0663-163">-WhatIf</span></span>
<span data-ttu-id="d0663-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0663-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0663-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0663-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0663-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0663-166">CommonParameters</span></span>
<span data-ttu-id="d0663-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0663-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0663-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0663-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0663-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0663-169">INPUTS</span></span>

### <span data-ttu-id="d0663-170">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d0663-170">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d0663-171">System. String</span><span class="sxs-lookup"><span data-stu-id="d0663-171">System.String</span></span>

### <span data-ttu-id="d0663-172">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d0663-172">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d0663-173">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d0663-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d0663-174">System. string []</span><span class="sxs-lookup"><span data-stu-id="d0663-174">System.String[]</span></span>

### <span data-ttu-id="d0663-175">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="d0663-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="d0663-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0663-176">OUTPUTS</span></span>

### <span data-ttu-id="d0663-177">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d0663-177">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d0663-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0663-178">NOTES</span></span>

## <span data-ttu-id="d0663-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0663-179">RELATED LINKS</span></span>

[<span data-ttu-id="d0663-180">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d0663-180">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="d0663-181">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d0663-181">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="d0663-182">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d0663-182">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="d0663-183">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d0663-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

