---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 042c29ca079978a4ce740dba7d8ced9b0387eaf4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319619"
---
# <span data-ttu-id="fb254-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="fb254-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="fb254-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb254-102">SYNOPSIS</span></span>
<span data-ttu-id="fb254-103">Uppdatera en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="fb254-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="fb254-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb254-104">SYNTAX</span></span>

### <span data-ttu-id="fb254-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="fb254-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb254-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="fb254-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb254-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="fb254-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb254-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb254-108">DESCRIPTION</span></span>
<span data-ttu-id="fb254-109">Uppdatera en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="fb254-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="fb254-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb254-110">EXAMPLES</span></span>

### <span data-ttu-id="fb254-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fb254-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="fb254-112">Uppdatera en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="fb254-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="fb254-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb254-113">PARAMETERS</span></span>

### <span data-ttu-id="fb254-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb254-114">-AsJob</span></span>
<span data-ttu-id="fb254-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fb254-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb254-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb254-116">-DefaultProfile</span></span>
<span data-ttu-id="fb254-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb254-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb254-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="fb254-118">-Description</span></span>
<span data-ttu-id="fb254-119">Beskrivning av bild definitions resursen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="fb254-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="fb254-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="fb254-120">-DisallowedDiskType</span></span>
<span data-ttu-id="fb254-121">De otillåtna disk typerna.</span><span class="sxs-lookup"><span data-stu-id="fb254-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="fb254-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="fb254-122">-EndOfLifeDate</span></span>
<span data-ttu-id="fb254-123">Livs cykel datum för bild definitionen för galleriet</span><span class="sxs-lookup"><span data-stu-id="fb254-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="fb254-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="fb254-124">-Eula</span></span>
<span data-ttu-id="fb254-125">EULA-avtalet för bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="fb254-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="fb254-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="fb254-126">-GalleryName</span></span>
<span data-ttu-id="fb254-127">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="fb254-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="fb254-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb254-128">-InputObject</span></span>
<span data-ttu-id="fb254-129">Bild definitions objekt för PS-galleriet.</span><span class="sxs-lookup"><span data-stu-id="fb254-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="fb254-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="fb254-130">-MaximumMemory</span></span>
<span data-ttu-id="fb254-131">Det högsta av det rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="fb254-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="fb254-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="fb254-132">-MaximumVCPU</span></span>
<span data-ttu-id="fb254-133">Max för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="fb254-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="fb254-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="fb254-134">-MinimumMemory</span></span>
<span data-ttu-id="fb254-135">Det minsta rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="fb254-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="fb254-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="fb254-136">-MinimumVCPU</span></span>
<span data-ttu-id="fb254-137">Minimum för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="fb254-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="fb254-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb254-138">-Name</span></span>
<span data-ttu-id="fb254-139">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="fb254-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="fb254-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="fb254-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="fb254-141">URL för integritets policyn.</span><span class="sxs-lookup"><span data-stu-id="fb254-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="fb254-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="fb254-142">-PurchasePlanName</span></span>
<span data-ttu-id="fb254-143">ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="fb254-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fb254-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="fb254-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="fb254-145">Produkt-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="fb254-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fb254-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="fb254-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="fb254-147">Publisher-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="fb254-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fb254-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="fb254-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="fb254-149">URI för release Note.</span><span class="sxs-lookup"><span data-stu-id="fb254-149">The release note uri.</span></span>

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

### <span data-ttu-id="fb254-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb254-150">-ResourceGroupName</span></span>
<span data-ttu-id="fb254-151">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fb254-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="fb254-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb254-152">-ResourceId</span></span>
<span data-ttu-id="fb254-153">Resurs-ID för bild definitionen</span><span class="sxs-lookup"><span data-stu-id="fb254-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="fb254-154">-Tagg</span><span class="sxs-lookup"><span data-stu-id="fb254-154">-Tag</span></span>
<span data-ttu-id="fb254-155">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="fb254-155">Resource tags</span></span>

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

### <span data-ttu-id="fb254-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb254-156">-Confirm</span></span>
<span data-ttu-id="fb254-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb254-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb254-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb254-158">-WhatIf</span></span>
<span data-ttu-id="fb254-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb254-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb254-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb254-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb254-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb254-161">CommonParameters</span></span>
<span data-ttu-id="fb254-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb254-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb254-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb254-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb254-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb254-164">INPUTS</span></span>

### <span data-ttu-id="fb254-165">System. String</span><span class="sxs-lookup"><span data-stu-id="fb254-165">System.String</span></span>

### <span data-ttu-id="fb254-166">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="fb254-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="fb254-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="fb254-167">System.DateTime</span></span>

### <span data-ttu-id="fb254-168">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="fb254-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fb254-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fb254-169">System.Int32</span></span>

### <span data-ttu-id="fb254-170">System. string []</span><span class="sxs-lookup"><span data-stu-id="fb254-170">System.String[]</span></span>

## <span data-ttu-id="fb254-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb254-171">OUTPUTS</span></span>

### <span data-ttu-id="fb254-172">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="fb254-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="fb254-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb254-173">NOTES</span></span>

## <span data-ttu-id="fb254-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb254-174">RELATED LINKS</span></span>