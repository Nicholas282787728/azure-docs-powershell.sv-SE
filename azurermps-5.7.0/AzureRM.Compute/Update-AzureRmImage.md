---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: b7c5155706b968973bef6a5cf1ce2285caee819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573501"
---
# <span data-ttu-id="69402-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="69402-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="69402-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69402-102">SYNOPSIS</span></span>
<span data-ttu-id="69402-103">Uppdaterar en bild.</span><span class="sxs-lookup"><span data-stu-id="69402-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69402-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69402-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69402-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69402-105">DESCRIPTION</span></span>
<span data-ttu-id="69402-106">Cmdleten **Update-AzureRmImage** uppdaterar en bild.</span><span class="sxs-lookup"><span data-stu-id="69402-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="69402-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69402-107">EXAMPLES</span></span>

### <span data-ttu-id="69402-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="69402-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="69402-109">Det här kommandot tar bort data disken för det logiska enhets numret 1 från den befintliga bilden ' Image01 ' i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="69402-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="69402-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69402-110">PARAMETERS</span></span>

### <span data-ttu-id="69402-111">-Image</span><span class="sxs-lookup"><span data-stu-id="69402-111">-Image</span></span>
<span data-ttu-id="69402-112">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="69402-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69402-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="69402-113">-ImageName</span></span>
<span data-ttu-id="69402-114">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="69402-114">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69402-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69402-115">-ResourceGroupName</span></span>
<span data-ttu-id="69402-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="69402-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69402-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="69402-117">-Confirm</span></span>
<span data-ttu-id="69402-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="69402-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69402-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69402-119">-WhatIf</span></span>
<span data-ttu-id="69402-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="69402-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69402-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="69402-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69402-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69402-122">CommonParameters</span></span>
<span data-ttu-id="69402-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69402-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69402-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69402-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69402-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69402-125">INPUTS</span></span>

### <span data-ttu-id="69402-126">System. String</span><span class="sxs-lookup"><span data-stu-id="69402-126">System.String</span></span>
<span data-ttu-id="69402-127">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="69402-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="69402-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69402-128">OUTPUTS</span></span>

### <span data-ttu-id="69402-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="69402-129">System.Object</span></span>

## <span data-ttu-id="69402-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69402-130">NOTES</span></span>

## <span data-ttu-id="69402-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69402-131">RELATED LINKS</span></span>

