---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092334"
---
# <span data-ttu-id="d1b19-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d1b19-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="d1b19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1b19-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b19-103">Anger lagrings profil egenskaper för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d1b19-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="d1b19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1b19-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1b19-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1b19-105">DESCRIPTION</span></span>
<span data-ttu-id="d1b19-106">Cmdleten **set-AzVmssStorageProfile** anger lagrings profil egenskaperna för den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d1b19-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d1b19-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1b19-107">EXAMPLES</span></span>

### <span data-ttu-id="d1b19-108">Exempel 1: Ange lagrings profil egenskaper för VMSS</span><span class="sxs-lookup"><span data-stu-id="d1b19-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="d1b19-109">Det här kommandot anger lagrings profil egenskaperna för VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="d1b19-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="d1b19-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1b19-110">PARAMETERS</span></span>

### <span data-ttu-id="d1b19-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="d1b19-111">-DataDisk</span></span>
<span data-ttu-id="d1b19-112">Anger data diskens objekt.</span><span class="sxs-lookup"><span data-stu-id="d1b19-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="d1b19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b19-113">-DefaultProfile</span></span>
<span data-ttu-id="d1b19-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b19-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1b19-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="d1b19-115">-DiffDiskSetting</span></span>
<span data-ttu-id="d1b19-116">Anger differentiering disk inställningar för operativ system disk.</span><span class="sxs-lookup"><span data-stu-id="d1b19-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="d1b19-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="d1b19-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="d1b19-118">Anger resurs-ID för kund hanterad disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="d1b19-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="d1b19-119">Detta kan endast anges för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="d1b19-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="d1b19-120">-Image</span><span class="sxs-lookup"><span data-stu-id="d1b19-120">-Image</span></span>
<span data-ttu-id="d1b19-121">Anger BLOB URI för användar avbildningen.</span><span class="sxs-lookup"><span data-stu-id="d1b19-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="d1b19-122">VMSS skapar en operativ Systems disk i samma behållare som användar bilden.</span><span class="sxs-lookup"><span data-stu-id="d1b19-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="d1b19-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="d1b19-123">-ImageReferenceId</span></span>
<span data-ttu-id="d1b19-124">Anger bild referens-ID.</span><span class="sxs-lookup"><span data-stu-id="d1b19-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="d1b19-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="d1b19-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="d1b19-126">Anger typen av virtuell dator avbildning (VMImage).</span><span class="sxs-lookup"><span data-stu-id="d1b19-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="d1b19-127">För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="d1b19-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="d1b19-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="d1b19-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="d1b19-129">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="d1b19-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="d1b19-130">Använd Get-AzVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="d1b19-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="d1b19-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="d1b19-131">-ImageReferenceSku</span></span>
<span data-ttu-id="d1b19-132">Anger VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="d1b19-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="d1b19-133">För att få SKU: er, Använd Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1b19-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="d1b19-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="d1b19-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="d1b19-135">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="d1b19-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="d1b19-136">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="d1b19-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="d1b19-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="d1b19-137">-ManagedDisk</span></span>
<span data-ttu-id="d1b19-138">Anger den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="d1b19-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="d1b19-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="d1b19-139">-OsDiskCaching</span></span>
<span data-ttu-id="d1b19-140">Anger operativ system diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="d1b19-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="d1b19-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d1b19-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d1b19-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d1b19-142">ReadOnly</span></span>
- <span data-ttu-id="d1b19-143">ReadWrite standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="d1b19-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="d1b19-144">Om du ändrar värdet för cachelagring startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="d1b19-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="d1b19-145">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="d1b19-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="d1b19-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="d1b19-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="d1b19-147">Anger hur den här cmdleten skapar de VMSS virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="d1b19-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="d1b19-148">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d1b19-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d1b19-149">Bifoga: det här värdet används när du använder en specialiserad disk för att skapa den VMSS virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d1b19-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="d1b19-150">FromImage: det här värdet används när du använder en bild för att skapa den virtuella VMSS-datorn.</span><span class="sxs-lookup"><span data-stu-id="d1b19-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="d1b19-151">Om du använder en plattforms bild kan du även använda parametern *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="d1b19-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="d1b19-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="d1b19-152">-OsDiskName</span></span>
<span data-ttu-id="d1b19-153">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="d1b19-153">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="d1b19-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="d1b19-154">-OsDiskOsType</span></span>
<span data-ttu-id="d1b19-155">Anger operativ systemet på disken.</span><span class="sxs-lookup"><span data-stu-id="d1b19-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="d1b19-156">Detta krävs endast för användar bild scenarier och inte för en plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="d1b19-156">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="d1b19-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d1b19-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="d1b19-158">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="d1b19-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="d1b19-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="d1b19-159">-VhdContainer</span></span>
<span data-ttu-id="d1b19-160">Anger de URL-adresser som används för att lagra operativ system diskar för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d1b19-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="d1b19-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d1b19-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d1b19-162">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="d1b19-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="d1b19-163">Använd New-AzVmssConfig-objektet för att få ett objekt.</span><span class="sxs-lookup"><span data-stu-id="d1b19-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="d1b19-164">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d1b19-164">-Confirm</span></span>
<span data-ttu-id="d1b19-165">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d1b19-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1b19-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1b19-166">-WhatIf</span></span>
<span data-ttu-id="d1b19-167">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d1b19-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1b19-168">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d1b19-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1b19-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b19-169">CommonParameters</span></span>
<span data-ttu-id="d1b19-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1b19-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b19-171">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1b19-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b19-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1b19-172">INPUTS</span></span>

### <span data-ttu-id="d1b19-173">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d1b19-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d1b19-174">System. String</span><span class="sxs-lookup"><span data-stu-id="d1b19-174">System.String</span></span>

### <span data-ttu-id="d1b19-175">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d1b19-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d1b19-176">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d1b19-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d1b19-177">System. string []</span><span class="sxs-lookup"><span data-stu-id="d1b19-177">System.String[]</span></span>

### <span data-ttu-id="d1b19-178">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="d1b19-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="d1b19-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1b19-179">OUTPUTS</span></span>

### <span data-ttu-id="d1b19-180">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d1b19-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d1b19-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1b19-181">NOTES</span></span>

## <span data-ttu-id="d1b19-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1b19-182">RELATED LINKS</span></span>

[<span data-ttu-id="d1b19-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d1b19-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="d1b19-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d1b19-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="d1b19-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d1b19-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="d1b19-186">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d1b19-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


