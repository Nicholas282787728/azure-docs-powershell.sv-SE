---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: c164d352256f84ea18c09b775c9a9639dbde7866
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577082"
---
# <span data-ttu-id="4cb81-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="4cb81-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="4cb81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cb81-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb81-103">Anger bilden för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4cb81-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cb81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cb81-104">SYNTAX</span></span>

### <span data-ttu-id="4cb81-105">ImageReferenceSkuParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4cb81-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cb81-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cb81-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cb81-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cb81-107">DESCRIPTION</span></span>
<span data-ttu-id="4cb81-108">Cmdleten **set-AzureRmVMSourceImage** anger vilken plattforms bild som ska användas för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4cb81-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="4cb81-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cb81-109">EXAMPLES</span></span>

### <span data-ttu-id="4cb81-110">Exempel 1: Ange värden för en bild</span><span class="sxs-lookup"><span data-stu-id="4cb81-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="4cb81-111">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="4cb81-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4cb81-112">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="4cb81-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4cb81-113">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="4cb81-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4cb81-114">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4cb81-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4cb81-115">Det sista kommandot ställer in värden för utgivarens namn, offerter, SKU och version.</span><span class="sxs-lookup"><span data-stu-id="4cb81-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="4cb81-116">De här inställningarna kan upptäckas i cmdletarna **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** och **Get-AzureRmVMImage** .</span><span class="sxs-lookup"><span data-stu-id="4cb81-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="4cb81-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cb81-117">PARAMETERS</span></span>

### <span data-ttu-id="4cb81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb81-118">-DefaultProfile</span></span>
<span data-ttu-id="4cb81-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cb81-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cb81-120">-ID</span><span class="sxs-lookup"><span data-stu-id="4cb81-120">-Id</span></span>
<span data-ttu-id="4cb81-121">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="4cb81-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="4cb81-122">-Ge</span><span class="sxs-lookup"><span data-stu-id="4cb81-122">-Offer</span></span>
<span data-ttu-id="4cb81-123">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="4cb81-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="4cb81-124">För att få ett bild utbud, Använd cmdleten Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="4cb81-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="4cb81-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4cb81-125">-PublisherName</span></span>
<span data-ttu-id="4cb81-126">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="4cb81-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="4cb81-127">Använd Get-AzureRmVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="4cb81-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4cb81-128">-SKU: er</span><span class="sxs-lookup"><span data-stu-id="4cb81-128">-Skus</span></span>
<span data-ttu-id="4cb81-129">Anger en VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="4cb81-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="4cb81-130">För att få SKU: er, Använd Get-AzureRmVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cb81-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="4cb81-131">-Version</span><span class="sxs-lookup"><span data-stu-id="4cb81-131">-Version</span></span>
<span data-ttu-id="4cb81-132">Anger en version av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="4cb81-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="4cb81-133">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="4cb81-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="4cb81-134">-VM</span><span class="sxs-lookup"><span data-stu-id="4cb81-134">-VM</span></span>
<span data-ttu-id="4cb81-135">Anger det lokala virtuella dator objekt som ska konfigureras.</span><span class="sxs-lookup"><span data-stu-id="4cb81-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="4cb81-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb81-136">CommonParameters</span></span>
<span data-ttu-id="4cb81-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cb81-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb81-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cb81-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb81-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cb81-139">INPUTS</span></span>

### <span data-ttu-id="4cb81-140">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4cb81-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4cb81-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4cb81-141">System.String</span></span>

## <span data-ttu-id="4cb81-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cb81-142">OUTPUTS</span></span>

### <span data-ttu-id="4cb81-143">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4cb81-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4cb81-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cb81-144">NOTES</span></span>

## <span data-ttu-id="4cb81-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cb81-145">RELATED LINKS</span></span>

[<span data-ttu-id="4cb81-146">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4cb81-146">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="4cb81-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4cb81-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4cb81-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4cb81-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="4cb81-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4cb81-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4cb81-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4cb81-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="4cb81-151">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="4cb81-151">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


