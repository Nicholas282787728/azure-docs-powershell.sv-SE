---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 054462398a0f7b3e8710928000f9c10fb42f04db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755776"
---
# <span data-ttu-id="ce24f-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="ce24f-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="ce24f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce24f-102">SYNOPSIS</span></span>
<span data-ttu-id="ce24f-103">Tar bort en bild.</span><span class="sxs-lookup"><span data-stu-id="ce24f-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce24f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce24f-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce24f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce24f-105">DESCRIPTION</span></span>
<span data-ttu-id="ce24f-106">Cmdleten **Remove-AzureRmImage** tar bort en bild..</span><span class="sxs-lookup"><span data-stu-id="ce24f-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="ce24f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce24f-107">EXAMPLES</span></span>

### <span data-ttu-id="ce24f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ce24f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="ce24f-109">Det här kommandot tar bort bilden "Image01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ce24f-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ce24f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce24f-110">PARAMETERS</span></span>

### <span data-ttu-id="ce24f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ce24f-111">-Force</span></span>
<span data-ttu-id="ce24f-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ce24f-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce24f-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ce24f-113">-ImageName</span></span>
<span data-ttu-id="ce24f-114">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="ce24f-114">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="ce24f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce24f-115">-ResourceGroupName</span></span>
<span data-ttu-id="ce24f-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ce24f-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ce24f-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce24f-117">-Confirm</span></span>
<span data-ttu-id="ce24f-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce24f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce24f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce24f-119">-WhatIf</span></span>
<span data-ttu-id="ce24f-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce24f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce24f-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce24f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce24f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce24f-122">CommonParameters</span></span>
<span data-ttu-id="ce24f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce24f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce24f-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce24f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce24f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce24f-125">INPUTS</span></span>

### <span data-ttu-id="ce24f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ce24f-126">System.String</span></span>

## <span data-ttu-id="ce24f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce24f-127">OUTPUTS</span></span>

### <span data-ttu-id="ce24f-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="ce24f-128">System.Object</span></span>

## <span data-ttu-id="ce24f-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce24f-129">NOTES</span></span>

## <span data-ttu-id="ce24f-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce24f-130">RELATED LINKS</span></span>

