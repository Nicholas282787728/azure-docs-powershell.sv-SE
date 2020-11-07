---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssstorageprofile
schema: 2.0.0
ms.openlocfilehash: c96ff571ef1b82e52a313c2044a41b97d46ffa0b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929941"
---
# <span data-ttu-id="1e30d-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="1e30d-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="1e30d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e30d-102">SYNOPSIS</span></span>
<span data-ttu-id="1e30d-103">Anger lagrings profil egenskaper för VMSS.</span><span class="sxs-lookup"><span data-stu-id="1e30d-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e30d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e30d-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-ManagedDisk <StorageAccountTypes>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e30d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e30d-105">DESCRIPTION</span></span>
<span data-ttu-id="1e30d-106">Cmdleten **set-AzureRmVmssStorageProfile** anger lagrings profil egenskaperna för den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1e30d-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1e30d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e30d-107">EXAMPLES</span></span>

### <span data-ttu-id="1e30d-108">Exempel 1: Ange lagrings profil egenskaper för VMSS</span><span class="sxs-lookup"><span data-stu-id="1e30d-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="1e30d-109">Det här kommandot anger lagrings profil egenskaperna för VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="1e30d-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="1e30d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e30d-110">PARAMETERS</span></span>

### <span data-ttu-id="1e30d-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="1e30d-111">-DataDisk</span></span>
<span data-ttu-id="1e30d-112">Anger data diskens objekt.</span><span class="sxs-lookup"><span data-stu-id="1e30d-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="1e30d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e30d-113">-DefaultProfile</span></span>
<span data-ttu-id="1e30d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e30d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e30d-115">-Image</span><span class="sxs-lookup"><span data-stu-id="1e30d-115">-Image</span></span>
<span data-ttu-id="1e30d-116">Anger BLOB URI för användar avbildningen.</span><span class="sxs-lookup"><span data-stu-id="1e30d-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="1e30d-117">VMSS skapar en operativ Systems disk i samma behållare som användar bilden.</span><span class="sxs-lookup"><span data-stu-id="1e30d-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="1e30d-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="1e30d-118">-ImageReferenceId</span></span>
<span data-ttu-id="1e30d-119">Anger bild referens-ID.</span><span class="sxs-lookup"><span data-stu-id="1e30d-119">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="1e30d-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="1e30d-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="1e30d-121">Anger typen av virtuell dator avbildning (VMImage).</span><span class="sxs-lookup"><span data-stu-id="1e30d-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="1e30d-122">För att få ett bild utbud, Använd cmdleten Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="1e30d-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="1e30d-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="1e30d-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="1e30d-124">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="1e30d-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="1e30d-125">Använd Get-AzureRmVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="1e30d-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="1e30d-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="1e30d-126">-ImageReferenceSku</span></span>
<span data-ttu-id="1e30d-127">Anger VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="1e30d-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="1e30d-128">För att få SKU: er, Använd Get-AzureRmVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e30d-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="1e30d-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="1e30d-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="1e30d-130">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="1e30d-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="1e30d-131">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="1e30d-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="1e30d-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1e30d-132">-ManagedDisk</span></span>
<span data-ttu-id="1e30d-133">Anger den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="1e30d-133">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="1e30d-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="1e30d-134">-OsDiskCaching</span></span>
<span data-ttu-id="1e30d-135">Anger operativ system diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="1e30d-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="1e30d-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1e30d-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e30d-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1e30d-137">ReadOnly</span></span>
- <span data-ttu-id="1e30d-138">Läs</span><span class="sxs-lookup"><span data-stu-id="1e30d-138">ReadWrite</span></span>

<span data-ttu-id="1e30d-139">Standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="1e30d-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="1e30d-140">Om du ändrar värdet för cachelagring startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="1e30d-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="1e30d-141">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="1e30d-141">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="1e30d-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="1e30d-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="1e30d-143">Anger hur den här cmdleten skapar de VMSS virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="1e30d-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="1e30d-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1e30d-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e30d-145">Bifoga: det här värdet används när du använder en specialiserad disk för att skapa den VMSS virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1e30d-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="1e30d-146">FromImage: det här värdet används när du använder en bild för att skapa den virtuella VMSS-datorn.</span><span class="sxs-lookup"><span data-stu-id="1e30d-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="1e30d-147">Om du använder en plattforms bild kan du även använda parametern *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="1e30d-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="1e30d-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="1e30d-148">-OsDiskName</span></span>
<span data-ttu-id="1e30d-149">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="1e30d-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="1e30d-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="1e30d-150">-OsDiskOsType</span></span>
<span data-ttu-id="1e30d-151">Anger operativ systemet på disken.</span><span class="sxs-lookup"><span data-stu-id="1e30d-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="1e30d-152">Detta krävs endast för användar bild scenarier och inte för en plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="1e30d-152">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="1e30d-153">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="1e30d-153">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="1e30d-154">Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.</span><span class="sxs-lookup"><span data-stu-id="1e30d-154">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="1e30d-155">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="1e30d-155">-VhdContainer</span></span>
<span data-ttu-id="1e30d-156">Anger de URL-adresser som används för att lagra operativ system diskar för VMSS.</span><span class="sxs-lookup"><span data-stu-id="1e30d-156">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="1e30d-157">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1e30d-157">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1e30d-158">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="1e30d-158">Specifies the VMSS object.</span></span>
<span data-ttu-id="1e30d-159">Använd New-AzureRmVmssConfig-objektet för att få ett objekt.</span><span class="sxs-lookup"><span data-stu-id="1e30d-159">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

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

### <span data-ttu-id="1e30d-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e30d-160">-Confirm</span></span>
<span data-ttu-id="1e30d-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e30d-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e30d-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e30d-162">-WhatIf</span></span>
<span data-ttu-id="1e30d-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e30d-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e30d-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e30d-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e30d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e30d-165">CommonParameters</span></span>
<span data-ttu-id="1e30d-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e30d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e30d-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e30d-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e30d-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e30d-168">INPUTS</span></span>

###  
<span data-ttu-id="1e30d-169">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1e30d-169">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1e30d-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e30d-170">OUTPUTS</span></span>

### <span data-ttu-id="1e30d-171">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1e30d-171">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1e30d-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e30d-172">NOTES</span></span>

## <span data-ttu-id="1e30d-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e30d-173">RELATED LINKS</span></span>

[<span data-ttu-id="1e30d-174">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="1e30d-174">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="1e30d-175">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1e30d-175">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="1e30d-176">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="1e30d-176">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="1e30d-177">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1e30d-177">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


