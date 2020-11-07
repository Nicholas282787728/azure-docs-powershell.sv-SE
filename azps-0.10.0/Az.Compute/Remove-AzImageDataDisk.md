---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 3c7399e3eec760e8d4a40d58a8ea9a56e744cfd4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924993"
---
# <span data-ttu-id="d3fa3-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="d3fa3-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="d3fa3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="d3fa3-103">Tar bort en datadisk från ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="d3fa3-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="d3fa3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3fa3-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3fa3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="d3fa3-106">Cmdleten **Remove-AzImageDataDisk** tar bort en datadisk från ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="d3fa3-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="d3fa3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3fa3-107">EXAMPLES</span></span>

### <span data-ttu-id="d3fa3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d3fa3-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="d3fa3-109">Det här kommandot tar bort data disken för det logiska enhets numret 1 från den befintliga bilden ' Image01 ' i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="d3fa3-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d3fa3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3fa3-110">PARAMETERS</span></span>

### <span data-ttu-id="d3fa3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3fa3-111">-DefaultProfile</span></span>
<span data-ttu-id="d3fa3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fa3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3fa3-113">-Image</span><span class="sxs-lookup"><span data-stu-id="d3fa3-113">-Image</span></span>
<span data-ttu-id="d3fa3-114">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="d3fa3-114">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3fa3-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="d3fa3-115">-Lun</span></span>
<span data-ttu-id="d3fa3-116">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="d3fa3-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="d3fa3-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3fa3-117">-Confirm</span></span>
<span data-ttu-id="d3fa3-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3fa3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3fa3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3fa3-119">-WhatIf</span></span>
<span data-ttu-id="d3fa3-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3fa3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3fa3-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3fa3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3fa3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3fa3-122">CommonParameters</span></span>
<span data-ttu-id="d3fa3-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3fa3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3fa3-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3fa3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3fa3-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3fa3-125">INPUTS</span></span>

### <span data-ttu-id="d3fa3-126">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="d3fa3-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="d3fa3-127">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d3fa3-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d3fa3-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3fa3-128">OUTPUTS</span></span>

### <span data-ttu-id="d3fa3-129">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="d3fa3-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="d3fa3-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3fa3-130">NOTES</span></span>

## <span data-ttu-id="d3fa3-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3fa3-131">RELATED LINKS</span></span>

