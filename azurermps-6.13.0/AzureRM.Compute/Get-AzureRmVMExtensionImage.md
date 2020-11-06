---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: 4a348d4e3aa6089ae3e8f3c0bdf871156111ce93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586351"
---
# <span data-ttu-id="4d206-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="4d206-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="4d206-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d206-102">SYNOPSIS</span></span>
<span data-ttu-id="4d206-103">Hämtar alla versioner för ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="4d206-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d206-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d206-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d206-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d206-105">DESCRIPTION</span></span>
<span data-ttu-id="4d206-106">Cmdleten **Get-AzureRmVMExtensionImage** hämtar alla versioner av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="4d206-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="4d206-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d206-107">EXAMPLES</span></span>

### <span data-ttu-id="4d206-108">Exempel 1: Hämta versionerna av en tilläggs bild</span><span class="sxs-lookup"><span data-stu-id="4d206-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="4d206-109">Det här kommandot får alla versioner av tilläggs bilden för den angivna platsen, utgivaren och typen.</span><span class="sxs-lookup"><span data-stu-id="4d206-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="4d206-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d206-110">PARAMETERS</span></span>

### <span data-ttu-id="4d206-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d206-111">-DefaultProfile</span></span>
<span data-ttu-id="4d206-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d206-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d206-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="4d206-113">-FilterExpression</span></span>
<span data-ttu-id="4d206-114">Anger ett filter uttryck.</span><span class="sxs-lookup"><span data-stu-id="4d206-114">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d206-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="4d206-115">-Location</span></span>
<span data-ttu-id="4d206-116">Anger platsen för ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="4d206-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="4d206-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4d206-117">-PublisherName</span></span>
<span data-ttu-id="4d206-118">Anger namnet på en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="4d206-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="4d206-119">Använd Get-AzureRmVMImagePublisher cmdlet för att få en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="4d206-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4d206-120">– Skriv</span><span class="sxs-lookup"><span data-stu-id="4d206-120">-Type</span></span>
<span data-ttu-id="4d206-121">Anger typen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="4d206-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="4d206-122">För att få en tilläggs typ, Använd cmdleten Get-AzureRmVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="4d206-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="4d206-123">-Version</span><span class="sxs-lookup"><span data-stu-id="4d206-123">-Version</span></span>
<span data-ttu-id="4d206-124">Anger vilken version av tillägget som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="4d206-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d206-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d206-125">CommonParameters</span></span>
<span data-ttu-id="4d206-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d206-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d206-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d206-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d206-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d206-128">INPUTS</span></span>

### <span data-ttu-id="4d206-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4d206-129">System.String</span></span>

## <span data-ttu-id="4d206-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d206-130">OUTPUTS</span></span>

### <span data-ttu-id="4d206-131">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="4d206-131">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="4d206-132">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="4d206-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="4d206-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d206-133">NOTES</span></span>

## <span data-ttu-id="4d206-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d206-134">RELATED LINKS</span></span>

[<span data-ttu-id="4d206-135">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="4d206-135">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="4d206-136">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4d206-136">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4d206-137">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4d206-137">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


