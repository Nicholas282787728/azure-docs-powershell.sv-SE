---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: eb31437870a77e4af84bdcb94ffa4172d117c78d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757803"
---
# <span data-ttu-id="bc38e-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="bc38e-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="bc38e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc38e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc38e-103">Hämtar typer av VMImage-offerter.</span><span class="sxs-lookup"><span data-stu-id="bc38e-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc38e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc38e-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc38e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc38e-105">DESCRIPTION</span></span>
<span data-ttu-id="bc38e-106">Cmdleten **Get-AzureRmVMImageOffer** har typen VMImage-utbud.</span><span class="sxs-lookup"><span data-stu-id="bc38e-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="bc38e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc38e-107">EXAMPLES</span></span>

### <span data-ttu-id="bc38e-108">Exempel 1: Hämta bud typer för en publicerare</span><span class="sxs-lookup"><span data-stu-id="bc38e-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="bc38e-109">Det här kommandot får utbuds typerna för den angivna utgivaren i det centrala USA-området.</span><span class="sxs-lookup"><span data-stu-id="bc38e-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="bc38e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc38e-110">PARAMETERS</span></span>

### <span data-ttu-id="bc38e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc38e-111">-DefaultProfile</span></span>
<span data-ttu-id="bc38e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bc38e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc38e-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="bc38e-113">-Location</span></span>
<span data-ttu-id="bc38e-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="bc38e-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="bc38e-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="bc38e-115">-PublisherName</span></span>
<span data-ttu-id="bc38e-116">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="bc38e-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="bc38e-117">Använd Get-AzureRmVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="bc38e-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="bc38e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc38e-118">CommonParameters</span></span>
<span data-ttu-id="bc38e-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc38e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc38e-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc38e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc38e-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc38e-121">INPUTS</span></span>

## <span data-ttu-id="bc38e-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc38e-122">OUTPUTS</span></span>

## <span data-ttu-id="bc38e-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc38e-123">NOTES</span></span>

## <span data-ttu-id="bc38e-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc38e-124">RELATED LINKS</span></span>

[<span data-ttu-id="bc38e-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="bc38e-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="bc38e-126">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="bc38e-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="bc38e-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="bc38e-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="bc38e-128">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="bc38e-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


