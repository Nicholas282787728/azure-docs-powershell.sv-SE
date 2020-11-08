---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088290"
---
# <span data-ttu-id="accde-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="accde-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="accde-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="accde-102">SYNOPSIS</span></span>
<span data-ttu-id="accde-103">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="accde-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="accde-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="accde-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="accde-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="accde-105">DESCRIPTION</span></span>
<span data-ttu-id="accde-106">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="accde-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="accde-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="accde-107">EXAMPLES</span></span>

### <span data-ttu-id="accde-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="accde-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="accde-109">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="accde-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="accde-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="accde-110">PARAMETERS</span></span>

### <span data-ttu-id="accde-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="accde-111">-AsJob</span></span>
<span data-ttu-id="accde-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="accde-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="accde-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="accde-113">-DefaultProfile</span></span>
<span data-ttu-id="accde-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="accde-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="accde-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="accde-115">-Description</span></span>
<span data-ttu-id="accde-116">Beskrivning av bild definitions resursen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="accde-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="accde-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="accde-117">-DisallowedDiskType</span></span>
<span data-ttu-id="accde-118">De otillåtna disk typerna.</span><span class="sxs-lookup"><span data-stu-id="accde-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="accde-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="accde-119">-EndOfLifeDate</span></span>
<span data-ttu-id="accde-120">Livs cykel datum för bild definitionen för galleriet</span><span class="sxs-lookup"><span data-stu-id="accde-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="accde-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="accde-121">-Eula</span></span>
<span data-ttu-id="accde-122">EULA-avtalet för bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="accde-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="accde-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="accde-123">-GalleryName</span></span>
<span data-ttu-id="accde-124">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="accde-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="accde-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="accde-125">-HyperVGeneration</span></span>
<span data-ttu-id="accde-126">Hypervisor-generering av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="accde-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="accde-127">Gäller endast för OS-diskar.</span><span class="sxs-lookup"><span data-stu-id="accde-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="accde-128">Tillåtna värden är v1 och v2.</span><span class="sxs-lookup"><span data-stu-id="accde-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="accde-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="accde-129">-Location</span></span>
<span data-ttu-id="accde-130">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="accde-130">Resource location</span></span>

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

### <span data-ttu-id="accde-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="accde-131">-MaximumMemory</span></span>
<span data-ttu-id="accde-132">Det högsta av det rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="accde-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="accde-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="accde-133">-MaximumVCPU</span></span>
<span data-ttu-id="accde-134">Max för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="accde-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="accde-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="accde-135">-MinimumMemory</span></span>
<span data-ttu-id="accde-136">Det minsta rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="accde-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="accde-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="accde-137">-MinimumVCPU</span></span>
<span data-ttu-id="accde-138">Minimum för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="accde-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="accde-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="accde-139">-Name</span></span>
<span data-ttu-id="accde-140">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="accde-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="accde-141">-Ge</span><span class="sxs-lookup"><span data-stu-id="accde-141">-Offer</span></span>
<span data-ttu-id="accde-142">Namnet på galleriet med bild definitions förslag.</span><span class="sxs-lookup"><span data-stu-id="accde-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="accde-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="accde-143">-OsState</span></span>
<span data-ttu-id="accde-144">Tillståndet för operativ systemet</span><span class="sxs-lookup"><span data-stu-id="accde-144">The state of OS</span></span>

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

### <span data-ttu-id="accde-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="accde-145">-OsType</span></span>
<span data-ttu-id="accde-146">OS-typen</span><span class="sxs-lookup"><span data-stu-id="accde-146">The type of OS</span></span>

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

### <span data-ttu-id="accde-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="accde-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="accde-148">URL för integritets policyn.</span><span class="sxs-lookup"><span data-stu-id="accde-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="accde-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="accde-149">-Publisher</span></span>
<span data-ttu-id="accde-150">Namnet på Galleri bild definitions utgivaren.</span><span class="sxs-lookup"><span data-stu-id="accde-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="accde-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="accde-151">-PurchasePlanName</span></span>
<span data-ttu-id="accde-152">ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="accde-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="accde-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="accde-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="accde-154">Produkt-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="accde-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="accde-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="accde-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="accde-156">Publisher-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="accde-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="accde-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="accde-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="accde-158">URI för release Note.</span><span class="sxs-lookup"><span data-stu-id="accde-158">The release note uri.</span></span>

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

### <span data-ttu-id="accde-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="accde-159">-ResourceGroupName</span></span>
<span data-ttu-id="accde-160">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="accde-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="accde-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="accde-161">-Sku</span></span>
<span data-ttu-id="accde-162">Namnet på bild definitions filen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="accde-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="accde-163">-Tagg</span><span class="sxs-lookup"><span data-stu-id="accde-163">-Tag</span></span>
<span data-ttu-id="accde-164">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="accde-164">Resource tags</span></span>

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

### <span data-ttu-id="accde-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="accde-165">-Confirm</span></span>
<span data-ttu-id="accde-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="accde-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="accde-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="accde-167">-WhatIf</span></span>
<span data-ttu-id="accde-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="accde-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="accde-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="accde-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="accde-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="accde-170">CommonParameters</span></span>
<span data-ttu-id="accde-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="accde-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="accde-172">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="accde-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="accde-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="accde-173">INPUTS</span></span>

### <span data-ttu-id="accde-174">System. String</span><span class="sxs-lookup"><span data-stu-id="accde-174">System.String</span></span>

### <span data-ttu-id="accde-175">Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="accde-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="accde-176">Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="accde-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="accde-177">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="accde-177">System.DateTime</span></span>

### <span data-ttu-id="accde-178">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="accde-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="accde-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="accde-179">System.Int32</span></span>

### <span data-ttu-id="accde-180">System. string []</span><span class="sxs-lookup"><span data-stu-id="accde-180">System.String[]</span></span>

## <span data-ttu-id="accde-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="accde-181">OUTPUTS</span></span>

### <span data-ttu-id="accde-182">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="accde-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="accde-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="accde-183">NOTES</span></span>

## <span data-ttu-id="accde-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="accde-184">RELATED LINKS</span></span>
