---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: f2b0cd955cd63eb6066da43e8b468ab4ea9bb0bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917421"
---
# <span data-ttu-id="84e91-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="84e91-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="84e91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84e91-102">SYNOPSIS</span></span>
<span data-ttu-id="84e91-103">Hämtar VMImage-utgivaren.</span><span class="sxs-lookup"><span data-stu-id="84e91-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="84e91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84e91-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84e91-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84e91-105">DESCRIPTION</span></span>
<span data-ttu-id="84e91-106">Cmdleten **Get-AzVMImagePublisher** får VMImage-utgivaren.</span><span class="sxs-lookup"><span data-stu-id="84e91-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="84e91-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84e91-107">EXAMPLES</span></span>

### <span data-ttu-id="84e91-108">Exempel 1: skaffa VMImage-utgivare för en region</span><span class="sxs-lookup"><span data-stu-id="84e91-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="84e91-109">Det här kommandot får utgivare av VMImage-instanser för området Central USA i din Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="84e91-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="84e91-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84e91-110">PARAMETERS</span></span>

### <span data-ttu-id="84e91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e91-111">-DefaultProfile</span></span>
<span data-ttu-id="84e91-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84e91-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84e91-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="84e91-113">-Location</span></span>
<span data-ttu-id="84e91-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="84e91-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="84e91-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e91-115">CommonParameters</span></span>
<span data-ttu-id="84e91-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e91-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e91-117">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84e91-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e91-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84e91-118">INPUTS</span></span>

### <span data-ttu-id="84e91-119">System. String</span><span class="sxs-lookup"><span data-stu-id="84e91-119">System.String</span></span>

## <span data-ttu-id="84e91-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84e91-120">OUTPUTS</span></span>

### <span data-ttu-id="84e91-121">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="84e91-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="84e91-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84e91-122">NOTES</span></span>

## <span data-ttu-id="84e91-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84e91-123">RELATED LINKS</span></span>

[<span data-ttu-id="84e91-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="84e91-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="84e91-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="84e91-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="84e91-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="84e91-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="84e91-127">Spara – AzVMImage</span><span class="sxs-lookup"><span data-stu-id="84e91-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


