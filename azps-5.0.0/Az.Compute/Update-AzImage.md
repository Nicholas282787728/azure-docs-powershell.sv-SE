---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319608"
---
# <span data-ttu-id="02268-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="02268-101">Update-AzImage</span></span>

## <span data-ttu-id="02268-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02268-102">SYNOPSIS</span></span>
<span data-ttu-id="02268-103">Uppdaterar en bild.</span><span class="sxs-lookup"><span data-stu-id="02268-103">Updates an image.</span></span>

## <span data-ttu-id="02268-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02268-104">SYNTAX</span></span>

### <span data-ttu-id="02268-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="02268-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02268-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="02268-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02268-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="02268-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02268-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02268-108">DESCRIPTION</span></span>
<span data-ttu-id="02268-109">Cmdleten **Update-AzImage** uppdaterar en bild.</span><span class="sxs-lookup"><span data-stu-id="02268-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="02268-110">För närvarande går det bara att uppdatera märkningarna.</span><span class="sxs-lookup"><span data-stu-id="02268-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="02268-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02268-111">EXAMPLES</span></span>

### <span data-ttu-id="02268-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="02268-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="02268-113">Det här kommandot uppdaterar taggnamnet för den befintliga bilden "Image01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="02268-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="02268-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02268-114">PARAMETERS</span></span>

### <span data-ttu-id="02268-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02268-115">-AsJob</span></span>
<span data-ttu-id="02268-116">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="02268-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="02268-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02268-117">-DefaultProfile</span></span>
<span data-ttu-id="02268-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02268-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02268-119">-Image</span><span class="sxs-lookup"><span data-stu-id="02268-119">-Image</span></span>
<span data-ttu-id="02268-120">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="02268-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02268-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="02268-121">-ImageName</span></span>
<span data-ttu-id="02268-122">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="02268-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02268-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02268-123">-ResourceGroupName</span></span>
<span data-ttu-id="02268-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="02268-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02268-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02268-125">-ResourceId</span></span>
<span data-ttu-id="02268-126">Resurs-ID för bilden</span><span class="sxs-lookup"><span data-stu-id="02268-126">The resource Id for the image</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02268-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="02268-127">-Tag</span></span>
<span data-ttu-id="02268-128">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="02268-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02268-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02268-129">-Confirm</span></span>
<span data-ttu-id="02268-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02268-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02268-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02268-131">-WhatIf</span></span>
<span data-ttu-id="02268-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02268-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02268-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02268-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02268-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02268-134">CommonParameters</span></span>
<span data-ttu-id="02268-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02268-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02268-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02268-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02268-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02268-137">INPUTS</span></span>

### <span data-ttu-id="02268-138">System. String</span><span class="sxs-lookup"><span data-stu-id="02268-138">System.String</span></span>

### <span data-ttu-id="02268-139">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="02268-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="02268-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02268-140">OUTPUTS</span></span>

### <span data-ttu-id="02268-141">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="02268-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="02268-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02268-142">NOTES</span></span>

## <span data-ttu-id="02268-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02268-143">RELATED LINKS</span></span>