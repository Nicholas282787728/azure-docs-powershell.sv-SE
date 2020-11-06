---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: bae8fb04e71700d1572b8742f8cccbb2ebe8e331
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574364"
---
# <span data-ttu-id="6bc5f-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="6bc5f-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="6bc5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6bc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc5f-103">Hämtar alla versioner för ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bc5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6bc5f-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [<CommonParameters>]
```

## <span data-ttu-id="6bc5f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6bc5f-105">DESCRIPTION</span></span>
<span data-ttu-id="6bc5f-106">Cmdleten **Get-AzureRmVMExtensionImage** hämtar alla versioner av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="6bc5f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6bc5f-107">EXAMPLES</span></span>

### <span data-ttu-id="6bc5f-108">Exempel 1: Hämta versionerna av en tilläggs bild</span><span class="sxs-lookup"><span data-stu-id="6bc5f-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="6bc5f-109">Det här kommandot får alla versioner av tilläggs bilden för den angivna platsen, utgivaren och typen.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="6bc5f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6bc5f-110">PARAMETERS</span></span>

### <span data-ttu-id="6bc5f-111">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="6bc5f-111">-FilterExpression</span></span>
<span data-ttu-id="6bc5f-112">Anger ett filter uttryck.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-112">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc5f-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="6bc5f-113">-Location</span></span>
<span data-ttu-id="6bc5f-114">Anger platsen för ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-114">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="6bc5f-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="6bc5f-115">-PublisherName</span></span>
<span data-ttu-id="6bc5f-116">Anger namnet på en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-116">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="6bc5f-117">Använd Get-AzureRmVMImagePublisher cmdlet för att få en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-117">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="6bc5f-118">– Skriv</span><span class="sxs-lookup"><span data-stu-id="6bc5f-118">-Type</span></span>
<span data-ttu-id="6bc5f-119">Anger typen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-119">Specifies the type of the extension.</span></span>
<span data-ttu-id="6bc5f-120">För att få en tilläggs typ, Använd cmdleten Get-AzureRmVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-120">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="6bc5f-121">-Version</span><span class="sxs-lookup"><span data-stu-id="6bc5f-121">-Version</span></span>
<span data-ttu-id="6bc5f-122">Anger vilken version av tillägget som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-122">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc5f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc5f-123">CommonParameters</span></span>
<span data-ttu-id="6bc5f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc5f-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bc5f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc5f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6bc5f-126">INPUTS</span></span>

### <span data-ttu-id="6bc5f-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="6bc5f-127">None</span></span>
<span data-ttu-id="6bc5f-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6bc5f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6bc5f-129">OUTPUTS</span></span>

## <span data-ttu-id="6bc5f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6bc5f-130">NOTES</span></span>

## <span data-ttu-id="6bc5f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6bc5f-131">RELATED LINKS</span></span>

[<span data-ttu-id="6bc5f-132">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="6bc5f-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="6bc5f-133">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6bc5f-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="6bc5f-134">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6bc5f-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


