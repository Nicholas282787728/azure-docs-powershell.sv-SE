---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: c69474929fa91b2e4ae1c7f4e50d5961a9322f66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929958"
---
# <span data-ttu-id="f2b24-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f2b24-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="f2b24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2b24-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b24-103">Får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="f2b24-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2b24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2b24-104">SYNTAX</span></span>

### <span data-ttu-id="f2b24-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="f2b24-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2b24-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="f2b24-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2b24-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2b24-107">DESCRIPTION</span></span>
<span data-ttu-id="f2b24-108">Cmdleten **Get-AzureRmVMImage** får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="f2b24-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="f2b24-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2b24-109">EXAMPLES</span></span>

### <span data-ttu-id="f2b24-110">Exempel 1: skaffa VMImage-objekt</span><span class="sxs-lookup"><span data-stu-id="f2b24-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="f2b24-111">Det här kommandot får alla versioner av VMImage som matchar de angivna värdena.</span><span class="sxs-lookup"><span data-stu-id="f2b24-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="f2b24-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2b24-112">PARAMETERS</span></span>

### <span data-ttu-id="f2b24-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b24-113">-DefaultProfile</span></span>
<span data-ttu-id="f2b24-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b24-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2b24-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="f2b24-115">-FilterExpression</span></span>
<span data-ttu-id="f2b24-116">Anger ett filter uttryck.</span><span class="sxs-lookup"><span data-stu-id="f2b24-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="f2b24-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="f2b24-117">-Location</span></span>
<span data-ttu-id="f2b24-118">Anger platsen för en VMImage.</span><span class="sxs-lookup"><span data-stu-id="f2b24-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="f2b24-119">-Ge</span><span class="sxs-lookup"><span data-stu-id="f2b24-119">-Offer</span></span>
<span data-ttu-id="f2b24-120">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="f2b24-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="f2b24-121">För att få ett bild utbud, Använd cmdleten Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="f2b24-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="f2b24-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="f2b24-122">-PublisherName</span></span>
<span data-ttu-id="f2b24-123">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="f2b24-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="f2b24-124">Använd Get-AzureRmVMImagePublisher cmdlet för att få en bild utgivare.</span><span class="sxs-lookup"><span data-stu-id="f2b24-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="f2b24-125">-SKU: er</span><span class="sxs-lookup"><span data-stu-id="f2b24-125">-Skus</span></span>
<span data-ttu-id="f2b24-126">Anger en VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="f2b24-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="f2b24-127">För att skaffa en SKU, Använd cmdleten Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="f2b24-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="f2b24-128">-Version</span><span class="sxs-lookup"><span data-stu-id="f2b24-128">-Version</span></span>
<span data-ttu-id="f2b24-129">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="f2b24-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="f2b24-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b24-130">CommonParameters</span></span>
<span data-ttu-id="f2b24-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2b24-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b24-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b24-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b24-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2b24-133">INPUTS</span></span>

### <span data-ttu-id="f2b24-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="f2b24-134">None</span></span>
<span data-ttu-id="f2b24-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f2b24-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2b24-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2b24-136">OUTPUTS</span></span>

### <span data-ttu-id="f2b24-137">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="f2b24-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="f2b24-138">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="f2b24-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="f2b24-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2b24-139">NOTES</span></span>

## <span data-ttu-id="f2b24-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2b24-140">RELATED LINKS</span></span>

[<span data-ttu-id="f2b24-141">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f2b24-141">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="f2b24-142">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f2b24-142">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f2b24-143">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f2b24-143">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="f2b24-144">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f2b24-144">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


