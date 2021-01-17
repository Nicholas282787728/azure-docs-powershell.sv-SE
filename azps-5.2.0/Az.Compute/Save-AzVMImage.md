---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 0d2a4ade662ec23a4a139460bce8fe5387683120
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416520"
---
# <span data-ttu-id="fcdeb-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="fcdeb-101">Save-AzVMImage</span></span>

## <span data-ttu-id="fcdeb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fcdeb-102">SYNOPSIS</span></span>
<span data-ttu-id="fcdeb-103">Sparar en virtuell dator som en VMImage.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="fcdeb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fcdeb-104">SYNTAX</span></span>

### <span data-ttu-id="fcdeb-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="fcdeb-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fcdeb-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="fcdeb-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcdeb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fcdeb-107">DESCRIPTION</span></span>
<span data-ttu-id="fcdeb-108">Cmdleten **Save-AzVMImage** sparar en virtuell dator som en VMImage.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="fcdeb-109">Innan du skapar en virtuell dator bild, syspreperar du den virtuella datorn och markerar den som allmänt med hjälp av Set-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="fcdeb-110">Utdata från denna cmdlet är en JSON-mall (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="fcdeb-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="fcdeb-111">Du kan distribuera virtuella datorer från din bild.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="fcdeb-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fcdeb-112">EXAMPLES</span></span>

### <span data-ttu-id="fcdeb-113">Exempel 1: avbilda en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="fcdeb-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="fcdeb-114">Det första kommandot anger den virtuella datorn med namnet VirtualMachine07 som allmänt.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="fcdeb-115">Det andra kommandot fångar en virtuell dator med namnet VirtualMachine07 som en VMImage.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="fcdeb-116">Egenskapen **output** returnerar en JSON-mall.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="fcdeb-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fcdeb-117">PARAMETERS</span></span>

### <span data-ttu-id="fcdeb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcdeb-118">-AsJob</span></span>
<span data-ttu-id="fcdeb-119">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fcdeb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcdeb-120">-DefaultProfile</span></span>
<span data-ttu-id="fcdeb-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcdeb-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="fcdeb-122">-DestinationContainerName</span></span>
<span data-ttu-id="fcdeb-123">Anger namnet på en behållare i "system"-behållaren som du vill hålla bilderna till.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="fcdeb-124">Om behållaren inte finns skapas den åt dig.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="fcdeb-125">De virtuella hård diskar (VHD: er) som utgörs av VMImage finns i behållaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="fcdeb-126">Om VHD-diskar sprids över flera lagrings konton skapar denna cmdlet en behållare med det här namnet i varje lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="fcdeb-127">URL-adressen till den sparade bilden liknar: https:// \<storageAccountName\> . blob.Core.Windows.net/system/Microsoft.Compute/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX. VHD.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="fcdeb-128">-ID</span><span class="sxs-lookup"><span data-stu-id="fcdeb-128">-Id</span></span>
<span data-ttu-id="fcdeb-129">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="fcdeb-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="fcdeb-130">-Name</span></span>
<span data-ttu-id="fcdeb-131">Anger ett namn.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcdeb-132">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="fcdeb-132">-Overwrite</span></span>
<span data-ttu-id="fcdeb-133">Anger att denna cmdlet skriver över alla VHD-diskar som har samma prefix i mål behållaren.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="fcdeb-134">-Path</span><span class="sxs-lookup"><span data-stu-id="fcdeb-134">-Path</span></span>
<span data-ttu-id="fcdeb-135">Fil Sök vägen där mallen för den fångade bilden lagras.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="fcdeb-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcdeb-136">-ResourceGroupName</span></span>
<span data-ttu-id="fcdeb-137">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fcdeb-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="fcdeb-138">-VHDNamePrefix</span></span>
<span data-ttu-id="fcdeb-139">Anger prefixet i namnet på de blobbar som utgör lagrings profilen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="fcdeb-140">Ett prefix vhdPrefix för en operativ system disk ger till exempel namnet vhdPrefix-OSDisk. \<guid\> . VHD.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="fcdeb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcdeb-141">CommonParameters</span></span>
<span data-ttu-id="fcdeb-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcdeb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcdeb-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcdeb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcdeb-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fcdeb-144">INPUTS</span></span>

### <span data-ttu-id="fcdeb-145">System. String</span><span class="sxs-lookup"><span data-stu-id="fcdeb-145">System.String</span></span>

### <span data-ttu-id="fcdeb-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fcdeb-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fcdeb-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fcdeb-147">OUTPUTS</span></span>

### <span data-ttu-id="fcdeb-148">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="fcdeb-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="fcdeb-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fcdeb-149">NOTES</span></span>

## <span data-ttu-id="fcdeb-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fcdeb-150">RELATED LINKS</span></span>

[<span data-ttu-id="fcdeb-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="fcdeb-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="fcdeb-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="fcdeb-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="fcdeb-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fcdeb-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="fcdeb-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fcdeb-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="fcdeb-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="fcdeb-155">Set-AzVM</span></span>](./Set-AzVM.md)


