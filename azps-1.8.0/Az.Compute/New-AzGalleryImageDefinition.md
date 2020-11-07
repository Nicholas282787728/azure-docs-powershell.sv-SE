---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: 7959f11931b815a8e096cf9b5223064aa3554757
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917374"
---
# <span data-ttu-id="ddd97-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="ddd97-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="ddd97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddd97-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd97-103">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="ddd97-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="ddd97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddd97-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>]
 [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>]
 [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd97-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddd97-105">DESCRIPTION</span></span>
<span data-ttu-id="ddd97-106">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="ddd97-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="ddd97-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddd97-107">EXAMPLES</span></span>

### <span data-ttu-id="ddd97-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ddd97-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="ddd97-109">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="ddd97-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="ddd97-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddd97-110">PARAMETERS</span></span>

### <span data-ttu-id="ddd97-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddd97-111">-AsJob</span></span>
<span data-ttu-id="ddd97-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ddd97-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddd97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd97-113">-DefaultProfile</span></span>
<span data-ttu-id="ddd97-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd97-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddd97-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ddd97-115">-Description</span></span>
<span data-ttu-id="ddd97-116">Beskrivning av bild definitions resursen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="ddd97-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="ddd97-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="ddd97-117">-DisallowedDiskType</span></span>
<span data-ttu-id="ddd97-118">De otillåtna disk typerna.</span><span class="sxs-lookup"><span data-stu-id="ddd97-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="ddd97-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="ddd97-119">-EndOfLifeDate</span></span>
<span data-ttu-id="ddd97-120">Livs cykel datum för bild definitionen för galleriet</span><span class="sxs-lookup"><span data-stu-id="ddd97-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="ddd97-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="ddd97-121">-Eula</span></span>
<span data-ttu-id="ddd97-122">EULA-avtalet för bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="ddd97-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="ddd97-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="ddd97-123">-GalleryName</span></span>
<span data-ttu-id="ddd97-124">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="ddd97-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="ddd97-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="ddd97-125">-Location</span></span>
<span data-ttu-id="ddd97-126">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="ddd97-126">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="ddd97-127">-MaximumMemory</span></span>
<span data-ttu-id="ddd97-128">Det högsta av det rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="ddd97-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="ddd97-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="ddd97-129">-MaximumVCPU</span></span>
<span data-ttu-id="ddd97-130">Max för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="ddd97-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="ddd97-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="ddd97-131">-MinimumMemory</span></span>
<span data-ttu-id="ddd97-132">Det minsta rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="ddd97-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="ddd97-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="ddd97-133">-MinimumVCPU</span></span>
<span data-ttu-id="ddd97-134">Minimum för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="ddd97-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="ddd97-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="ddd97-135">-Name</span></span>
<span data-ttu-id="ddd97-136">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="ddd97-136">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-137">-Ge</span><span class="sxs-lookup"><span data-stu-id="ddd97-137">-Offer</span></span>
<span data-ttu-id="ddd97-138">Namnet på galleriet med bild definitions förslag.</span><span class="sxs-lookup"><span data-stu-id="ddd97-138">The name of the gallery Image Definition offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="ddd97-139">-OsState</span></span>
<span data-ttu-id="ddd97-140">Tillståndet för operativ systemet</span><span class="sxs-lookup"><span data-stu-id="ddd97-140">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="ddd97-141">-OsType</span></span>
<span data-ttu-id="ddd97-142">OS-typen</span><span class="sxs-lookup"><span data-stu-id="ddd97-142">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="ddd97-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="ddd97-144">URL för integritets policyn.</span><span class="sxs-lookup"><span data-stu-id="ddd97-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="ddd97-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ddd97-145">-Publisher</span></span>
<span data-ttu-id="ddd97-146">Namnet på Galleri bild definitions utgivaren.</span><span class="sxs-lookup"><span data-stu-id="ddd97-146">The name of the gallery Image Definition publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="ddd97-147">-PurchasePlanName</span></span>
<span data-ttu-id="ddd97-148">ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="ddd97-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ddd97-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="ddd97-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="ddd97-150">Produkt-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="ddd97-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ddd97-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ddd97-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="ddd97-152">Publisher-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="ddd97-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ddd97-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="ddd97-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="ddd97-154">URI för release Note.</span><span class="sxs-lookup"><span data-stu-id="ddd97-154">The release note uri.</span></span>

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

### <span data-ttu-id="ddd97-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd97-155">-ResourceGroupName</span></span>
<span data-ttu-id="ddd97-156">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ddd97-156">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="ddd97-157">-Sku</span></span>
<span data-ttu-id="ddd97-158">Namnet på bild definitions filen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="ddd97-158">The name of the gallery Image Definition SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd97-159">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ddd97-159">-Tag</span></span>
<span data-ttu-id="ddd97-160">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="ddd97-160">Resource tags</span></span>

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

### <span data-ttu-id="ddd97-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ddd97-161">-Confirm</span></span>
<span data-ttu-id="ddd97-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ddd97-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd97-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd97-163">-WhatIf</span></span>
<span data-ttu-id="ddd97-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ddd97-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd97-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ddd97-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd97-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd97-166">CommonParameters</span></span>
<span data-ttu-id="ddd97-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd97-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd97-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd97-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd97-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddd97-169">INPUTS</span></span>

### <span data-ttu-id="ddd97-170">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd97-170">System.String</span></span>

### <span data-ttu-id="ddd97-171">Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="ddd97-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="ddd97-172">Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="ddd97-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="ddd97-173">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="ddd97-173">System.DateTime</span></span>

### <span data-ttu-id="ddd97-174">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ddd97-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ddd97-175">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ddd97-175">System.Int32</span></span>

### <span data-ttu-id="ddd97-176">System. string []</span><span class="sxs-lookup"><span data-stu-id="ddd97-176">System.String[]</span></span>

## <span data-ttu-id="ddd97-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddd97-177">OUTPUTS</span></span>

### <span data-ttu-id="ddd97-178">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="ddd97-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="ddd97-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddd97-179">NOTES</span></span>

## <span data-ttu-id="ddd97-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddd97-180">RELATED LINKS</span></span>
