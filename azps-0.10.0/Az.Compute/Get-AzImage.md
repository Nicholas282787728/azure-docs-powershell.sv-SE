---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 13829081952be7ab79c6d7badde4dc687aa845ed
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925225"
---
# <span data-ttu-id="c486b-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="c486b-101">Get-AzImage</span></span>

## <span data-ttu-id="c486b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c486b-102">SYNOPSIS</span></span>
<span data-ttu-id="c486b-103">Hämtar egenskaperna för en bild.</span><span class="sxs-lookup"><span data-stu-id="c486b-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="c486b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c486b-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c486b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c486b-105">DESCRIPTION</span></span>
<span data-ttu-id="c486b-106">Cmdleten **Get-AzImage** hämtar egenskaperna för en bild.</span><span class="sxs-lookup"><span data-stu-id="c486b-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="c486b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c486b-107">EXAMPLES</span></span>

### <span data-ttu-id="c486b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c486b-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="c486b-109">Det här kommandot får egenskaperna för bilden med namnet "Image01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c486b-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c486b-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c486b-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="c486b-111">Det här kommandot får egenskaperna för alla bilder i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="c486b-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c486b-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c486b-112">Example 3</span></span>
```
PS C:\> Get-AzImage
```

<span data-ttu-id="c486b-113">Det här kommandot får egenskaperna för alla bilder under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c486b-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="c486b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c486b-114">PARAMETERS</span></span>

### <span data-ttu-id="c486b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c486b-115">-DefaultProfile</span></span>
<span data-ttu-id="c486b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c486b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c486b-117">-Expandera</span><span class="sxs-lookup"><span data-stu-id="c486b-117">-Expand</span></span>
<span data-ttu-id="c486b-118">Anger frågan expandera uttryck.</span><span class="sxs-lookup"><span data-stu-id="c486b-118">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="c486b-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="c486b-119">-ImageName</span></span>
<span data-ttu-id="c486b-120">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="c486b-120">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="c486b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c486b-121">-ResourceGroupName</span></span>
<span data-ttu-id="c486b-122">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c486b-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c486b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c486b-123">CommonParameters</span></span>
<span data-ttu-id="c486b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c486b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c486b-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c486b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c486b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c486b-126">INPUTS</span></span>

### <span data-ttu-id="c486b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c486b-127">System.String</span></span>

## <span data-ttu-id="c486b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c486b-128">OUTPUTS</span></span>

### <span data-ttu-id="c486b-129">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="c486b-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="c486b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c486b-130">NOTES</span></span>

## <span data-ttu-id="c486b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c486b-131">RELATED LINKS</span></span>

