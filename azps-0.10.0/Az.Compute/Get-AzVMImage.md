---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 7b7a61c6d3043fcb4687d75ac49400b88361b81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925170"
---
# <span data-ttu-id="6f715-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="6f715-101">Get-AzVMImage</span></span>

## <span data-ttu-id="6f715-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f715-102">SYNOPSIS</span></span>
<span data-ttu-id="6f715-103">Får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="6f715-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="6f715-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f715-104">SYNTAX</span></span>

### <span data-ttu-id="6f715-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="6f715-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f715-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="6f715-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f715-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f715-107">DESCRIPTION</span></span>
<span data-ttu-id="6f715-108">Cmdleten **Get-AzVMImage** får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="6f715-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="6f715-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f715-109">EXAMPLES</span></span>

### <span data-ttu-id="6f715-110">Exempel 1: skaffa VMImage-objekt</span><span class="sxs-lookup"><span data-stu-id="6f715-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="6f715-111">Det här kommandot får alla versioner av VMImage som matchar de angivna värdena.</span><span class="sxs-lookup"><span data-stu-id="6f715-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="6f715-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f715-112">PARAMETERS</span></span>

### <span data-ttu-id="6f715-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f715-113">-DefaultProfile</span></span>
<span data-ttu-id="6f715-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f715-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f715-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="6f715-115">-FilterExpression</span></span>
<span data-ttu-id="6f715-116">Anger ett filter uttryck.</span><span class="sxs-lookup"><span data-stu-id="6f715-116">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f715-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="6f715-117">-Location</span></span>
<span data-ttu-id="6f715-118">Anger platsen för en VMImage.</span><span class="sxs-lookup"><span data-stu-id="6f715-118">Specifies the location of a VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f715-119">-Ge</span><span class="sxs-lookup"><span data-stu-id="6f715-119">-Offer</span></span>
<span data-ttu-id="6f715-120">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="6f715-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="6f715-121">För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="6f715-121">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f715-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="6f715-122">-PublisherName</span></span>
<span data-ttu-id="6f715-123">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="6f715-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="6f715-124">Använd Get-AzVMImagePublisher cmdlet för att få en bild utgivare.</span><span class="sxs-lookup"><span data-stu-id="6f715-124">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f715-125">-SKU: er</span><span class="sxs-lookup"><span data-stu-id="6f715-125">-Skus</span></span>
<span data-ttu-id="6f715-126">Anger en VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="6f715-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="6f715-127">För att skaffa en SKU, Använd cmdleten Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="6f715-127">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f715-128">-Version</span><span class="sxs-lookup"><span data-stu-id="6f715-128">-Version</span></span>
<span data-ttu-id="6f715-129">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="6f715-129">Specifies the version of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f715-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f715-130">CommonParameters</span></span>
<span data-ttu-id="6f715-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f715-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f715-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f715-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f715-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f715-133">INPUTS</span></span>

### <span data-ttu-id="6f715-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="6f715-134">None</span></span>
<span data-ttu-id="6f715-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6f715-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f715-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f715-136">OUTPUTS</span></span>

### <span data-ttu-id="6f715-137">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="6f715-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="6f715-138">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="6f715-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="6f715-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f715-139">NOTES</span></span>

## <span data-ttu-id="6f715-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f715-140">RELATED LINKS</span></span>

[<span data-ttu-id="6f715-141">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="6f715-141">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="6f715-142">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6f715-142">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="6f715-143">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="6f715-143">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="6f715-144">Spara – AzVMImage</span><span class="sxs-lookup"><span data-stu-id="6f715-144">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


