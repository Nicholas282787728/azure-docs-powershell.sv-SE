---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: 34c4eefe2792de239b2f3ae2a9348704497a4bd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756217"
---
# <span data-ttu-id="ad618-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="ad618-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="ad618-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad618-102">SYNOPSIS</span></span>
<span data-ttu-id="ad618-103">Uppdaterar en bild.</span><span class="sxs-lookup"><span data-stu-id="ad618-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad618-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad618-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad618-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad618-105">DESCRIPTION</span></span>
<span data-ttu-id="ad618-106">Cmdleten **Update-AzureRmImage** uppdaterar en bild.</span><span class="sxs-lookup"><span data-stu-id="ad618-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="ad618-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad618-107">EXAMPLES</span></span>

### <span data-ttu-id="ad618-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ad618-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="ad618-109">Det här kommandot tar bort data disken för det logiska enhets numret 1 från den befintliga bilden ' Image01 ' i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="ad618-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ad618-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad618-110">PARAMETERS</span></span>

### <span data-ttu-id="ad618-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad618-111">-AsJob</span></span>
<span data-ttu-id="ad618-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ad618-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad618-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad618-113">-DefaultProfile</span></span>
<span data-ttu-id="ad618-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad618-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad618-115">-Image</span><span class="sxs-lookup"><span data-stu-id="ad618-115">-Image</span></span>
<span data-ttu-id="ad618-116">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="ad618-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="ad618-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ad618-117">-ImageName</span></span>
<span data-ttu-id="ad618-118">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="ad618-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="ad618-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad618-119">-ResourceGroupName</span></span>
<span data-ttu-id="ad618-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ad618-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad618-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad618-121">-Confirm</span></span>
<span data-ttu-id="ad618-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad618-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad618-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad618-123">-WhatIf</span></span>
<span data-ttu-id="ad618-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad618-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad618-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad618-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad618-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad618-126">CommonParameters</span></span>
<span data-ttu-id="ad618-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad618-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad618-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad618-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad618-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad618-129">INPUTS</span></span>

### <span data-ttu-id="ad618-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ad618-130">System.String</span></span>

### <span data-ttu-id="ad618-131">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="ad618-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>
<span data-ttu-id="ad618-132">Parametrar: bild (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad618-132">Parameters: Image (ByValue)</span></span>

## <span data-ttu-id="ad618-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad618-133">OUTPUTS</span></span>

### <span data-ttu-id="ad618-134">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="ad618-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="ad618-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad618-135">NOTES</span></span>

## <span data-ttu-id="ad618-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad618-136">RELATED LINKS</span></span>
