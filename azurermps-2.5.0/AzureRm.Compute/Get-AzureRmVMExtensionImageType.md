---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
ms.openlocfilehash: 3a310588b77888851684638911f88af95d600db7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929977"
---
# <span data-ttu-id="30461-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="30461-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="30461-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30461-102">SYNOPSIS</span></span>
<span data-ttu-id="30461-103">Hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="30461-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30461-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30461-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30461-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30461-105">DESCRIPTION</span></span>
<span data-ttu-id="30461-106">Cmdleten **Get-AzureRmVMExtensionImageType** hämtar typen av ett Azure-tillägg.</span><span class="sxs-lookup"><span data-stu-id="30461-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="30461-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30461-107">EXAMPLES</span></span>

### <span data-ttu-id="30461-108">Exempel 1: Hämta en bild av typen tillägg</span><span class="sxs-lookup"><span data-stu-id="30461-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="30461-109">Det här kommandot får bild typen tillägg för angiven utgivare och plats.</span><span class="sxs-lookup"><span data-stu-id="30461-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="30461-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30461-110">PARAMETERS</span></span>

### <span data-ttu-id="30461-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30461-111">-DefaultProfile</span></span>
<span data-ttu-id="30461-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30461-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30461-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="30461-113">-Location</span></span>
<span data-ttu-id="30461-114">Anger platsen för ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="30461-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="30461-115">Denna cmdlet får typen för ett tillägg på den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="30461-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="30461-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="30461-116">-PublisherName</span></span>
<span data-ttu-id="30461-117">Anger namnet på en utgivare av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="30461-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="30461-118">Använd Get-AzureRmVMImagePublisher cmdlet för att få en förlängnings utgivare.</span><span class="sxs-lookup"><span data-stu-id="30461-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="30461-119">Denna cmdlet får typen för ett tillägg från den utgivare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="30461-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="30461-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30461-120">CommonParameters</span></span>
<span data-ttu-id="30461-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30461-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30461-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30461-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30461-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30461-123">INPUTS</span></span>

### <span data-ttu-id="30461-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="30461-124">None</span></span>
<span data-ttu-id="30461-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="30461-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30461-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30461-126">OUTPUTS</span></span>

### <span data-ttu-id="30461-127">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="30461-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="30461-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30461-128">NOTES</span></span>

## <span data-ttu-id="30461-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30461-129">RELATED LINKS</span></span>

[<span data-ttu-id="30461-130">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="30461-130">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="30461-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="30461-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

