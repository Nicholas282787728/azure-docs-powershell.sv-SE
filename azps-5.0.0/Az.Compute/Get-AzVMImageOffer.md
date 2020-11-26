---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270860"
---
# <span data-ttu-id="b3f5c-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="b3f5c-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="b3f5c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f5c-103">Hämtar typer av VMImage-offerter.</span><span class="sxs-lookup"><span data-stu-id="b3f5c-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="b3f5c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3f5c-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3f5c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3f5c-105">DESCRIPTION</span></span>
<span data-ttu-id="b3f5c-106">Cmdleten **Get-AzVMImageOffer** har typen VMImage-utbud.</span><span class="sxs-lookup"><span data-stu-id="b3f5c-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="b3f5c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3f5c-107">EXAMPLES</span></span>

### <span data-ttu-id="b3f5c-108">Exempel 1: Hämta bud typer för en publicerare</span><span class="sxs-lookup"><span data-stu-id="b3f5c-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="b3f5c-109">Det här kommandot får utbuds typerna för den angivna utgivaren i det centrala USA-området.</span><span class="sxs-lookup"><span data-stu-id="b3f5c-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="b3f5c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3f5c-110">PARAMETERS</span></span>

### <span data-ttu-id="b3f5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f5c-111">-DefaultProfile</span></span>
<span data-ttu-id="b3f5c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f5c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3f5c-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="b3f5c-113">-Location</span></span>
<span data-ttu-id="b3f5c-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="b3f5c-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="b3f5c-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b3f5c-115">-PublisherName</span></span>
<span data-ttu-id="b3f5c-116">Anger namnet på en utgivare av en VMImage.</span><span class="sxs-lookup"><span data-stu-id="b3f5c-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="b3f5c-117">Använd Get-AzVMImagePublisher cmdlet för att få en utgivare.</span><span class="sxs-lookup"><span data-stu-id="b3f5c-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="b3f5c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f5c-118">CommonParameters</span></span>
<span data-ttu-id="b3f5c-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3f5c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f5c-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3f5c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f5c-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3f5c-121">INPUTS</span></span>

### <span data-ttu-id="b3f5c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b3f5c-122">System.String</span></span>

## <span data-ttu-id="b3f5c-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3f5c-123">OUTPUTS</span></span>

### <span data-ttu-id="b3f5c-124">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="b3f5c-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="b3f5c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3f5c-125">NOTES</span></span>

## <span data-ttu-id="b3f5c-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3f5c-126">RELATED LINKS</span></span>

[<span data-ttu-id="b3f5c-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b3f5c-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="b3f5c-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b3f5c-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="b3f5c-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="b3f5c-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="b3f5c-130">Spara – AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b3f5c-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)

