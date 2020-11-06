---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: cadcaccc2bb93dee5298ca92561c5bef36b5d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585727"
---
# <span data-ttu-id="40e14-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="40e14-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="40e14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40e14-102">SYNOPSIS</span></span>
<span data-ttu-id="40e14-103">Sparar en virtuell dator som en VMImage.</span><span class="sxs-lookup"><span data-stu-id="40e14-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40e14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40e14-104">SYNTAX</span></span>

### <span data-ttu-id="40e14-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="40e14-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40e14-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="40e14-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40e14-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40e14-107">DESCRIPTION</span></span>
<span data-ttu-id="40e14-108">Cmdleten **Save-AzureRmVMImage** sparar en virtuell dator som en VMImage.</span><span class="sxs-lookup"><span data-stu-id="40e14-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="40e14-109">Innan du skapar en virtuell dator bild, syspreperar du den virtuella datorn och markerar den som allmänt med hjälp av Set-AzureRmVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40e14-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="40e14-110">Utdata från denna cmdlet är en JSON-mall (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="40e14-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="40e14-111">Du kan distribuera virtuella datorer från din bild.</span><span class="sxs-lookup"><span data-stu-id="40e14-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="40e14-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40e14-112">EXAMPLES</span></span>

### <span data-ttu-id="40e14-113">Exempel 1: avbilda en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="40e14-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="40e14-114">Det första kommandot anger den virtuella datorn med namnet VirtualMachine07 som allmänt.</span><span class="sxs-lookup"><span data-stu-id="40e14-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="40e14-115">Det andra kommandot fångar en virtuell dator med namnet VirtualMachine07 som en VMImage.</span><span class="sxs-lookup"><span data-stu-id="40e14-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="40e14-116">Egenskapen **output** returnerar en JSON-mall.</span><span class="sxs-lookup"><span data-stu-id="40e14-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="40e14-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40e14-117">PARAMETERS</span></span>

### <span data-ttu-id="40e14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e14-118">-DefaultProfile</span></span>
<span data-ttu-id="40e14-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40e14-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e14-120">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="40e14-120">-DestinationContainerName</span></span>
<span data-ttu-id="40e14-121">Anger namnet på en behållare i "system"-behållaren som du vill hålla bilderna till.</span><span class="sxs-lookup"><span data-stu-id="40e14-121">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="40e14-122">Om behållaren inte finns skapas den åt dig.</span><span class="sxs-lookup"><span data-stu-id="40e14-122">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="40e14-123">De virtuella hård diskar (VHD: er) som utgörs av VMImage finns i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="40e14-123">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="40e14-124">Om VHD-diskar sprids över flera lagrings konton skapar denna cmdlet en behållare med det här namnet i varje lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="40e14-124">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="40e14-125">URL-adressen till den sparade bilden liknar:</span><span class="sxs-lookup"><span data-stu-id="40e14-125">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="40e14-126"> https:// \<storageAccountName\> . blob.Core.Windows.net/system/Microsoft.Compute/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX. VHD.</span><span class="sxs-lookup"><span data-stu-id="40e14-126">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e14-127">-ID</span><span class="sxs-lookup"><span data-stu-id="40e14-127">-Id</span></span>
<span data-ttu-id="40e14-128">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="40e14-128">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e14-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="40e14-129">-Name</span></span>
<span data-ttu-id="40e14-130">Anger ett namn.</span><span class="sxs-lookup"><span data-stu-id="40e14-130">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e14-131">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="40e14-131">-Overwrite</span></span>
<span data-ttu-id="40e14-132">Anger att denna cmdlet skriver över alla VHD-diskar som har samma prefix i mål behållaren.</span><span class="sxs-lookup"><span data-stu-id="40e14-132">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e14-133">-Path</span><span class="sxs-lookup"><span data-stu-id="40e14-133">-Path</span></span>
<span data-ttu-id="40e14-134">Anger sökvägen för VHD: n.</span><span class="sxs-lookup"><span data-stu-id="40e14-134">Specifies the path of the VHD.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e14-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e14-135">-ResourceGroupName</span></span>
<span data-ttu-id="40e14-136">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="40e14-136">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e14-137">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="40e14-137">-VHDNamePrefix</span></span>
<span data-ttu-id="40e14-138">Anger prefixet i namnet på de blobbar som utgör lagrings profilen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="40e14-138">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="40e14-139">Ett prefix vhdPrefix för en operativ system disk ger till exempel namnet vhdPrefix-OSDisk. \<guid\> . VHD.</span><span class="sxs-lookup"><span data-stu-id="40e14-139">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e14-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e14-140">CommonParameters</span></span>
<span data-ttu-id="40e14-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e14-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e14-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e14-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e14-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40e14-143">INPUTS</span></span>

## <span data-ttu-id="40e14-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40e14-144">OUTPUTS</span></span>

## <span data-ttu-id="40e14-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40e14-145">NOTES</span></span>

## <span data-ttu-id="40e14-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40e14-146">RELATED LINKS</span></span>

[<span data-ttu-id="40e14-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="40e14-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="40e14-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="40e14-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="40e14-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="40e14-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="40e14-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="40e14-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="40e14-151">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="40e14-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


