---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 6355ce5cea881f66473ca8d541585187a79fe23e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917418"
---
# <span data-ttu-id="3b77d-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="3b77d-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="3b77d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b77d-102">SYNOPSIS</span></span>
<span data-ttu-id="3b77d-103">Får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="3b77d-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="3b77d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b77d-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b77d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b77d-105">DESCRIPTION</span></span>
<span data-ttu-id="3b77d-106">Cmdleten **Get-AzVMImageSku** får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="3b77d-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="3b77d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b77d-107">EXAMPLES</span></span>

### <span data-ttu-id="3b77d-108">Exempel 1: skaffa VMImage SKU: er</span><span class="sxs-lookup"><span data-stu-id="3b77d-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="3b77d-109">Det här kommandot får SKU: erna för den angivna utgivaren och anbudet.</span><span class="sxs-lookup"><span data-stu-id="3b77d-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="3b77d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b77d-110">PARAMETERS</span></span>

### <span data-ttu-id="3b77d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b77d-111">-DefaultProfile</span></span>
<span data-ttu-id="3b77d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b77d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b77d-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="3b77d-113">-Location</span></span>
<span data-ttu-id="3b77d-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="3b77d-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="3b77d-115">-Ge</span><span class="sxs-lookup"><span data-stu-id="3b77d-115">-Offer</span></span>
<span data-ttu-id="3b77d-116">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="3b77d-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="3b77d-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3b77d-117">-PublisherName</span></span>
<span data-ttu-id="3b77d-118">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="3b77d-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="3b77d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b77d-119">CommonParameters</span></span>
<span data-ttu-id="3b77d-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b77d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b77d-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b77d-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b77d-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b77d-122">INPUTS</span></span>

### <span data-ttu-id="3b77d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3b77d-123">System.String</span></span>

## <span data-ttu-id="3b77d-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b77d-124">OUTPUTS</span></span>

### <span data-ttu-id="3b77d-125">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="3b77d-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="3b77d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b77d-126">NOTES</span></span>

## <span data-ttu-id="3b77d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b77d-127">RELATED LINKS</span></span>

[<span data-ttu-id="3b77d-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3b77d-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="3b77d-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="3b77d-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="3b77d-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3b77d-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="3b77d-131">Spara – AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3b77d-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


