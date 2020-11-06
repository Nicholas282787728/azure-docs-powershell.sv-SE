---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: e6e62fbe52aeb87868c688343ebbaed8f0046891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577098"
---
# <span data-ttu-id="8cadf-101">Remove-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="8cadf-101">Remove-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="8cadf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8cadf-102">SYNOPSIS</span></span>
<span data-ttu-id="8cadf-103">Ta bort en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="8cadf-103">Delete a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cadf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8cadf-104">SYNTAX</span></span>

### <span data-ttu-id="8cadf-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="8cadf-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cadf-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8cadf-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cadf-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8cadf-107">ObjectParameter</span></span>
```
Remove-AzureRmGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cadf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8cadf-108">DESCRIPTION</span></span>
<span data-ttu-id="8cadf-109">Ta bort en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="8cadf-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="8cadf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8cadf-110">EXAMPLES</span></span>

### <span data-ttu-id="8cadf-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8cadf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="8cadf-112">Ta bort bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="8cadf-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="8cadf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8cadf-113">PARAMETERS</span></span>

### <span data-ttu-id="8cadf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cadf-114">-AsJob</span></span>
<span data-ttu-id="8cadf-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8cadf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cadf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cadf-116">-DefaultProfile</span></span>
<span data-ttu-id="8cadf-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8cadf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cadf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8cadf-118">-Force</span></span>
<span data-ttu-id="8cadf-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8cadf-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8cadf-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="8cadf-120">-GalleryName</span></span>
<span data-ttu-id="8cadf-121">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="8cadf-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cadf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cadf-122">-InputObject</span></span>
<span data-ttu-id="8cadf-123">Bild definitions objekt för PS-galleriet</span><span class="sxs-lookup"><span data-stu-id="8cadf-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cadf-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="8cadf-124">-Name</span></span>
<span data-ttu-id="8cadf-125">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="8cadf-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cadf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cadf-126">-ResourceGroupName</span></span>
<span data-ttu-id="8cadf-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8cadf-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="8cadf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cadf-128">-ResourceId</span></span>
<span data-ttu-id="8cadf-129">Resurs-ID för bild definitionen för galleriet</span><span class="sxs-lookup"><span data-stu-id="8cadf-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="8cadf-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8cadf-130">-Confirm</span></span>
<span data-ttu-id="8cadf-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8cadf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cadf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cadf-132">-WhatIf</span></span>
<span data-ttu-id="8cadf-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8cadf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cadf-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8cadf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cadf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cadf-135">CommonParameters</span></span>
<span data-ttu-id="8cadf-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cadf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cadf-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cadf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cadf-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8cadf-138">INPUTS</span></span>

### <span data-ttu-id="8cadf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8cadf-139">System.String</span></span>

### <span data-ttu-id="8cadf-140">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="8cadf-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="8cadf-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8cadf-141">OUTPUTS</span></span>

### <span data-ttu-id="8cadf-142">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8cadf-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8cadf-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8cadf-143">NOTES</span></span>

## <span data-ttu-id="8cadf-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8cadf-144">RELATED LINKS</span></span>
