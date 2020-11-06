---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 15b1316940c42534844245eaaf1aee3e450adc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574361"
---
# <span data-ttu-id="657d5-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="657d5-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="657d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="657d5-102">SYNOPSIS</span></span>
<span data-ttu-id="657d5-103">Hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="657d5-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="657d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="657d5-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="657d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="657d5-105">DESCRIPTION</span></span>
<span data-ttu-id="657d5-106">Cmdleten **Get-AzureRmVMExtensionImageType** hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="657d5-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="657d5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="657d5-107">EXAMPLES</span></span>

### <span data-ttu-id="657d5-108">Exempel 1: Hämta en bild av typen tillägg</span><span class="sxs-lookup"><span data-stu-id="657d5-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="657d5-109">Det här kommandot får bild typen tillägg för angiven utgivare och plats.</span><span class="sxs-lookup"><span data-stu-id="657d5-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="657d5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="657d5-110">PARAMETERS</span></span>

### <span data-ttu-id="657d5-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="657d5-111">-Location</span></span>
<span data-ttu-id="657d5-112">Anger platsen för ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="657d5-112">Specifies the location of an extension.</span></span>
<span data-ttu-id="657d5-113">Denna cmdlet får typen för ett tillägg på den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="657d5-113">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="657d5-114">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="657d5-114">-PublisherName</span></span>
<span data-ttu-id="657d5-115">Anger namnet på en utgivare av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="657d5-115">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="657d5-116">Använd Get-AzureRmVMImagePublisher cmdlet för att få en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="657d5-116">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="657d5-117">Denna cmdlet får typen för ett tillägg från den utgivare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="657d5-117">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="657d5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="657d5-118">CommonParameters</span></span>
<span data-ttu-id="657d5-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="657d5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="657d5-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="657d5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="657d5-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="657d5-121">INPUTS</span></span>

### <span data-ttu-id="657d5-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="657d5-122">None</span></span>
<span data-ttu-id="657d5-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="657d5-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="657d5-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="657d5-124">OUTPUTS</span></span>

## <span data-ttu-id="657d5-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="657d5-125">NOTES</span></span>

## <span data-ttu-id="657d5-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="657d5-126">RELATED LINKS</span></span>

[<span data-ttu-id="657d5-127">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="657d5-127">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="657d5-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="657d5-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


