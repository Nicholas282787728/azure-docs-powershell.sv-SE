---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: ccca83cdbebcf73df9059807dc5b030e4ab21736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756354"
---
# <span data-ttu-id="8ca04-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="8ca04-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="8ca04-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ca04-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca04-103">Uppdaterar en bild.</span><span class="sxs-lookup"><span data-stu-id="8ca04-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ca04-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ca04-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ca04-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ca04-105">DESCRIPTION</span></span>
<span data-ttu-id="8ca04-106">Cmdleten **Update-AzureRmImage** uppdaterar en bild.</span><span class="sxs-lookup"><span data-stu-id="8ca04-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="8ca04-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ca04-107">EXAMPLES</span></span>

### <span data-ttu-id="8ca04-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8ca04-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="8ca04-109">Det här kommandot tar bort data disken för det logiska enhets numret 1 från den befintliga bilden ' Image01 ' i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="8ca04-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8ca04-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ca04-110">PARAMETERS</span></span>

### <span data-ttu-id="8ca04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca04-111">-DefaultProfile</span></span>
<span data-ttu-id="8ca04-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ca04-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ca04-113">-Image</span><span class="sxs-lookup"><span data-stu-id="8ca04-113">-Image</span></span>
<span data-ttu-id="8ca04-114">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="8ca04-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca04-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="8ca04-115">-ImageName</span></span>
<span data-ttu-id="8ca04-116">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="8ca04-116">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca04-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ca04-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ca04-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8ca04-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca04-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8ca04-119">-Confirm</span></span>
<span data-ttu-id="8ca04-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8ca04-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ca04-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ca04-121">-WhatIf</span></span>
<span data-ttu-id="8ca04-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8ca04-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ca04-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8ca04-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ca04-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca04-124">CommonParameters</span></span>
<span data-ttu-id="8ca04-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ca04-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca04-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ca04-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca04-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ca04-127">INPUTS</span></span>

### <span data-ttu-id="8ca04-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8ca04-128">System.String</span></span>
<span data-ttu-id="8ca04-129">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="8ca04-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="8ca04-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ca04-130">OUTPUTS</span></span>

### <span data-ttu-id="8ca04-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="8ca04-131">System.Object</span></span>

## <span data-ttu-id="8ca04-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ca04-132">NOTES</span></span>

## <span data-ttu-id="8ca04-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ca04-133">RELATED LINKS</span></span>

