---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: 109f55c1afc1c00d26c47d0131d098158010bd70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93586636"
---
# <span data-ttu-id="51f3d-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="51f3d-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="51f3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="51f3d-103">Hämtar VMImage-utgivaren.</span><span class="sxs-lookup"><span data-stu-id="51f3d-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51f3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51f3d-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51f3d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51f3d-105">DESCRIPTION</span></span>
<span data-ttu-id="51f3d-106">Cmdleten **Get-AzureRmVMImagePublisher** får VMImage-utgivaren.</span><span class="sxs-lookup"><span data-stu-id="51f3d-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="51f3d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51f3d-107">EXAMPLES</span></span>

### <span data-ttu-id="51f3d-108">Exempel 1: skaffa VMImage-utgivare för en region</span><span class="sxs-lookup"><span data-stu-id="51f3d-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="51f3d-109">Det här kommandot får utgivare av VMImage-instanser för området Central USA i din Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="51f3d-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="51f3d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51f3d-110">PARAMETERS</span></span>

### <span data-ttu-id="51f3d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f3d-111">-DefaultProfile</span></span>
<span data-ttu-id="51f3d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51f3d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51f3d-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="51f3d-113">-Location</span></span>
<span data-ttu-id="51f3d-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="51f3d-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="51f3d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f3d-115">CommonParameters</span></span>
<span data-ttu-id="51f3d-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f3d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f3d-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f3d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f3d-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51f3d-118">INPUTS</span></span>

### <span data-ttu-id="51f3d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="51f3d-119">System.String</span></span>

## <span data-ttu-id="51f3d-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51f3d-120">OUTPUTS</span></span>

### <span data-ttu-id="51f3d-121">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="51f3d-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="51f3d-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51f3d-122">NOTES</span></span>

## <span data-ttu-id="51f3d-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51f3d-123">RELATED LINKS</span></span>

[<span data-ttu-id="51f3d-124">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="51f3d-124">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="51f3d-125">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="51f3d-125">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="51f3d-126">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="51f3d-126">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="51f3d-127">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="51f3d-127">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


