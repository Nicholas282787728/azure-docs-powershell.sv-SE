---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 7c4b59f97a6cd74da791f090b1c90be72f43a2c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757710"
---
# <span data-ttu-id="7277f-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7277f-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="7277f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7277f-102">SYNOPSIS</span></span>
<span data-ttu-id="7277f-103">Får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="7277f-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7277f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7277f-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String> [<CommonParameters>]
```

## <span data-ttu-id="7277f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7277f-105">DESCRIPTION</span></span>
<span data-ttu-id="7277f-106">Cmdleten **Get-AzureRmVMImageSku** får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="7277f-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="7277f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7277f-107">EXAMPLES</span></span>

### <span data-ttu-id="7277f-108">Exempel 1: skaffa VMImage SKU: er</span><span class="sxs-lookup"><span data-stu-id="7277f-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="7277f-109">Det här kommandot får SKU: erna för den angivna utgivaren och anbudet.</span><span class="sxs-lookup"><span data-stu-id="7277f-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="7277f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7277f-110">PARAMETERS</span></span>

### <span data-ttu-id="7277f-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="7277f-111">-Location</span></span>
<span data-ttu-id="7277f-112">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="7277f-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="7277f-113">-Ge</span><span class="sxs-lookup"><span data-stu-id="7277f-113">-Offer</span></span>
<span data-ttu-id="7277f-114">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="7277f-114">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="7277f-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7277f-115">-PublisherName</span></span>
<span data-ttu-id="7277f-116">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="7277f-116">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="7277f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7277f-117">CommonParameters</span></span>
<span data-ttu-id="7277f-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7277f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7277f-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7277f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7277f-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7277f-120">INPUTS</span></span>

### <span data-ttu-id="7277f-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="7277f-121">None</span></span>
<span data-ttu-id="7277f-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7277f-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7277f-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7277f-123">OUTPUTS</span></span>

## <span data-ttu-id="7277f-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7277f-124">NOTES</span></span>

## <span data-ttu-id="7277f-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7277f-125">RELATED LINKS</span></span>

[<span data-ttu-id="7277f-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7277f-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="7277f-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7277f-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="7277f-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7277f-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="7277f-129">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7277f-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


