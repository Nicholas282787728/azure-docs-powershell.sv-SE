---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
ms.openlocfilehash: 1faae0848a96595e71ba96c20f2df9df59cd7ef0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930741"
---
# <span data-ttu-id="fc283-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fc283-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="fc283-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc283-102">SYNOPSIS</span></span>
<span data-ttu-id="fc283-103">Hämtar VMImage-utgivaren.</span><span class="sxs-lookup"><span data-stu-id="fc283-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc283-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc283-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc283-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc283-105">DESCRIPTION</span></span>
<span data-ttu-id="fc283-106">Cmdleten **Get-AzureRmVMImagePublisher** får VMImage-utgivaren.</span><span class="sxs-lookup"><span data-stu-id="fc283-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="fc283-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc283-107">EXAMPLES</span></span>

### <span data-ttu-id="fc283-108">Exempel 1: skaffa VMImage-utgivare för en region</span><span class="sxs-lookup"><span data-stu-id="fc283-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="fc283-109">Det här kommandot får utgivare av VMImage-instanser för området Central USA i din Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="fc283-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="fc283-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc283-110">PARAMETERS</span></span>

### <span data-ttu-id="fc283-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc283-111">-DefaultProfile</span></span>
<span data-ttu-id="fc283-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc283-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc283-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="fc283-113">-Location</span></span>
<span data-ttu-id="fc283-114">Anger platsen för VMImage.</span><span class="sxs-lookup"><span data-stu-id="fc283-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="fc283-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc283-115">CommonParameters</span></span>
<span data-ttu-id="fc283-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc283-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc283-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc283-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc283-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc283-118">INPUTS</span></span>

### <span data-ttu-id="fc283-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="fc283-119">None</span></span>
<span data-ttu-id="fc283-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="fc283-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fc283-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc283-121">OUTPUTS</span></span>

### <span data-ttu-id="fc283-122">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fc283-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="fc283-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc283-123">NOTES</span></span>

## <span data-ttu-id="fc283-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc283-124">RELATED LINKS</span></span>

[<span data-ttu-id="fc283-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fc283-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="fc283-126">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="fc283-126">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="fc283-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fc283-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="fc283-128">Spara – AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fc283-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


