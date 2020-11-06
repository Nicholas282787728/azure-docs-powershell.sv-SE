---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: 5588d320d63a298fab632ea55d7c3b6c2220db85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573725"
---
# <span data-ttu-id="5f2e7-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="5f2e7-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="5f2e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="5f2e7-103">Får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f2e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f2e7-104">SYNTAX</span></span>

### <span data-ttu-id="5f2e7-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="5f2e7-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f2e7-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="5f2e7-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f2e7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f2e7-107">DESCRIPTION</span></span>
<span data-ttu-id="5f2e7-108">Cmdleten **Get-AzureRmVMImage** får alla versioner av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="5f2e7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f2e7-109">EXAMPLES</span></span>

### <span data-ttu-id="5f2e7-110">Exempel 1: skaffa VMImage-objekt</span><span class="sxs-lookup"><span data-stu-id="5f2e7-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="5f2e7-111">Det här kommandot får alla versioner av VMImage som matchar de angivna värdena.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="5f2e7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f2e7-112">PARAMETERS</span></span>

### <span data-ttu-id="5f2e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f2e7-113">-DefaultProfile</span></span>
<span data-ttu-id="5f2e7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f2e7-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="5f2e7-115">-FilterExpression</span></span>
<span data-ttu-id="5f2e7-116">Anger ett filter uttryck.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-116">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f2e7-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="5f2e7-117">-Location</span></span>
<span data-ttu-id="5f2e7-118">Anger platsen för en VMImage.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="5f2e7-119">-Ge</span><span class="sxs-lookup"><span data-stu-id="5f2e7-119">-Offer</span></span>
<span data-ttu-id="5f2e7-120">Anger typen av VMImage-offer.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="5f2e7-121">För att få ett bild utbud, Använd cmdleten Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="5f2e7-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="5f2e7-122">-PublisherName</span></span>
<span data-ttu-id="5f2e7-123">Anger utgivaren av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="5f2e7-124">Använd Get-AzureRmVMImagePublisher cmdlet för att få en bild utgivare.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="5f2e7-125">-SKU: er</span><span class="sxs-lookup"><span data-stu-id="5f2e7-125">-Skus</span></span>
<span data-ttu-id="5f2e7-126">Anger en VMImage-SKU.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="5f2e7-127">För att skaffa en SKU, Använd cmdleten Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="5f2e7-128">-Version</span><span class="sxs-lookup"><span data-stu-id="5f2e7-128">-Version</span></span>
<span data-ttu-id="5f2e7-129">Anger versionen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-129">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f2e7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f2e7-130">CommonParameters</span></span>
<span data-ttu-id="5f2e7-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f2e7-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f2e7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f2e7-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f2e7-133">INPUTS</span></span>

## <span data-ttu-id="5f2e7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f2e7-134">OUTPUTS</span></span>

## <span data-ttu-id="5f2e7-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f2e7-135">NOTES</span></span>

## <span data-ttu-id="5f2e7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f2e7-136">RELATED LINKS</span></span>

[<span data-ttu-id="5f2e7-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="5f2e7-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="5f2e7-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="5f2e7-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="5f2e7-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="5f2e7-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="5f2e7-140">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="5f2e7-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


