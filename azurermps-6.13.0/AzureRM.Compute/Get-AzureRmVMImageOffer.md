---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: 66c0355af202c5900fddc60c81e92f2851ddc1ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578095"
---
# <span data-ttu-id="b16b4-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="b16b4-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="b16b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b16b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b16b4-103">Hämtar typer av VMImage-offerter.</span><span class="sxs-lookup"><span data-stu-id="b16b4-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b16b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b16b4-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b16b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b16b4-105">DESCRIPTION</span></span>
<span data-ttu-id="b16b4-106">Cmdleten **Get-AzureRmVMImageOffer** har typen VMImage-utbud.</span><span class="sxs-lookup"><span data-stu-id="b16b4-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="b16b4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b16b4-107">EXAMPLES</span></span>

### <span data-ttu-id="b16b4-108">Exempel 1: Hämta bud typer för en publicerare</span><span class="sxs-lookup"><span data-stu-id="b16b4-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="b16b4-109">Det här kommandot får utbuds typerna för den angivna utgivaren i det centrala USA-området.</span><span class="sxs-lookup"><span data-stu-id="b16b4-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="b16b4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b16b4-110">PARAMETERS</span></span>

### <span data-ttu-id="b16b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16b4-111">-DefaultProfile</span></span>
<span data-ttu-id="b16b4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b16b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b16b4-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="b16b4-113">-Location</span></span>
<span data-ttu-id="b16b4-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="b16b4-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="b16b4-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b16b4-115">-PublisherName</span></span>
<span data-ttu-id="b16b4-116">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="b16b4-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="b16b4-117">Använd Get-AzureRmVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="b16b4-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="b16b4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16b4-118">CommonParameters</span></span>
<span data-ttu-id="b16b4-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b16b4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16b4-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b16b4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16b4-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b16b4-121">INPUTS</span></span>

### <span data-ttu-id="b16b4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b16b4-122">System.String</span></span>

## <span data-ttu-id="b16b4-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b16b4-123">OUTPUTS</span></span>

### <span data-ttu-id="b16b4-124">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="b16b4-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="b16b4-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b16b4-125">NOTES</span></span>

## <span data-ttu-id="b16b4-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b16b4-126">RELATED LINKS</span></span>

[<span data-ttu-id="b16b4-127">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b16b4-127">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="b16b4-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b16b4-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="b16b4-129">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="b16b4-129">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="b16b4-130">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b16b4-130">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


