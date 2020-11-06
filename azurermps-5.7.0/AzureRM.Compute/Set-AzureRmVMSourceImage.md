---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: d96d583f871e0d037c72018339d44952562bac35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574333"
---
# <span data-ttu-id="529b1-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="529b1-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="529b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="529b1-102">SYNOPSIS</span></span>
<span data-ttu-id="529b1-103">Anger bilden för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="529b1-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="529b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="529b1-104">SYNTAX</span></span>

### <span data-ttu-id="529b1-105">ImageReferenceSkuParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="529b1-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [<CommonParameters>]
```

### <span data-ttu-id="529b1-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="529b1-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="529b1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="529b1-107">DESCRIPTION</span></span>
<span data-ttu-id="529b1-108">Cmdleten **set-AzureRmVMSourceImage** anger vilken plattforms bild som ska användas för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="529b1-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="529b1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="529b1-109">EXAMPLES</span></span>

### <span data-ttu-id="529b1-110">Exempel 1: Ange värden för en bild</span><span class="sxs-lookup"><span data-stu-id="529b1-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="529b1-111">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="529b1-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="529b1-112">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="529b1-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="529b1-113">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="529b1-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="529b1-114">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="529b1-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="529b1-115">Det sista kommandot ställer in värden för utgivarens namn, offerter, SKU och version.</span><span class="sxs-lookup"><span data-stu-id="529b1-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="529b1-116">De här inställningarna kan upptäckas i cmdletarna **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** och **Get-AzureRmVMImage** .</span><span class="sxs-lookup"><span data-stu-id="529b1-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="529b1-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="529b1-117">PARAMETERS</span></span>

### <span data-ttu-id="529b1-118">-ID</span><span class="sxs-lookup"><span data-stu-id="529b1-118">-Id</span></span>
<span data-ttu-id="529b1-119">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="529b1-119">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceIdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529b1-120">-Ge</span><span class="sxs-lookup"><span data-stu-id="529b1-120">-Offer</span></span>
<span data-ttu-id="529b1-121">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="529b1-121">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="529b1-122">För att få ett bild utbud, Använd cmdleten Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="529b1-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529b1-123">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="529b1-123">-PublisherName</span></span>
<span data-ttu-id="529b1-124">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="529b1-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="529b1-125">Använd Get-AzureRmVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="529b1-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529b1-126">-SKU: er</span><span class="sxs-lookup"><span data-stu-id="529b1-126">-Skus</span></span>
<span data-ttu-id="529b1-127">Anger en VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="529b1-127">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="529b1-128">För att få SKU: er, Använd Get-AzureRmVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="529b1-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529b1-129">-Version</span><span class="sxs-lookup"><span data-stu-id="529b1-129">-Version</span></span>
<span data-ttu-id="529b1-130">Anger en version av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="529b1-130">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="529b1-131">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="529b1-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529b1-132">-VM</span><span class="sxs-lookup"><span data-stu-id="529b1-132">-VM</span></span>
<span data-ttu-id="529b1-133">Anger det lokala virtuella dator objekt som ska konfigureras.</span><span class="sxs-lookup"><span data-stu-id="529b1-133">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="529b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529b1-134">CommonParameters</span></span>
<span data-ttu-id="529b1-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="529b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529b1-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="529b1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529b1-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="529b1-137">INPUTS</span></span>

### <span data-ttu-id="529b1-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="529b1-138">None</span></span>
<span data-ttu-id="529b1-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="529b1-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="529b1-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="529b1-140">OUTPUTS</span></span>

## <span data-ttu-id="529b1-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="529b1-141">NOTES</span></span>

## <span data-ttu-id="529b1-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="529b1-142">RELATED LINKS</span></span>

[<span data-ttu-id="529b1-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="529b1-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="529b1-144">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="529b1-144">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="529b1-145">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="529b1-145">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="529b1-146">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="529b1-146">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="529b1-147">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="529b1-147">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="529b1-148">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="529b1-148">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


