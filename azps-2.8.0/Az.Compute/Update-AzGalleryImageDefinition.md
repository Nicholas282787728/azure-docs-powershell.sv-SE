---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: d0a149f5ee2e03345cd433952d49748886c066ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744884"
---
# <span data-ttu-id="4e9c8-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4e9c8-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="4e9c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e9c8-102">SYNOPSIS</span></span>
<span data-ttu-id="4e9c8-103">Uppdatera en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="4e9c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e9c8-104">SYNTAX</span></span>

### <span data-ttu-id="4e9c8-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="4e9c8-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e9c8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4e9c8-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e9c8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4e9c8-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e9c8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e9c8-108">DESCRIPTION</span></span>
<span data-ttu-id="4e9c8-109">Uppdatera en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="4e9c8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e9c8-110">EXAMPLES</span></span>

### <span data-ttu-id="4e9c8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4e9c8-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="4e9c8-112">Uppdatera en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="4e9c8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e9c8-113">PARAMETERS</span></span>

### <span data-ttu-id="4e9c8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e9c8-114">-AsJob</span></span>
<span data-ttu-id="4e9c8-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4e9c8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e9c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e9c8-116">-DefaultProfile</span></span>
<span data-ttu-id="4e9c8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e9c8-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4e9c8-118">-Description</span></span>
<span data-ttu-id="4e9c8-119">Beskrivning av bild definitions resursen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="4e9c8-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="4e9c8-120">-DisallowedDiskType</span></span>
<span data-ttu-id="4e9c8-121">De otillåtna disk typerna.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-121">The disallowed disk types.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9c8-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="4e9c8-122">-EndOfLifeDate</span></span>
<span data-ttu-id="4e9c8-123">Livs cykel datum för bild definitionen för galleriet</span><span class="sxs-lookup"><span data-stu-id="4e9c8-123">The end of life date of the gallery Image Definition</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9c8-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="4e9c8-124">-Eula</span></span>
<span data-ttu-id="4e9c8-125">EULA-avtalet för bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="4e9c8-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="4e9c8-126">-GalleryName</span></span>
<span data-ttu-id="4e9c8-127">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="4e9c8-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e9c8-128">-InputObject</span></span>
<span data-ttu-id="4e9c8-129">Bild definitions objekt för PS-galleriet.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="4e9c8-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="4e9c8-130">-MaximumMemory</span></span>
<span data-ttu-id="4e9c8-131">Det högsta av det rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="4e9c8-131">The maximum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9c8-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="4e9c8-132">-MaximumVCPU</span></span>
<span data-ttu-id="4e9c8-133">Max för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="4e9c8-133">The maximum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9c8-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="4e9c8-134">-MinimumMemory</span></span>
<span data-ttu-id="4e9c8-135">Det minsta rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="4e9c8-135">The minimum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9c8-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="4e9c8-136">-MinimumVCPU</span></span>
<span data-ttu-id="4e9c8-137">Minimum för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="4e9c8-137">The minimum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9c8-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="4e9c8-138">-Name</span></span>
<span data-ttu-id="4e9c8-139">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="4e9c8-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="4e9c8-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="4e9c8-141">URL för integritets policyn.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="4e9c8-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="4e9c8-142">-PurchasePlanName</span></span>
<span data-ttu-id="4e9c8-143">ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4e9c8-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="4e9c8-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="4e9c8-145">Produkt-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4e9c8-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="4e9c8-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="4e9c8-147">Publisher-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4e9c8-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="4e9c8-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="4e9c8-149">URI för release Note.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-149">The release note uri.</span></span>

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

### <span data-ttu-id="4e9c8-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e9c8-150">-ResourceGroupName</span></span>
<span data-ttu-id="4e9c8-151">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e9c8-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e9c8-152">-ResourceId</span></span>
<span data-ttu-id="4e9c8-153">Resurs-ID för bild definitionen</span><span class="sxs-lookup"><span data-stu-id="4e9c8-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="4e9c8-154">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4e9c8-154">-Tag</span></span>
<span data-ttu-id="4e9c8-155">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="4e9c8-155">Resource tags</span></span>

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

### <span data-ttu-id="4e9c8-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e9c8-156">-Confirm</span></span>
<span data-ttu-id="4e9c8-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e9c8-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e9c8-158">-WhatIf</span></span>
<span data-ttu-id="4e9c8-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e9c8-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e9c8-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e9c8-161">CommonParameters</span></span>
<span data-ttu-id="4e9c8-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e9c8-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e9c8-163">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e9c8-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e9c8-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e9c8-164">INPUTS</span></span>

### <span data-ttu-id="4e9c8-165">System. String</span><span class="sxs-lookup"><span data-stu-id="4e9c8-165">System.String</span></span>

### <span data-ttu-id="4e9c8-166">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="4e9c8-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="4e9c8-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="4e9c8-167">System.DateTime</span></span>

### <span data-ttu-id="4e9c8-168">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="4e9c8-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4e9c8-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4e9c8-169">System.Int32</span></span>

### <span data-ttu-id="4e9c8-170">System. string []</span><span class="sxs-lookup"><span data-stu-id="4e9c8-170">System.String[]</span></span>

## <span data-ttu-id="4e9c8-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e9c8-171">OUTPUTS</span></span>

### <span data-ttu-id="4e9c8-172">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="4e9c8-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="4e9c8-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e9c8-173">NOTES</span></span>

## <span data-ttu-id="4e9c8-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e9c8-174">RELATED LINKS</span></span>