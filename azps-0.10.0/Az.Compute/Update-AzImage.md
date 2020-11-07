---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 1a04ca9df307b8d6251c6a8378df86827a76d001
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923025"
---
# <span data-ttu-id="288af-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="288af-101">Update-AzImage</span></span>

## <span data-ttu-id="288af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="288af-102">SYNOPSIS</span></span>
<span data-ttu-id="288af-103">Uppdaterar en bild.</span><span class="sxs-lookup"><span data-stu-id="288af-103">Updates an image.</span></span>

## <span data-ttu-id="288af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="288af-104">SYNTAX</span></span>

```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="288af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="288af-105">DESCRIPTION</span></span>
<span data-ttu-id="288af-106">Cmdleten **Update-AzImage** uppdaterar en bild.</span><span class="sxs-lookup"><span data-stu-id="288af-106">The **Update-AzImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="288af-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="288af-107">EXAMPLES</span></span>

### <span data-ttu-id="288af-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="288af-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="288af-109">Det här kommandot tar bort data disken för det logiska enhets numret 1 från den befintliga bilden ' Image01 ' i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="288af-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="288af-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="288af-110">PARAMETERS</span></span>

### <span data-ttu-id="288af-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="288af-111">-AsJob</span></span>
<span data-ttu-id="288af-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="288af-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="288af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288af-113">-DefaultProfile</span></span>
<span data-ttu-id="288af-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="288af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="288af-115">-Image</span><span class="sxs-lookup"><span data-stu-id="288af-115">-Image</span></span>
<span data-ttu-id="288af-116">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="288af-116">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="288af-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="288af-117">-ImageName</span></span>
<span data-ttu-id="288af-118">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="288af-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="288af-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288af-119">-ResourceGroupName</span></span>
<span data-ttu-id="288af-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="288af-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="288af-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="288af-121">-Confirm</span></span>
<span data-ttu-id="288af-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="288af-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="288af-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="288af-123">-WhatIf</span></span>
<span data-ttu-id="288af-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="288af-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="288af-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="288af-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="288af-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288af-126">CommonParameters</span></span>
<span data-ttu-id="288af-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="288af-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288af-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="288af-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288af-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="288af-129">INPUTS</span></span>

### <span data-ttu-id="288af-130">System. String</span><span class="sxs-lookup"><span data-stu-id="288af-130">System.String</span></span>
<span data-ttu-id="288af-131">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="288af-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="288af-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="288af-132">OUTPUTS</span></span>

### <span data-ttu-id="288af-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="288af-133">System.Object</span></span>

## <span data-ttu-id="288af-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="288af-134">NOTES</span></span>

## <span data-ttu-id="288af-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="288af-135">RELATED LINKS</span></span>

