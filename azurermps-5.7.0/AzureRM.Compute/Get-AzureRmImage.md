---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: 3976418d89076b290500343775ca42e2fb975659
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578312"
---
# <span data-ttu-id="d285e-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="d285e-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="d285e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d285e-102">SYNOPSIS</span></span>
<span data-ttu-id="d285e-103">Hämtar egenskaperna för en bild.</span><span class="sxs-lookup"><span data-stu-id="d285e-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d285e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d285e-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d285e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d285e-105">DESCRIPTION</span></span>
<span data-ttu-id="d285e-106">Cmdleten **Get-AzureRmImage** hämtar egenskaperna för en bild.</span><span class="sxs-lookup"><span data-stu-id="d285e-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="d285e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d285e-107">EXAMPLES</span></span>

### <span data-ttu-id="d285e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d285e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="d285e-109">Det här kommandot får egenskaperna för bilden med namnet "Image01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d285e-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d285e-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d285e-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="d285e-111">Det här kommandot får egenskaperna för alla bilder i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="d285e-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d285e-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="d285e-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="d285e-113">Det här kommandot får egenskaperna för alla bilder under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d285e-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="d285e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d285e-114">PARAMETERS</span></span>

### <span data-ttu-id="d285e-115">-Expandera</span><span class="sxs-lookup"><span data-stu-id="d285e-115">-Expand</span></span>
<span data-ttu-id="d285e-116">Anger frågan expandera uttryck.</span><span class="sxs-lookup"><span data-stu-id="d285e-116">Specifies the expand expression query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d285e-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="d285e-117">-ImageName</span></span>
<span data-ttu-id="d285e-118">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="d285e-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d285e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d285e-119">-ResourceGroupName</span></span>
<span data-ttu-id="d285e-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d285e-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d285e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d285e-121">CommonParameters</span></span>
<span data-ttu-id="d285e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d285e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d285e-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d285e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d285e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d285e-124">INPUTS</span></span>

### <span data-ttu-id="d285e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d285e-125">System.String</span></span>

## <span data-ttu-id="d285e-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d285e-126">OUTPUTS</span></span>

### <span data-ttu-id="d285e-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="d285e-127">System.Object</span></span>

## <span data-ttu-id="d285e-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d285e-128">NOTES</span></span>

## <span data-ttu-id="d285e-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d285e-129">RELATED LINKS</span></span>

