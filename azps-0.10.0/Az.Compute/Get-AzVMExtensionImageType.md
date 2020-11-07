---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 6a342143c8117bca1da5165ecb5a285ee6c0b686
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925166"
---
# <span data-ttu-id="6711b-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="6711b-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="6711b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6711b-102">SYNOPSIS</span></span>
<span data-ttu-id="6711b-103">Hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="6711b-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="6711b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6711b-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6711b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6711b-105">DESCRIPTION</span></span>
<span data-ttu-id="6711b-106">Cmdleten **Get-AzVMExtensionImageType** hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="6711b-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="6711b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6711b-107">EXAMPLES</span></span>

### <span data-ttu-id="6711b-108">Exempel 1: Hämta en bild av typen tillägg</span><span class="sxs-lookup"><span data-stu-id="6711b-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="6711b-109">Det här kommandot får bild typen tillägg för angiven utgivare och plats.</span><span class="sxs-lookup"><span data-stu-id="6711b-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="6711b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6711b-110">PARAMETERS</span></span>

### <span data-ttu-id="6711b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6711b-111">-DefaultProfile</span></span>
<span data-ttu-id="6711b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6711b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6711b-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="6711b-113">-Location</span></span>
<span data-ttu-id="6711b-114">Anger platsen för ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="6711b-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="6711b-115">Denna cmdlet får typen för ett tillägg på den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6711b-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="6711b-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="6711b-116">-PublisherName</span></span>
<span data-ttu-id="6711b-117">Anger namnet på en utgivare av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="6711b-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="6711b-118">Använd Get-AzVMImagePublisher cmdlet för att få en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="6711b-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="6711b-119">Denna cmdlet får typen för ett tillägg från den utgivare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6711b-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="6711b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6711b-120">CommonParameters</span></span>
<span data-ttu-id="6711b-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6711b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6711b-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6711b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6711b-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6711b-123">INPUTS</span></span>

### <span data-ttu-id="6711b-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="6711b-124">None</span></span>
<span data-ttu-id="6711b-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6711b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6711b-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6711b-126">OUTPUTS</span></span>

### <span data-ttu-id="6711b-127">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="6711b-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="6711b-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6711b-128">NOTES</span></span>

## <span data-ttu-id="6711b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6711b-129">RELATED LINKS</span></span>

[<span data-ttu-id="6711b-130">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="6711b-130">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="6711b-131">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6711b-131">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


