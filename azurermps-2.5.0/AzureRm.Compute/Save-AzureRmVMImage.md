---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: b781023b424dd23d3d0874893b724744ecb33bda
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931489"
---
# <span data-ttu-id="8d86e-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8d86e-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="8d86e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d86e-102">SYNOPSIS</span></span>
<span data-ttu-id="8d86e-103">Sparar en virtuell dator som en VMImage.</span><span class="sxs-lookup"><span data-stu-id="8d86e-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d86e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d86e-104">SYNTAX</span></span>

### <span data-ttu-id="8d86e-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="8d86e-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d86e-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8d86e-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d86e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d86e-107">DESCRIPTION</span></span>
<span data-ttu-id="8d86e-108">Cmdleten **Save-AzureRmVMImage** sparar en virtuell dator som en VMImage.</span><span class="sxs-lookup"><span data-stu-id="8d86e-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="8d86e-109">Innan du skapar en virtuell dator bild, syspreperar du den virtuella datorn och markerar den som allmänt med hjälp av Set-AzureRmVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d86e-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="8d86e-110">Utdata från denna cmdlet är en JSON-mall (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="8d86e-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="8d86e-111">Du kan distribuera virtuella datorer från din bild.</span><span class="sxs-lookup"><span data-stu-id="8d86e-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="8d86e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d86e-112">EXAMPLES</span></span>

### <span data-ttu-id="8d86e-113">Exempel 1: avbilda en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8d86e-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="8d86e-114">Det första kommandot anger den virtuella datorn med namnet VirtualMachine07 som allmänt.</span><span class="sxs-lookup"><span data-stu-id="8d86e-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="8d86e-115">Det andra kommandot fångar en virtuell dator med namnet VirtualMachine07 som en VMImage.</span><span class="sxs-lookup"><span data-stu-id="8d86e-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="8d86e-116">Egenskapen **output** returnerar en JSON-mall.</span><span class="sxs-lookup"><span data-stu-id="8d86e-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="8d86e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d86e-117">PARAMETERS</span></span>

### <span data-ttu-id="8d86e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d86e-118">-AsJob</span></span>
<span data-ttu-id="8d86e-119">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="8d86e-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8d86e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d86e-120">-DefaultProfile</span></span>
<span data-ttu-id="8d86e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d86e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d86e-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="8d86e-122">-DestinationContainerName</span></span>
<span data-ttu-id="8d86e-123">Anger namnet på en behållare i "system"-behållaren som du vill hålla bilderna till.</span><span class="sxs-lookup"><span data-stu-id="8d86e-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="8d86e-124">Om behållaren inte finns skapas den åt dig.</span><span class="sxs-lookup"><span data-stu-id="8d86e-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="8d86e-125">De virtuella hård diskar (VHD: er) som utgörs av VMImage finns i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8d86e-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="8d86e-126">Om VHD-diskar sprids över flera lagrings konton skapar denna cmdlet en behållare med det här namnet i varje lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8d86e-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="8d86e-127">URL-adressen till den sparade bilden liknar:</span><span class="sxs-lookup"><span data-stu-id="8d86e-127">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="8d86e-128"> https:// \<storageAccountName\> . blob.Core.Windows.net/system/Microsoft.Compute/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX. VHD.</span><span class="sxs-lookup"><span data-stu-id="8d86e-128">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d86e-129">-ID</span><span class="sxs-lookup"><span data-stu-id="8d86e-129">-Id</span></span>
<span data-ttu-id="8d86e-130">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="8d86e-130">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d86e-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="8d86e-131">-Name</span></span>
<span data-ttu-id="8d86e-132">Anger ett namn.</span><span class="sxs-lookup"><span data-stu-id="8d86e-132">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d86e-133">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="8d86e-133">-Overwrite</span></span>
<span data-ttu-id="8d86e-134">Anger att denna cmdlet skriver över alla VHD-diskar som har samma prefix i mål behållaren.</span><span class="sxs-lookup"><span data-stu-id="8d86e-134">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d86e-135">-Path</span><span class="sxs-lookup"><span data-stu-id="8d86e-135">-Path</span></span>
<span data-ttu-id="8d86e-136">Anger sökvägen för VHD: n.</span><span class="sxs-lookup"><span data-stu-id="8d86e-136">Specifies the path of the VHD.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d86e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d86e-137">-ResourceGroupName</span></span>
<span data-ttu-id="8d86e-138">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8d86e-138">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d86e-139">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="8d86e-139">-VHDNamePrefix</span></span>
<span data-ttu-id="8d86e-140">Anger prefixet i namnet på de blobbar som utgör lagrings profilen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="8d86e-140">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="8d86e-141">Ett prefix vhdPrefix för en operativ system disk ger till exempel namnet vhdPrefix-OSDisk. \<guid\> . VHD.</span><span class="sxs-lookup"><span data-stu-id="8d86e-141">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d86e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d86e-142">CommonParameters</span></span>
<span data-ttu-id="8d86e-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d86e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d86e-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d86e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d86e-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d86e-145">INPUTS</span></span>

### <span data-ttu-id="8d86e-146">Ingen</span><span class="sxs-lookup"><span data-stu-id="8d86e-146">None</span></span>
<span data-ttu-id="8d86e-147">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8d86e-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d86e-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d86e-148">OUTPUTS</span></span>

### <span data-ttu-id="8d86e-149">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="8d86e-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="8d86e-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d86e-150">NOTES</span></span>

## <span data-ttu-id="8d86e-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d86e-151">RELATED LINKS</span></span>

[<span data-ttu-id="8d86e-152">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8d86e-152">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="8d86e-153">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8d86e-153">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="8d86e-154">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8d86e-154">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="8d86e-155">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8d86e-155">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="8d86e-156">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d86e-156">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


