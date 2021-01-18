---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526571"
---
# <span data-ttu-id="79856-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="79856-101">Update-AzGallery</span></span>

## <span data-ttu-id="79856-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79856-102">SYNOPSIS</span></span>
<span data-ttu-id="79856-103">Uppdatera ett galleri.</span><span class="sxs-lookup"><span data-stu-id="79856-103">Update a gallery.</span></span>

## <span data-ttu-id="79856-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79856-104">SYNTAX</span></span>

### <span data-ttu-id="79856-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="79856-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79856-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="79856-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79856-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="79856-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79856-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79856-108">DESCRIPTION</span></span>
<span data-ttu-id="79856-109">Uppdatera ett galleri.</span><span class="sxs-lookup"><span data-stu-id="79856-109">Update a gallery.</span></span>

## <span data-ttu-id="79856-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79856-110">EXAMPLES</span></span>

### <span data-ttu-id="79856-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="79856-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="79856-112">Uppdatera ett galleri.</span><span class="sxs-lookup"><span data-stu-id="79856-112">Update a gallery.</span></span>

## <span data-ttu-id="79856-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79856-113">PARAMETERS</span></span>

### <span data-ttu-id="79856-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79856-114">-AsJob</span></span>
<span data-ttu-id="79856-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="79856-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79856-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79856-116">-DefaultProfile</span></span>
<span data-ttu-id="79856-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79856-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79856-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="79856-118">-Description</span></span>
<span data-ttu-id="79856-119">Beskrivning av Galleri resursen.</span><span class="sxs-lookup"><span data-stu-id="79856-119">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79856-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79856-120">-InputObject</span></span>
<span data-ttu-id="79856-121">PS-GALLERYITEM.</span><span class="sxs-lookup"><span data-stu-id="79856-121">The PS Gallery Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79856-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="79856-122">-Name</span></span>
<span data-ttu-id="79856-123">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="79856-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79856-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79856-124">-ResourceGroupName</span></span>
<span data-ttu-id="79856-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="79856-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="79856-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79856-126">-ResourceId</span></span>
<span data-ttu-id="79856-127">Resurs-ID för galleriet</span><span class="sxs-lookup"><span data-stu-id="79856-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="79856-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="79856-128">-Tag</span></span>
<span data-ttu-id="79856-129">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="79856-129">Resource tags</span></span>

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

### <span data-ttu-id="79856-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="79856-130">-Confirm</span></span>
<span data-ttu-id="79856-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79856-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79856-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79856-132">-WhatIf</span></span>
<span data-ttu-id="79856-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="79856-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79856-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="79856-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79856-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79856-135">CommonParameters</span></span>
<span data-ttu-id="79856-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79856-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79856-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79856-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79856-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79856-138">INPUTS</span></span>

### <span data-ttu-id="79856-139">System. String</span><span class="sxs-lookup"><span data-stu-id="79856-139">System.String</span></span>

### <span data-ttu-id="79856-140">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="79856-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="79856-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="79856-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="79856-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79856-142">OUTPUTS</span></span>

### <span data-ttu-id="79856-143">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="79856-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="79856-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79856-144">NOTES</span></span>

## <span data-ttu-id="79856-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79856-145">RELATED LINKS</span></span>
