---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 26f61261bd8fd1c2d5fc2bbdacec71f73db91fb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579576"
---
# <span data-ttu-id="10fd1-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="10fd1-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="10fd1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="10fd1-103">Anger lagrings profil egenskaper för VMSS.</span><span class="sxs-lookup"><span data-stu-id="10fd1-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10fd1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10fd1-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [-OsDiskName <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10fd1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10fd1-105">DESCRIPTION</span></span>
<span data-ttu-id="10fd1-106">Cmdleten **set-AzureRmVmssStorageProfile** anger lagrings profil egenskaperna för den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="10fd1-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="10fd1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10fd1-107">EXAMPLES</span></span>

### <span data-ttu-id="10fd1-108">Exempel 1: Ange lagrings profil egenskaper för VMSS</span><span class="sxs-lookup"><span data-stu-id="10fd1-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="10fd1-109">Det här kommandot anger lagrings profil egenskaperna för VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="10fd1-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="10fd1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10fd1-110">PARAMETERS</span></span>

### <span data-ttu-id="10fd1-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="10fd1-111">-DataDisk</span></span>
<span data-ttu-id="10fd1-112">Anger data diskens objekt.</span><span class="sxs-lookup"><span data-stu-id="10fd1-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="10fd1-113">-Image</span><span class="sxs-lookup"><span data-stu-id="10fd1-113">-Image</span></span>
<span data-ttu-id="10fd1-114">Anger BLOB URI för användar avbildningen.</span><span class="sxs-lookup"><span data-stu-id="10fd1-114">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="10fd1-115">VMSS skapar en operativ Systems disk i samma behållare som användar bilden.</span><span class="sxs-lookup"><span data-stu-id="10fd1-115">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="10fd1-116">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="10fd1-116">-ImageReferenceId</span></span>
<span data-ttu-id="10fd1-117">Anger bild referens-ID.</span><span class="sxs-lookup"><span data-stu-id="10fd1-117">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="10fd1-118">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="10fd1-118">-ImageReferenceOffer</span></span>
<span data-ttu-id="10fd1-119">Anger typen av virtuell dator avbildning (VMImage).</span><span class="sxs-lookup"><span data-stu-id="10fd1-119">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="10fd1-120">För att få ett bild utbud, Använd cmdleten Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="10fd1-120">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="10fd1-121">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="10fd1-121">-ImageReferencePublisher</span></span>
<span data-ttu-id="10fd1-122">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="10fd1-122">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="10fd1-123">Använd Get-AzureRmVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="10fd1-123">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="10fd1-124">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="10fd1-124">-ImageReferenceSku</span></span>
<span data-ttu-id="10fd1-125">Anger VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="10fd1-125">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="10fd1-126">För att få SKU: er, Använd Get-AzureRmVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10fd1-126">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="10fd1-127">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="10fd1-127">-ImageReferenceVersion</span></span>
<span data-ttu-id="10fd1-128">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="10fd1-128">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="10fd1-129">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="10fd1-129">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="10fd1-130">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="10fd1-130">-ManagedDisk</span></span>
<span data-ttu-id="10fd1-131">Anger den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="10fd1-131">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="10fd1-132">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="10fd1-132">-OsDiskCaching</span></span>
<span data-ttu-id="10fd1-133">Anger operativ system diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="10fd1-133">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="10fd1-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="10fd1-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10fd1-135">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="10fd1-135">ReadOnly</span></span>
- <span data-ttu-id="10fd1-136">Läs</span><span class="sxs-lookup"><span data-stu-id="10fd1-136">ReadWrite</span></span>

<span data-ttu-id="10fd1-137">Standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="10fd1-137">The default value is ReadWrite.</span></span>
<span data-ttu-id="10fd1-138">Om du ändrar värdet för cachelagring startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="10fd1-138">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="10fd1-139">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="10fd1-139">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="10fd1-140">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="10fd1-140">-OsDiskCreateOption</span></span>
<span data-ttu-id="10fd1-141">Anger hur den här cmdleten skapar de VMSS virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="10fd1-141">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="10fd1-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="10fd1-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10fd1-143">Bifoga: det här värdet används när du använder en specialiserad disk för att skapa den VMSS virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="10fd1-143">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="10fd1-144">FromImage: det här värdet används när du använder en bild för att skapa den virtuella VMSS-datorn.</span><span class="sxs-lookup"><span data-stu-id="10fd1-144">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="10fd1-145">Om du använder en plattforms bild kan du även använda parametern *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="10fd1-145">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="10fd1-146">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="10fd1-146">-OsDiskName</span></span>
<span data-ttu-id="10fd1-147">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="10fd1-147">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd1-148">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="10fd1-148">-OsDiskOsType</span></span>
<span data-ttu-id="10fd1-149">Anger operativ systemet på disken.</span><span class="sxs-lookup"><span data-stu-id="10fd1-149">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="10fd1-150">Detta krävs endast för användar bild scenarier och inte för en plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="10fd1-150">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="10fd1-151">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="10fd1-151">-VhdContainer</span></span>
<span data-ttu-id="10fd1-152">Anger de URL-adresser som används för att lagra operativ system diskar för VMSS.</span><span class="sxs-lookup"><span data-stu-id="10fd1-152">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="10fd1-153">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="10fd1-153">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="10fd1-154">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="10fd1-154">Specifies the VMSS object.</span></span>
<span data-ttu-id="10fd1-155">Använd New-AzureRmVmssConfig-objektet för att få ett objekt.</span><span class="sxs-lookup"><span data-stu-id="10fd1-155">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd1-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10fd1-156">-Confirm</span></span>
<span data-ttu-id="10fd1-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10fd1-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10fd1-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10fd1-158">-WhatIf</span></span>
<span data-ttu-id="10fd1-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10fd1-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10fd1-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10fd1-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10fd1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10fd1-161">CommonParameters</span></span>
<span data-ttu-id="10fd1-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10fd1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10fd1-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10fd1-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10fd1-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10fd1-164">INPUTS</span></span>

###  
<span data-ttu-id="10fd1-165">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="10fd1-165">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="10fd1-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10fd1-166">OUTPUTS</span></span>

## <span data-ttu-id="10fd1-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10fd1-167">NOTES</span></span>

## <span data-ttu-id="10fd1-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10fd1-168">RELATED LINKS</span></span>

[<span data-ttu-id="10fd1-169">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="10fd1-169">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="10fd1-170">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="10fd1-170">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="10fd1-171">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="10fd1-171">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="10fd1-172">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="10fd1-172">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


