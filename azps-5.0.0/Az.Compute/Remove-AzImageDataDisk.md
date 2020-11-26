---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 20399a1b62062afa5585e78a9fdb229ad3781d33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322524"
---
# <span data-ttu-id="f80f6-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="f80f6-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="f80f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f80f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f80f6-103">Tar bort en datadisk från ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="f80f6-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="f80f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f80f6-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f80f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f80f6-105">DESCRIPTION</span></span>
<span data-ttu-id="f80f6-106">Cmdleten **Remove-AzImageDataDisk** tar bort en datadisk från ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="f80f6-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="f80f6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f80f6-107">EXAMPLES</span></span>

### <span data-ttu-id="f80f6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f80f6-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="f80f6-109">Det här kommandot tar bort data disken för det logiska enhets numret 1 från den befintliga bilden ' Image01 ' i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="f80f6-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f80f6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f80f6-110">PARAMETERS</span></span>

### <span data-ttu-id="f80f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f80f6-111">-DefaultProfile</span></span>
<span data-ttu-id="f80f6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f80f6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f80f6-113">-Image</span><span class="sxs-lookup"><span data-stu-id="f80f6-113">-Image</span></span>
<span data-ttu-id="f80f6-114">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="f80f6-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="f80f6-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="f80f6-115">-Lun</span></span>
<span data-ttu-id="f80f6-116">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="f80f6-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="f80f6-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f80f6-117">-Confirm</span></span>
<span data-ttu-id="f80f6-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f80f6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f80f6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f80f6-119">-WhatIf</span></span>
<span data-ttu-id="f80f6-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f80f6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f80f6-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f80f6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f80f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f80f6-122">CommonParameters</span></span>
<span data-ttu-id="f80f6-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f80f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f80f6-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f80f6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f80f6-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f80f6-125">INPUTS</span></span>

### <span data-ttu-id="f80f6-126">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="f80f6-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="f80f6-127">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f80f6-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f80f6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f80f6-128">OUTPUTS</span></span>

### <span data-ttu-id="f80f6-129">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="f80f6-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f80f6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f80f6-130">NOTES</span></span>

## <span data-ttu-id="f80f6-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f80f6-131">RELATED LINKS</span></span>