---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: f299d0f299eaef61ba3655e8ec221cc55f5ab578
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757709"
---
# <span data-ttu-id="7fdbe-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7fdbe-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="7fdbe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fdbe-102">SYNOPSIS</span></span>
<span data-ttu-id="7fdbe-103">Hämtar VMImage-utgivaren.</span><span class="sxs-lookup"><span data-stu-id="7fdbe-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fdbe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fdbe-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [<CommonParameters>]
```

## <span data-ttu-id="7fdbe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fdbe-105">DESCRIPTION</span></span>
<span data-ttu-id="7fdbe-106">Cmdleten **Get-AzureRmVMImagePublisher** får VMImage-utgivaren.</span><span class="sxs-lookup"><span data-stu-id="7fdbe-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="7fdbe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fdbe-107">EXAMPLES</span></span>

### <span data-ttu-id="7fdbe-108">Exempel 1: skaffa VMImage-utgivare för en region</span><span class="sxs-lookup"><span data-stu-id="7fdbe-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="7fdbe-109">Det här kommandot får utgivare av VMImage-instanser för området Central USA i din Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="7fdbe-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="7fdbe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fdbe-110">PARAMETERS</span></span>

### <span data-ttu-id="7fdbe-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="7fdbe-111">-Location</span></span>
<span data-ttu-id="7fdbe-112">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="7fdbe-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="7fdbe-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fdbe-113">CommonParameters</span></span>
<span data-ttu-id="7fdbe-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fdbe-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fdbe-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fdbe-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fdbe-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fdbe-116">INPUTS</span></span>

### <span data-ttu-id="7fdbe-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="7fdbe-117">None</span></span>
<span data-ttu-id="7fdbe-118">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7fdbe-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7fdbe-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fdbe-119">OUTPUTS</span></span>

## <span data-ttu-id="7fdbe-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fdbe-120">NOTES</span></span>

## <span data-ttu-id="7fdbe-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fdbe-121">RELATED LINKS</span></span>

[<span data-ttu-id="7fdbe-122">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7fdbe-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="7fdbe-123">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7fdbe-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="7fdbe-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7fdbe-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="7fdbe-125">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7fdbe-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


