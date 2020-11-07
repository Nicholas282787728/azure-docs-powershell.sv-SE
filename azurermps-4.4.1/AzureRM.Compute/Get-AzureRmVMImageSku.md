---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 5bdce17c963cc2529fab3f328b9ab64cc549e1d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758427"
---
# <span data-ttu-id="4297a-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4297a-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="4297a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4297a-102">SYNOPSIS</span></span>
<span data-ttu-id="4297a-103">Får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="4297a-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4297a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4297a-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4297a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4297a-105">DESCRIPTION</span></span>
<span data-ttu-id="4297a-106">Cmdleten **Get-AzureRmVMImageSku** får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="4297a-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="4297a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4297a-107">EXAMPLES</span></span>

### <span data-ttu-id="4297a-108">Exempel 1: skaffa VMImage SKU: er</span><span class="sxs-lookup"><span data-stu-id="4297a-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="4297a-109">Det här kommandot får SKU: erna för den angivna utgivaren och anbudet.</span><span class="sxs-lookup"><span data-stu-id="4297a-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="4297a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4297a-110">PARAMETERS</span></span>

### <span data-ttu-id="4297a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4297a-111">-DefaultProfile</span></span>
<span data-ttu-id="4297a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4297a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4297a-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="4297a-113">-Location</span></span>
<span data-ttu-id="4297a-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="4297a-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="4297a-115">-Ge</span><span class="sxs-lookup"><span data-stu-id="4297a-115">-Offer</span></span>
<span data-ttu-id="4297a-116">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="4297a-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="4297a-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4297a-117">-PublisherName</span></span>
<span data-ttu-id="4297a-118">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="4297a-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="4297a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4297a-119">CommonParameters</span></span>
<span data-ttu-id="4297a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4297a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4297a-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4297a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4297a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4297a-122">INPUTS</span></span>

## <span data-ttu-id="4297a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4297a-123">OUTPUTS</span></span>

## <span data-ttu-id="4297a-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4297a-124">NOTES</span></span>

## <span data-ttu-id="4297a-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4297a-125">RELATED LINKS</span></span>

[<span data-ttu-id="4297a-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4297a-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4297a-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4297a-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="4297a-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4297a-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4297a-129">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4297a-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


