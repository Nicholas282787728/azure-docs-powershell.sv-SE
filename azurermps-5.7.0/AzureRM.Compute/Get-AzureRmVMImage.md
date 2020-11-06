---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574359"
---
# <span data-ttu-id="664b2-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="664b2-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="664b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="664b2-102">SYNOPSIS</span></span>
<span data-ttu-id="664b2-103">Får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="664b2-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="664b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="664b2-104">SYNTAX</span></span>

### <span data-ttu-id="664b2-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="664b2-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### <span data-ttu-id="664b2-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="664b2-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## <span data-ttu-id="664b2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="664b2-107">DESCRIPTION</span></span>
<span data-ttu-id="664b2-108">Cmdleten **Get-AzureRmVMImage** får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="664b2-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="664b2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="664b2-109">EXAMPLES</span></span>

### <span data-ttu-id="664b2-110">Exempel 1: skaffa VMImage-objekt</span><span class="sxs-lookup"><span data-stu-id="664b2-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="664b2-111">Det här kommandot får alla versioner av VMImage som matchar de angivna värdena.</span><span class="sxs-lookup"><span data-stu-id="664b2-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="664b2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="664b2-112">PARAMETERS</span></span>

### <span data-ttu-id="664b2-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="664b2-113">-FilterExpression</span></span>
<span data-ttu-id="664b2-114">Anger ett filter uttryck.</span><span class="sxs-lookup"><span data-stu-id="664b2-114">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="664b2-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="664b2-115">-Location</span></span>
<span data-ttu-id="664b2-116">Anger platsen för en VMImage.</span><span class="sxs-lookup"><span data-stu-id="664b2-116">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="664b2-117">-Ge</span><span class="sxs-lookup"><span data-stu-id="664b2-117">-Offer</span></span>
<span data-ttu-id="664b2-118">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="664b2-118">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="664b2-119">För att få ett bild utbud, Använd cmdleten Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="664b2-119">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="664b2-120">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="664b2-120">-PublisherName</span></span>
<span data-ttu-id="664b2-121">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="664b2-121">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="664b2-122">Använd Get-AzureRmVMImagePublisher cmdlet för att få en bild utgivare.</span><span class="sxs-lookup"><span data-stu-id="664b2-122">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="664b2-123">-SKU: er</span><span class="sxs-lookup"><span data-stu-id="664b2-123">-Skus</span></span>
<span data-ttu-id="664b2-124">Anger en VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="664b2-124">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="664b2-125">För att skaffa en SKU, Använd cmdleten Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="664b2-125">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="664b2-126">-Version</span><span class="sxs-lookup"><span data-stu-id="664b2-126">-Version</span></span>
<span data-ttu-id="664b2-127">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="664b2-127">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="664b2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664b2-128">CommonParameters</span></span>
<span data-ttu-id="664b2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="664b2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664b2-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="664b2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664b2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="664b2-131">INPUTS</span></span>

### <span data-ttu-id="664b2-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="664b2-132">None</span></span>
<span data-ttu-id="664b2-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="664b2-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="664b2-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="664b2-134">OUTPUTS</span></span>

## <span data-ttu-id="664b2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="664b2-135">NOTES</span></span>

## <span data-ttu-id="664b2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="664b2-136">RELATED LINKS</span></span>

[<span data-ttu-id="664b2-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="664b2-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="664b2-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="664b2-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="664b2-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="664b2-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="664b2-140">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="664b2-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


