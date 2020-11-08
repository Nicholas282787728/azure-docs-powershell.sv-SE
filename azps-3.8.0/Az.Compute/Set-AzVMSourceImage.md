---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a1ed1fa266638891507b6853199bff23d23aa1b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092348"
---
# <span data-ttu-id="01c72-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="01c72-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="01c72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01c72-102">SYNOPSIS</span></span>
<span data-ttu-id="01c72-103">Anger bilden för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="01c72-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="01c72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01c72-104">SYNTAX</span></span>

### <span data-ttu-id="01c72-105">ImageReferenceSkuParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="01c72-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01c72-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01c72-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01c72-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01c72-107">DESCRIPTION</span></span>
<span data-ttu-id="01c72-108">Cmdleten **set-AzVMSourceImage** anger vilken plattforms bild som ska användas för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="01c72-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="01c72-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01c72-109">EXAMPLES</span></span>

### <span data-ttu-id="01c72-110">Exempel 1: Ange värden för en bild</span><span class="sxs-lookup"><span data-stu-id="01c72-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="01c72-111">Det första kommandot får den tillgänglighets uppsättning som heter AvailabilitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="01c72-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="01c72-112">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="01c72-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="01c72-113">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="01c72-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="01c72-114">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="01c72-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="01c72-115">Det sista kommandot ställer in värden för utgivarens namn, offerter, SKU och version.</span><span class="sxs-lookup"><span data-stu-id="01c72-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="01c72-116">De här inställningarna kan upptäckas i cmdletarna **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** och **Get-AzVMImage** .</span><span class="sxs-lookup"><span data-stu-id="01c72-116">The **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** , and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="01c72-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01c72-117">PARAMETERS</span></span>

### <span data-ttu-id="01c72-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c72-118">-DefaultProfile</span></span>
<span data-ttu-id="01c72-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01c72-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01c72-120">-ID</span><span class="sxs-lookup"><span data-stu-id="01c72-120">-Id</span></span>
<span data-ttu-id="01c72-121">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="01c72-121">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c72-122">-Ge</span><span class="sxs-lookup"><span data-stu-id="01c72-122">-Offer</span></span>
<span data-ttu-id="01c72-123">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="01c72-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="01c72-124">För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="01c72-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c72-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="01c72-125">-PublisherName</span></span>
<span data-ttu-id="01c72-126">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="01c72-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="01c72-127">Använd Get-AzVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="01c72-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c72-128">-SKU: er</span><span class="sxs-lookup"><span data-stu-id="01c72-128">-Skus</span></span>
<span data-ttu-id="01c72-129">Anger en VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="01c72-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="01c72-130">För att få SKU: er, Använd Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01c72-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c72-131">-Version</span><span class="sxs-lookup"><span data-stu-id="01c72-131">-Version</span></span>
<span data-ttu-id="01c72-132">Anger en version av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="01c72-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="01c72-133">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="01c72-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c72-134">-VM</span><span class="sxs-lookup"><span data-stu-id="01c72-134">-VM</span></span>
<span data-ttu-id="01c72-135">Anger det lokala virtuella dator objekt som ska konfigureras.</span><span class="sxs-lookup"><span data-stu-id="01c72-135">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01c72-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c72-136">CommonParameters</span></span>
<span data-ttu-id="01c72-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c72-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c72-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01c72-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c72-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01c72-139">INPUTS</span></span>

### <span data-ttu-id="01c72-140">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="01c72-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="01c72-141">System. String</span><span class="sxs-lookup"><span data-stu-id="01c72-141">System.String</span></span>

## <span data-ttu-id="01c72-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01c72-142">OUTPUTS</span></span>

### <span data-ttu-id="01c72-143">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="01c72-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="01c72-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01c72-144">NOTES</span></span>

## <span data-ttu-id="01c72-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01c72-145">RELATED LINKS</span></span>

[<span data-ttu-id="01c72-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="01c72-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="01c72-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="01c72-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="01c72-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="01c72-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="01c72-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="01c72-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="01c72-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="01c72-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="01c72-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="01c72-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

