---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: bd463ffad1c38265dbca894748d0c5b9a479fade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584792"
---
# <span data-ttu-id="1fc89-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1fc89-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="1fc89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fc89-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc89-103">Hämtar VMImage-utgivaren.</span><span class="sxs-lookup"><span data-stu-id="1fc89-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fc89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fc89-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fc89-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fc89-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc89-106">Cmdleten **Get-AzureRmVMImagePublisher** får VMImage-utgivaren.</span><span class="sxs-lookup"><span data-stu-id="1fc89-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="1fc89-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fc89-107">EXAMPLES</span></span>

### <span data-ttu-id="1fc89-108">Exempel 1: skaffa VMImage-utgivare för en region</span><span class="sxs-lookup"><span data-stu-id="1fc89-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="1fc89-109">Det här kommandot får utgivare av VMImage-instanser för området Central USA i din Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="1fc89-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="1fc89-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fc89-110">PARAMETERS</span></span>

### <span data-ttu-id="1fc89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc89-111">-DefaultProfile</span></span>
<span data-ttu-id="1fc89-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1fc89-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fc89-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="1fc89-113">-Location</span></span>
<span data-ttu-id="1fc89-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="1fc89-114">Specifies the location of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc89-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc89-115">CommonParameters</span></span>
<span data-ttu-id="1fc89-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc89-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc89-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc89-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc89-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fc89-118">INPUTS</span></span>

## <span data-ttu-id="1fc89-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fc89-119">OUTPUTS</span></span>

## <span data-ttu-id="1fc89-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fc89-120">NOTES</span></span>

## <span data-ttu-id="1fc89-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fc89-121">RELATED LINKS</span></span>

[<span data-ttu-id="1fc89-122">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1fc89-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="1fc89-123">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="1fc89-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="1fc89-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="1fc89-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="1fc89-125">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1fc89-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


