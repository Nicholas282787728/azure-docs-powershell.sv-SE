---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: c4af2c651438659508e231bf2710e88de19830cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578103"
---
# <span data-ttu-id="5a979-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="5a979-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="5a979-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a979-102">SYNOPSIS</span></span>
<span data-ttu-id="5a979-103">Hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="5a979-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a979-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a979-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a979-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a979-105">DESCRIPTION</span></span>
<span data-ttu-id="5a979-106">Cmdleten **Get-AzureRmVMExtensionImageType** hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="5a979-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="5a979-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a979-107">EXAMPLES</span></span>

### <span data-ttu-id="5a979-108">Exempel 1: Hämta en bild av typen tillägg</span><span class="sxs-lookup"><span data-stu-id="5a979-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="5a979-109">Det här kommandot får bild typen tillägg för angiven utgivare och plats.</span><span class="sxs-lookup"><span data-stu-id="5a979-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="5a979-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a979-110">PARAMETERS</span></span>

### <span data-ttu-id="5a979-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a979-111">-DefaultProfile</span></span>
<span data-ttu-id="5a979-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a979-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a979-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="5a979-113">-Location</span></span>
<span data-ttu-id="5a979-114">Anger platsen för ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="5a979-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="5a979-115">Denna cmdlet får typen för ett tillägg på den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5a979-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a979-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="5a979-116">-PublisherName</span></span>
<span data-ttu-id="5a979-117">Anger namnet på en utgivare av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="5a979-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="5a979-118">Använd Get-AzureRmVMImagePublisher cmdlet för att få en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="5a979-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="5a979-119">Denna cmdlet får typen för ett tillägg från den utgivare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5a979-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a979-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a979-120">CommonParameters</span></span>
<span data-ttu-id="5a979-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a979-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a979-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a979-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a979-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a979-123">INPUTS</span></span>

### <span data-ttu-id="5a979-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5a979-124">System.String</span></span>

## <span data-ttu-id="5a979-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a979-125">OUTPUTS</span></span>

### <span data-ttu-id="5a979-126">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="5a979-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="5a979-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a979-127">NOTES</span></span>

## <span data-ttu-id="5a979-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a979-128">RELATED LINKS</span></span>

[<span data-ttu-id="5a979-129">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="5a979-129">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="5a979-130">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="5a979-130">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

