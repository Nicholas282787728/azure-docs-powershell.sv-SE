---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319624"
---
# <span data-ttu-id="67c46-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="67c46-101">Update-AzGallery</span></span>

## <span data-ttu-id="67c46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67c46-102">SYNOPSIS</span></span>
<span data-ttu-id="67c46-103">Uppdatera ett galleri.</span><span class="sxs-lookup"><span data-stu-id="67c46-103">Update a gallery.</span></span>

## <span data-ttu-id="67c46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67c46-104">SYNTAX</span></span>

### <span data-ttu-id="67c46-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="67c46-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67c46-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="67c46-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67c46-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="67c46-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67c46-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67c46-108">DESCRIPTION</span></span>
<span data-ttu-id="67c46-109">Uppdatera ett galleri.</span><span class="sxs-lookup"><span data-stu-id="67c46-109">Update a gallery.</span></span>

## <span data-ttu-id="67c46-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67c46-110">EXAMPLES</span></span>

### <span data-ttu-id="67c46-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="67c46-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="67c46-112">Uppdatera ett galleri.</span><span class="sxs-lookup"><span data-stu-id="67c46-112">Update a gallery.</span></span>

## <span data-ttu-id="67c46-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67c46-113">PARAMETERS</span></span>

### <span data-ttu-id="67c46-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67c46-114">-AsJob</span></span>
<span data-ttu-id="67c46-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="67c46-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67c46-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c46-116">-DefaultProfile</span></span>
<span data-ttu-id="67c46-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67c46-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67c46-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="67c46-118">-Description</span></span>
<span data-ttu-id="67c46-119">Beskrivning av Galleri resursen.</span><span class="sxs-lookup"><span data-stu-id="67c46-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="67c46-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67c46-120">-InputObject</span></span>
<span data-ttu-id="67c46-121">PS-GALLERYITEM.</span><span class="sxs-lookup"><span data-stu-id="67c46-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="67c46-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="67c46-122">-Name</span></span>
<span data-ttu-id="67c46-123">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="67c46-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="67c46-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c46-124">-ResourceGroupName</span></span>
<span data-ttu-id="67c46-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="67c46-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="67c46-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67c46-126">-ResourceId</span></span>
<span data-ttu-id="67c46-127">Resurs-ID för galleriet</span><span class="sxs-lookup"><span data-stu-id="67c46-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="67c46-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="67c46-128">-Tag</span></span>
<span data-ttu-id="67c46-129">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="67c46-129">Resource tags</span></span>

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

### <span data-ttu-id="67c46-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="67c46-130">-Confirm</span></span>
<span data-ttu-id="67c46-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="67c46-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67c46-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67c46-132">-WhatIf</span></span>
<span data-ttu-id="67c46-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="67c46-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67c46-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="67c46-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67c46-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c46-135">CommonParameters</span></span>
<span data-ttu-id="67c46-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67c46-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c46-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67c46-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c46-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67c46-138">INPUTS</span></span>

### <span data-ttu-id="67c46-139">System. String</span><span class="sxs-lookup"><span data-stu-id="67c46-139">System.String</span></span>

### <span data-ttu-id="67c46-140">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="67c46-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="67c46-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="67c46-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="67c46-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67c46-142">OUTPUTS</span></span>

### <span data-ttu-id="67c46-143">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="67c46-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="67c46-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67c46-144">NOTES</span></span>

## <span data-ttu-id="67c46-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67c46-145">RELATED LINKS</span></span>
