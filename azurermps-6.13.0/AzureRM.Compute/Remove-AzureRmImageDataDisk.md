---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 8ff2544aab072842ed851ae0c3768f57d180186d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575270"
---
# <span data-ttu-id="694b6-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="694b6-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="694b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="694b6-102">SYNOPSIS</span></span>
<span data-ttu-id="694b6-103">Tar bort en datadisk från ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="694b6-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="694b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="694b6-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="694b6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="694b6-105">DESCRIPTION</span></span>
<span data-ttu-id="694b6-106">Cmdleten **Remove-AzureRmImageDataDisk** tar bort en datadisk från ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="694b6-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="694b6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="694b6-107">EXAMPLES</span></span>

### <span data-ttu-id="694b6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="694b6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="694b6-109">Det här kommandot tar bort data disken för det logiska enhets numret 1 från den befintliga bilden ' Image01 ' i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="694b6-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="694b6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="694b6-110">PARAMETERS</span></span>

### <span data-ttu-id="694b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="694b6-111">-DefaultProfile</span></span>
<span data-ttu-id="694b6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="694b6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="694b6-113">-Image</span><span class="sxs-lookup"><span data-stu-id="694b6-113">-Image</span></span>
<span data-ttu-id="694b6-114">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="694b6-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="694b6-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="694b6-115">-Lun</span></span>
<span data-ttu-id="694b6-116">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="694b6-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="694b6-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="694b6-117">-Confirm</span></span>
<span data-ttu-id="694b6-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="694b6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="694b6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="694b6-119">-WhatIf</span></span>
<span data-ttu-id="694b6-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="694b6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="694b6-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="694b6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="694b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694b6-122">CommonParameters</span></span>
<span data-ttu-id="694b6-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="694b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694b6-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="694b6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694b6-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="694b6-125">INPUTS</span></span>

### <span data-ttu-id="694b6-126">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="694b6-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="694b6-127">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="694b6-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="694b6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="694b6-128">OUTPUTS</span></span>

### <span data-ttu-id="694b6-129">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="694b6-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="694b6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="694b6-130">NOTES</span></span>

## <span data-ttu-id="694b6-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="694b6-131">RELATED LINKS</span></span>
