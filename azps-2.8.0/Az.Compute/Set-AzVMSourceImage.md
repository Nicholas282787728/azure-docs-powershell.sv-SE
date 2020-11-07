---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a9dff8f9661cfc7826adba78eca3d12961b343e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744924"
---
# <span data-ttu-id="d9509-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="d9509-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="d9509-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9509-102">SYNOPSIS</span></span>
<span data-ttu-id="d9509-103">Anger bilden för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d9509-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="d9509-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9509-104">SYNTAX</span></span>

### <span data-ttu-id="d9509-105">ImageReferenceSkuParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d9509-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9509-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9509-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9509-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9509-107">DESCRIPTION</span></span>
<span data-ttu-id="d9509-108">Cmdleten **set-AzVMSourceImage** anger vilken plattforms bild som ska användas för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d9509-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="d9509-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9509-109">EXAMPLES</span></span>

### <span data-ttu-id="d9509-110">Exempel 1: Ange värden för en bild</span><span class="sxs-lookup"><span data-stu-id="d9509-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="d9509-111">Det första kommandot får den tillgänglighets uppsättning som heter AvailabilitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="d9509-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="d9509-112">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="d9509-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d9509-113">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="d9509-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="d9509-114">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="d9509-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="d9509-115">Det sista kommandot ställer in värden för utgivarens namn, offerter, SKU och version.</span><span class="sxs-lookup"><span data-stu-id="d9509-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="d9509-116">De här inställningarna kan upptäckas i cmdletarna **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** och **Get-AzVMImage** .</span><span class="sxs-lookup"><span data-stu-id="d9509-116">The **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** , and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="d9509-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9509-117">PARAMETERS</span></span>

### <span data-ttu-id="d9509-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9509-118">-DefaultProfile</span></span>
<span data-ttu-id="d9509-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9509-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9509-120">-ID</span><span class="sxs-lookup"><span data-stu-id="d9509-120">-Id</span></span>
<span data-ttu-id="d9509-121">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="d9509-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="d9509-122">-Ge</span><span class="sxs-lookup"><span data-stu-id="d9509-122">-Offer</span></span>
<span data-ttu-id="d9509-123">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="d9509-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="d9509-124">För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="d9509-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="d9509-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="d9509-125">-PublisherName</span></span>
<span data-ttu-id="d9509-126">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="d9509-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="d9509-127">Använd Get-AzVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="d9509-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="d9509-128">-SKU: er</span><span class="sxs-lookup"><span data-stu-id="d9509-128">-Skus</span></span>
<span data-ttu-id="d9509-129">Anger en VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="d9509-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="d9509-130">För att få SKU: er, Använd Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9509-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="d9509-131">-Version</span><span class="sxs-lookup"><span data-stu-id="d9509-131">-Version</span></span>
<span data-ttu-id="d9509-132">Anger en version av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="d9509-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="d9509-133">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="d9509-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="d9509-134">-VM</span><span class="sxs-lookup"><span data-stu-id="d9509-134">-VM</span></span>
<span data-ttu-id="d9509-135">Anger det lokala virtuella dator objekt som ska konfigureras.</span><span class="sxs-lookup"><span data-stu-id="d9509-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="d9509-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9509-136">CommonParameters</span></span>
<span data-ttu-id="d9509-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9509-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9509-138">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9509-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9509-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9509-139">INPUTS</span></span>

### <span data-ttu-id="d9509-140">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d9509-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="d9509-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d9509-141">System.String</span></span>

## <span data-ttu-id="d9509-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9509-142">OUTPUTS</span></span>

### <span data-ttu-id="d9509-143">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d9509-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d9509-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9509-144">NOTES</span></span>

## <span data-ttu-id="d9509-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9509-145">RELATED LINKS</span></span>

[<span data-ttu-id="d9509-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d9509-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="d9509-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d9509-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="d9509-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d9509-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="d9509-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d9509-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="d9509-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d9509-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="d9509-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d9509-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


