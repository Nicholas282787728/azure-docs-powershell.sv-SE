---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
ms.openlocfilehash: 5d8ed5a26e141d0ae8d6eb7494a76d8c53590d29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757108"
---
# <span data-ttu-id="06e98-101">Update-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="06e98-101">Update-AzureRmGallery</span></span>

## <span data-ttu-id="06e98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06e98-102">SYNOPSIS</span></span>
<span data-ttu-id="06e98-103">Uppdatera ett galleri.</span><span class="sxs-lookup"><span data-stu-id="06e98-103">Update a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06e98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06e98-104">SYNTAX</span></span>

### <span data-ttu-id="06e98-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="06e98-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e98-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="06e98-106">ResourceIdParameter</span></span>
```
Update-AzureRmGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e98-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="06e98-107">ObjectParameter</span></span>
```
Update-AzureRmGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06e98-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06e98-108">DESCRIPTION</span></span>
<span data-ttu-id="06e98-109">Uppdatera ett galleri.</span><span class="sxs-lookup"><span data-stu-id="06e98-109">Update a gallery.</span></span>

## <span data-ttu-id="06e98-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06e98-110">EXAMPLES</span></span>

### <span data-ttu-id="06e98-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06e98-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="06e98-112">Uppdatera ett galleri.</span><span class="sxs-lookup"><span data-stu-id="06e98-112">Update a gallery.</span></span>

## <span data-ttu-id="06e98-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06e98-113">PARAMETERS</span></span>

### <span data-ttu-id="06e98-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06e98-114">-AsJob</span></span>
<span data-ttu-id="06e98-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="06e98-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06e98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e98-116">-DefaultProfile</span></span>
<span data-ttu-id="06e98-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06e98-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06e98-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="06e98-118">-Description</span></span>
<span data-ttu-id="06e98-119">Beskrivning av Galleri resursen.</span><span class="sxs-lookup"><span data-stu-id="06e98-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="06e98-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06e98-120">-InputObject</span></span>
<span data-ttu-id="06e98-121">PS-GALLERYITEM.</span><span class="sxs-lookup"><span data-stu-id="06e98-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="06e98-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="06e98-122">-Name</span></span>
<span data-ttu-id="06e98-123">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="06e98-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="06e98-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e98-124">-ResourceGroupName</span></span>
<span data-ttu-id="06e98-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="06e98-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="06e98-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06e98-126">-ResourceId</span></span>
<span data-ttu-id="06e98-127">Resurs-ID för galleriet</span><span class="sxs-lookup"><span data-stu-id="06e98-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="06e98-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="06e98-128">-Tag</span></span>
<span data-ttu-id="06e98-129">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="06e98-129">Resource tags</span></span>

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

### <span data-ttu-id="06e98-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06e98-130">-Confirm</span></span>
<span data-ttu-id="06e98-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06e98-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e98-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e98-132">-WhatIf</span></span>
<span data-ttu-id="06e98-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06e98-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06e98-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06e98-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e98-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e98-135">CommonParameters</span></span>
<span data-ttu-id="06e98-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06e98-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e98-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e98-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e98-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06e98-138">INPUTS</span></span>

### <span data-ttu-id="06e98-139">System. String</span><span class="sxs-lookup"><span data-stu-id="06e98-139">System.String</span></span>

### <span data-ttu-id="06e98-140">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="06e98-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="06e98-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="06e98-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="06e98-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06e98-142">OUTPUTS</span></span>

### <span data-ttu-id="06e98-143">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="06e98-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="06e98-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06e98-144">NOTES</span></span>

## <span data-ttu-id="06e98-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06e98-145">RELATED LINKS</span></span>
