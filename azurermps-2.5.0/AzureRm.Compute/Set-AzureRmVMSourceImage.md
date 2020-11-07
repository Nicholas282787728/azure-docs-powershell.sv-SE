---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsourceimage
schema: 2.0.0
ms.openlocfilehash: 5e07ba8ffceb42a94c41c0b21c62329f9dbe96a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929949"
---
# <span data-ttu-id="438f9-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="438f9-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="438f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="438f9-102">SYNOPSIS</span></span>
<span data-ttu-id="438f9-103">Anger bilden för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="438f9-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="438f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="438f9-104">SYNTAX</span></span>

### <span data-ttu-id="438f9-105">ImageReferenceSkuParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="438f9-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="438f9-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="438f9-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="438f9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="438f9-107">DESCRIPTION</span></span>
<span data-ttu-id="438f9-108">Cmdleten **set-AzureRmVMSourceImage** anger vilken plattforms bild som ska användas för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="438f9-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="438f9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="438f9-109">EXAMPLES</span></span>

### <span data-ttu-id="438f9-110">Exempel 1: Ange värden för en bild</span><span class="sxs-lookup"><span data-stu-id="438f9-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="438f9-111">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="438f9-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="438f9-112">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="438f9-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="438f9-113">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="438f9-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="438f9-114">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="438f9-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="438f9-115">Det sista kommandot ställer in värden för utgivarens namn, offerter, SKU och version.</span><span class="sxs-lookup"><span data-stu-id="438f9-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="438f9-116">De här inställningarna kan upptäckas i cmdletarna **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** och **Get-AzureRmVMImage** .</span><span class="sxs-lookup"><span data-stu-id="438f9-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="438f9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="438f9-117">PARAMETERS</span></span>

### <span data-ttu-id="438f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="438f9-118">-DefaultProfile</span></span>
<span data-ttu-id="438f9-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="438f9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="438f9-120">-ID</span><span class="sxs-lookup"><span data-stu-id="438f9-120">-Id</span></span>
<span data-ttu-id="438f9-121">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="438f9-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="438f9-122">-Ge</span><span class="sxs-lookup"><span data-stu-id="438f9-122">-Offer</span></span>
<span data-ttu-id="438f9-123">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="438f9-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="438f9-124">För att få ett bild utbud, Använd cmdleten Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="438f9-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="438f9-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="438f9-125">-PublisherName</span></span>
<span data-ttu-id="438f9-126">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="438f9-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="438f9-127">Använd Get-AzureRmVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="438f9-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="438f9-128">-SKU: er</span><span class="sxs-lookup"><span data-stu-id="438f9-128">-Skus</span></span>
<span data-ttu-id="438f9-129">Anger en VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="438f9-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="438f9-130">För att få SKU: er, Använd Get-AzureRmVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="438f9-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="438f9-131">-Version</span><span class="sxs-lookup"><span data-stu-id="438f9-131">-Version</span></span>
<span data-ttu-id="438f9-132">Anger en version av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="438f9-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="438f9-133">För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.</span><span class="sxs-lookup"><span data-stu-id="438f9-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="438f9-134">-VM</span><span class="sxs-lookup"><span data-stu-id="438f9-134">-VM</span></span>
<span data-ttu-id="438f9-135">Anger det lokala virtuella dator objekt som ska konfigureras.</span><span class="sxs-lookup"><span data-stu-id="438f9-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="438f9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="438f9-136">CommonParameters</span></span>
<span data-ttu-id="438f9-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="438f9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="438f9-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="438f9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="438f9-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="438f9-139">INPUTS</span></span>

### <span data-ttu-id="438f9-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="438f9-140">PSVirtualMachine</span></span>
<span data-ttu-id="438f9-141">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="438f9-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="438f9-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="438f9-142">OUTPUTS</span></span>

### <span data-ttu-id="438f9-143">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="438f9-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="438f9-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="438f9-144">NOTES</span></span>

## <span data-ttu-id="438f9-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="438f9-145">RELATED LINKS</span></span>

[<span data-ttu-id="438f9-146">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="438f9-146">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="438f9-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="438f9-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="438f9-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="438f9-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="438f9-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="438f9-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="438f9-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="438f9-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="438f9-151">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="438f9-151">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


