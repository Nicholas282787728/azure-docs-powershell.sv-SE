---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: fad6c42c53e475343ad518c89dbb1a918a0f1e68
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925158"
---
# <span data-ttu-id="16ee3-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="16ee3-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="16ee3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="16ee3-103">Får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="16ee3-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="16ee3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16ee3-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16ee3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16ee3-105">DESCRIPTION</span></span>
<span data-ttu-id="16ee3-106">Cmdleten **Get-AzVMImageSku** får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="16ee3-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="16ee3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16ee3-107">EXAMPLES</span></span>

### <span data-ttu-id="16ee3-108">Exempel 1: skaffa VMImage SKU: er</span><span class="sxs-lookup"><span data-stu-id="16ee3-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="16ee3-109">Det här kommandot får SKU: erna för den angivna utgivaren och anbudet.</span><span class="sxs-lookup"><span data-stu-id="16ee3-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="16ee3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16ee3-110">PARAMETERS</span></span>

### <span data-ttu-id="16ee3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ee3-111">-DefaultProfile</span></span>
<span data-ttu-id="16ee3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16ee3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16ee3-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="16ee3-113">-Location</span></span>
<span data-ttu-id="16ee3-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="16ee3-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="16ee3-115">-Ge</span><span class="sxs-lookup"><span data-stu-id="16ee3-115">-Offer</span></span>
<span data-ttu-id="16ee3-116">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="16ee3-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="16ee3-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="16ee3-117">-PublisherName</span></span>
<span data-ttu-id="16ee3-118">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="16ee3-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="16ee3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ee3-119">CommonParameters</span></span>
<span data-ttu-id="16ee3-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ee3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ee3-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ee3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ee3-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16ee3-122">INPUTS</span></span>

### <span data-ttu-id="16ee3-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="16ee3-123">None</span></span>
<span data-ttu-id="16ee3-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="16ee3-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16ee3-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16ee3-125">OUTPUTS</span></span>

### <span data-ttu-id="16ee3-126">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="16ee3-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="16ee3-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16ee3-127">NOTES</span></span>

## <span data-ttu-id="16ee3-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16ee3-128">RELATED LINKS</span></span>

[<span data-ttu-id="16ee3-129">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="16ee3-129">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="16ee3-130">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="16ee3-130">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="16ee3-131">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="16ee3-131">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="16ee3-132">Spara – AzVMImage</span><span class="sxs-lookup"><span data-stu-id="16ee3-132">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


