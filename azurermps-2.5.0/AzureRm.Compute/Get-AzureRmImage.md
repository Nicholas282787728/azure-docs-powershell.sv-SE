---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermimage
schema: 2.0.0
ms.openlocfilehash: 8508a7353924342449324588e90abf3807d7f7ac
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929985"
---
# <span data-ttu-id="22b15-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="22b15-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="22b15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22b15-102">SYNOPSIS</span></span>
<span data-ttu-id="22b15-103">Hämtar egenskaperna för en bild.</span><span class="sxs-lookup"><span data-stu-id="22b15-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22b15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22b15-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22b15-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22b15-105">DESCRIPTION</span></span>
<span data-ttu-id="22b15-106">Cmdleten **Get-AzureRmImage** hämtar egenskaperna för en bild.</span><span class="sxs-lookup"><span data-stu-id="22b15-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="22b15-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22b15-107">EXAMPLES</span></span>

### <span data-ttu-id="22b15-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="22b15-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="22b15-109">Det här kommandot får egenskaperna för bilden med namnet "Image01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="22b15-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="22b15-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="22b15-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="22b15-111">Det här kommandot får egenskaperna för alla bilder i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="22b15-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="22b15-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="22b15-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="22b15-113">Det här kommandot får egenskaperna för alla bilder under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="22b15-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="22b15-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22b15-114">PARAMETERS</span></span>

### <span data-ttu-id="22b15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b15-115">-DefaultProfile</span></span>
<span data-ttu-id="22b15-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22b15-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22b15-117">-Expandera</span><span class="sxs-lookup"><span data-stu-id="22b15-117">-Expand</span></span>
<span data-ttu-id="22b15-118">Anger frågan expandera uttryck.</span><span class="sxs-lookup"><span data-stu-id="22b15-118">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="22b15-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="22b15-119">-ImageName</span></span>
<span data-ttu-id="22b15-120">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="22b15-120">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="22b15-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22b15-121">-ResourceGroupName</span></span>
<span data-ttu-id="22b15-122">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="22b15-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="22b15-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b15-123">CommonParameters</span></span>
<span data-ttu-id="22b15-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b15-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b15-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b15-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b15-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22b15-126">INPUTS</span></span>

### <span data-ttu-id="22b15-127">System. String</span><span class="sxs-lookup"><span data-stu-id="22b15-127">System.String</span></span>

## <span data-ttu-id="22b15-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22b15-128">OUTPUTS</span></span>

### <span data-ttu-id="22b15-129">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="22b15-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="22b15-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22b15-130">NOTES</span></span>

## <span data-ttu-id="22b15-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22b15-131">RELATED LINKS</span></span>

