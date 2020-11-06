---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 1d37af16fcb84db8247ac5db495abb1f41319c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584771"
---
# <span data-ttu-id="e1ded-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="e1ded-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="e1ded-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1ded-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ded-103">Tar bort en datadisk från ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="e1ded-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ded-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1ded-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1ded-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1ded-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ded-106">Cmdleten **Remove-AzureRmImageDataDisk** tar bort en datadisk från ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="e1ded-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="e1ded-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1ded-107">EXAMPLES</span></span>

### <span data-ttu-id="e1ded-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e1ded-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="e1ded-109">Det här kommandot tar bort data disken för det logiska enhets numret 1 från den befintliga bilden ' Image01 ' i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="e1ded-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e1ded-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1ded-110">PARAMETERS</span></span>

### <span data-ttu-id="e1ded-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ded-111">-DefaultProfile</span></span>
<span data-ttu-id="e1ded-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ded-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ded-113">-Image</span><span class="sxs-lookup"><span data-stu-id="e1ded-113">-Image</span></span>
<span data-ttu-id="e1ded-114">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="e1ded-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ded-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="e1ded-115">-Lun</span></span>
<span data-ttu-id="e1ded-116">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="e1ded-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ded-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1ded-117">-Confirm</span></span>
<span data-ttu-id="e1ded-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1ded-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ded-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ded-119">-WhatIf</span></span>
<span data-ttu-id="e1ded-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1ded-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1ded-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1ded-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ded-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ded-122">CommonParameters</span></span>
<span data-ttu-id="e1ded-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ded-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ded-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ded-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ded-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1ded-125">INPUTS</span></span>

### <span data-ttu-id="e1ded-126">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="e1ded-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="e1ded-127">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e1ded-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e1ded-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1ded-128">OUTPUTS</span></span>

### <span data-ttu-id="e1ded-129">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="e1ded-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="e1ded-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1ded-130">NOTES</span></span>

## <span data-ttu-id="e1ded-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1ded-131">RELATED LINKS</span></span>

