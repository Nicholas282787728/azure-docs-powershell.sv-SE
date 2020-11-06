---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
ms.openlocfilehash: c2a65eeb742d4182dfad0cd32be1d78951977096
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575273"
---
# <span data-ttu-id="24f4f-101">Remove-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="24f4f-101">Remove-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="24f4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="24f4f-103">Ta bort en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="24f4f-103">Delete a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24f4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24f4f-104">SYNTAX</span></span>

### <span data-ttu-id="24f4f-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="24f4f-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f4f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="24f4f-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f4f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="24f4f-107">ObjectParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24f4f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24f4f-108">DESCRIPTION</span></span>
<span data-ttu-id="24f4f-109">Ta bort en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="24f4f-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="24f4f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24f4f-110">EXAMPLES</span></span>

### <span data-ttu-id="24f4f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="24f4f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="24f4f-112">Ta bort den angivna galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="24f4f-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="24f4f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24f4f-113">PARAMETERS</span></span>

### <span data-ttu-id="24f4f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24f4f-114">-AsJob</span></span>
<span data-ttu-id="24f4f-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="24f4f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24f4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f4f-116">-DefaultProfile</span></span>
<span data-ttu-id="24f4f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24f4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24f4f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="24f4f-118">-Force</span></span>
<span data-ttu-id="24f4f-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="24f4f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24f4f-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="24f4f-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="24f4f-121">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="24f4f-121">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f4f-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="24f4f-122">-GalleryName</span></span>
<span data-ttu-id="24f4f-123">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="24f4f-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="24f4f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24f4f-124">-InputObject</span></span>
<span data-ttu-id="24f4f-125">Versions objekt för PS-galleriet</span><span class="sxs-lookup"><span data-stu-id="24f4f-125">The PS Gallery Image Version Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24f4f-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="24f4f-126">-Name</span></span>
<span data-ttu-id="24f4f-127">Namnet på Galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="24f4f-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f4f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f4f-128">-ResourceGroupName</span></span>
<span data-ttu-id="24f4f-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="24f4f-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="24f4f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24f4f-130">-ResourceId</span></span>
<span data-ttu-id="24f4f-131">Resurs-ID för galleriet bild version</span><span class="sxs-lookup"><span data-stu-id="24f4f-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="24f4f-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24f4f-132">-Confirm</span></span>
<span data-ttu-id="24f4f-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24f4f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24f4f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f4f-134">-WhatIf</span></span>
<span data-ttu-id="24f4f-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24f4f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24f4f-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24f4f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24f4f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f4f-137">CommonParameters</span></span>
<span data-ttu-id="24f4f-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24f4f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f4f-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24f4f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f4f-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24f4f-140">INPUTS</span></span>

### <span data-ttu-id="24f4f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="24f4f-141">System.String</span></span>

### <span data-ttu-id="24f4f-142">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="24f4f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="24f4f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24f4f-143">OUTPUTS</span></span>

### <span data-ttu-id="24f4f-144">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="24f4f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="24f4f-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24f4f-145">NOTES</span></span>

## <span data-ttu-id="24f4f-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24f4f-146">RELATED LINKS</span></span>
