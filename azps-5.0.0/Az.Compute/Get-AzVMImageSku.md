---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269482"
---
# <span data-ttu-id="2b129-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2b129-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="2b129-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b129-102">SYNOPSIS</span></span>
<span data-ttu-id="2b129-103">Får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="2b129-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="2b129-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b129-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b129-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b129-105">DESCRIPTION</span></span>
<span data-ttu-id="2b129-106">Cmdleten **Get-AzVMImageSku** får VMImage SKU: er.</span><span class="sxs-lookup"><span data-stu-id="2b129-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="2b129-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b129-107">EXAMPLES</span></span>

### <span data-ttu-id="2b129-108">Exempel 1: skaffa VMImage SKU: er</span><span class="sxs-lookup"><span data-stu-id="2b129-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="2b129-109">Det här kommandot får SKU: erna för den angivna utgivaren och anbudet.</span><span class="sxs-lookup"><span data-stu-id="2b129-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="2b129-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b129-110">PARAMETERS</span></span>

### <span data-ttu-id="2b129-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b129-111">-DefaultProfile</span></span>
<span data-ttu-id="2b129-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b129-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b129-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="2b129-113">-Location</span></span>
<span data-ttu-id="2b129-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="2b129-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="2b129-115">-Ge</span><span class="sxs-lookup"><span data-stu-id="2b129-115">-Offer</span></span>
<span data-ttu-id="2b129-116">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="2b129-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="2b129-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="2b129-117">-PublisherName</span></span>
<span data-ttu-id="2b129-118">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="2b129-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="2b129-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b129-119">CommonParameters</span></span>
<span data-ttu-id="2b129-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b129-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b129-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b129-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b129-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b129-122">INPUTS</span></span>

### <span data-ttu-id="2b129-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2b129-123">System.String</span></span>

## <span data-ttu-id="2b129-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b129-124">OUTPUTS</span></span>

### <span data-ttu-id="2b129-125">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="2b129-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="2b129-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b129-126">NOTES</span></span>

## <span data-ttu-id="2b129-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b129-127">RELATED LINKS</span></span>

[<span data-ttu-id="2b129-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2b129-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="2b129-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="2b129-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="2b129-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2b129-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="2b129-131">Spara – AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2b129-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


