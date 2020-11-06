---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 4115cabbeeb2a7c458ce52e80eb251cb972491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574343"
---
# <span data-ttu-id="09410-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="09410-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="09410-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09410-102">SYNOPSIS</span></span>
<span data-ttu-id="09410-103">Tar bort en datadisk från ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="09410-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09410-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09410-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <Image> [-Lun] <Int32> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09410-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09410-105">DESCRIPTION</span></span>
<span data-ttu-id="09410-106">Cmdleten **Remove-AzureRmImageDataDisk** tar bort en datadisk från ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="09410-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="09410-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09410-107">EXAMPLES</span></span>

### <span data-ttu-id="09410-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="09410-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="09410-109">Det här kommandot tar bort data disken för det logiska enhets numret 1 från den befintliga bilden ' Image01 ' i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="09410-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="09410-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09410-110">PARAMETERS</span></span>

### <span data-ttu-id="09410-111">-Image</span><span class="sxs-lookup"><span data-stu-id="09410-111">-Image</span></span>
<span data-ttu-id="09410-112">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="09410-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09410-113">-LUN</span><span class="sxs-lookup"><span data-stu-id="09410-113">-Lun</span></span>
<span data-ttu-id="09410-114">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="09410-114">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09410-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09410-115">-Confirm</span></span>
<span data-ttu-id="09410-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09410-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09410-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09410-117">-WhatIf</span></span>
<span data-ttu-id="09410-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09410-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09410-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09410-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09410-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09410-120">CommonParameters</span></span>
<span data-ttu-id="09410-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09410-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09410-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09410-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09410-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09410-123">INPUTS</span></span>

### <span data-ttu-id="09410-124">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="09410-124">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="09410-125">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="09410-125">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="09410-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09410-126">OUTPUTS</span></span>

### <span data-ttu-id="09410-127">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="09410-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="09410-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09410-128">NOTES</span></span>

## <span data-ttu-id="09410-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09410-129">RELATED LINKS</span></span>

