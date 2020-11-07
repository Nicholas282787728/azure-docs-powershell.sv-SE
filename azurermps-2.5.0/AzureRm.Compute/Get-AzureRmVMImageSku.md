---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
ms.openlocfilehash: 8d2253e20e87a0e6a5d97f2dd0e405412f5a9282
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930737"
---
# <span data-ttu-id="3c744-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="3c744-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="3c744-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c744-102">SYNOPSIS</span></span>
<span data-ttu-id="3c744-103">Får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="3c744-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c744-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c744-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c744-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c744-105">DESCRIPTION</span></span>
<span data-ttu-id="3c744-106">Cmdleten **Get-AzureRmVMImageSku** får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="3c744-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="3c744-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c744-107">EXAMPLES</span></span>

### <span data-ttu-id="3c744-108">Exempel 1: skaffa VMImage SKU: er</span><span class="sxs-lookup"><span data-stu-id="3c744-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="3c744-109">Det här kommandot får SKU: erna för den angivna utgivaren och anbudet.</span><span class="sxs-lookup"><span data-stu-id="3c744-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="3c744-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c744-110">PARAMETERS</span></span>

### <span data-ttu-id="3c744-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c744-111">-DefaultProfile</span></span>
<span data-ttu-id="3c744-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c744-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c744-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="3c744-113">-Location</span></span>
<span data-ttu-id="3c744-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="3c744-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="3c744-115">-Ge</span><span class="sxs-lookup"><span data-stu-id="3c744-115">-Offer</span></span>
<span data-ttu-id="3c744-116">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="3c744-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="3c744-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3c744-117">-PublisherName</span></span>
<span data-ttu-id="3c744-118">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="3c744-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="3c744-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c744-119">CommonParameters</span></span>
<span data-ttu-id="3c744-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c744-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c744-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c744-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c744-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c744-122">INPUTS</span></span>

### <span data-ttu-id="3c744-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="3c744-123">None</span></span>
<span data-ttu-id="3c744-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3c744-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c744-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c744-125">OUTPUTS</span></span>

### <span data-ttu-id="3c744-126">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="3c744-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="3c744-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c744-127">NOTES</span></span>

## <span data-ttu-id="3c744-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c744-128">RELATED LINKS</span></span>

[<span data-ttu-id="3c744-129">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3c744-129">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="3c744-130">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="3c744-130">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="3c744-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3c744-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="3c744-132">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3c744-132">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


