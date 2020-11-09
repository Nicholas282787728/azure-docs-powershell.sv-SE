---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325332"
---
# <span data-ttu-id="894ab-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="894ab-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="894ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="894ab-102">SYNOPSIS</span></span>
<span data-ttu-id="894ab-103">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="894ab-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="894ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="894ab-104">SYNTAX</span></span>

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

## <span data-ttu-id="894ab-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="894ab-105">DESCRIPTION</span></span>
<span data-ttu-id="894ab-106">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="894ab-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="894ab-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="894ab-107">EXAMPLES</span></span>

### <span data-ttu-id="894ab-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="894ab-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="894ab-109">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="894ab-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="894ab-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="894ab-110">PARAMETERS</span></span>

### <span data-ttu-id="894ab-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="894ab-111">-AsJob</span></span>
<span data-ttu-id="894ab-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="894ab-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="894ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894ab-113">-DefaultProfile</span></span>
<span data-ttu-id="894ab-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="894ab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="894ab-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="894ab-115">-Description</span></span>
<span data-ttu-id="894ab-116">Beskrivning av bild definitions resursen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="894ab-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="894ab-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="894ab-117">-DisallowedDiskType</span></span>
<span data-ttu-id="894ab-118">De otillåtna disk typerna.</span><span class="sxs-lookup"><span data-stu-id="894ab-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="894ab-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="894ab-119">-EndOfLifeDate</span></span>
<span data-ttu-id="894ab-120">Livs cykel datum för bild definitionen för galleriet</span><span class="sxs-lookup"><span data-stu-id="894ab-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="894ab-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="894ab-121">-Eula</span></span>
<span data-ttu-id="894ab-122">EULA-avtalet för bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="894ab-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="894ab-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="894ab-123">-GalleryName</span></span>
<span data-ttu-id="894ab-124">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="894ab-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="894ab-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="894ab-125">-HyperVGeneration</span></span>
<span data-ttu-id="894ab-126">Hypervisor-generering av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="894ab-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="894ab-127">Gäller endast för OS-diskar.</span><span class="sxs-lookup"><span data-stu-id="894ab-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="894ab-128">Tillåtna värden är v1 och v2.</span><span class="sxs-lookup"><span data-stu-id="894ab-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="894ab-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="894ab-129">-Location</span></span>
<span data-ttu-id="894ab-130">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="894ab-130">Resource location</span></span>

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

### <span data-ttu-id="894ab-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="894ab-131">-MaximumMemory</span></span>
<span data-ttu-id="894ab-132">Det högsta av det rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="894ab-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="894ab-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="894ab-133">-MaximumVCPU</span></span>
<span data-ttu-id="894ab-134">Max för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="894ab-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="894ab-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="894ab-135">-MinimumMemory</span></span>
<span data-ttu-id="894ab-136">Det minsta rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="894ab-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="894ab-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="894ab-137">-MinimumVCPU</span></span>
<span data-ttu-id="894ab-138">Minimum för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="894ab-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="894ab-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="894ab-139">-Name</span></span>
<span data-ttu-id="894ab-140">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="894ab-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="894ab-141">-Ge</span><span class="sxs-lookup"><span data-stu-id="894ab-141">-Offer</span></span>
<span data-ttu-id="894ab-142">Namnet på galleriet med bild definitions förslag.</span><span class="sxs-lookup"><span data-stu-id="894ab-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="894ab-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="894ab-143">-OsState</span></span>
<span data-ttu-id="894ab-144">Tillståndet för operativ systemet</span><span class="sxs-lookup"><span data-stu-id="894ab-144">The state of OS</span></span>

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

### <span data-ttu-id="894ab-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="894ab-145">-OsType</span></span>
<span data-ttu-id="894ab-146">OS-typen</span><span class="sxs-lookup"><span data-stu-id="894ab-146">The type of OS</span></span>

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

### <span data-ttu-id="894ab-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="894ab-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="894ab-148">URL för integritets policyn.</span><span class="sxs-lookup"><span data-stu-id="894ab-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="894ab-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="894ab-149">-Publisher</span></span>
<span data-ttu-id="894ab-150">Namnet på Galleri bild definitions utgivaren.</span><span class="sxs-lookup"><span data-stu-id="894ab-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="894ab-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="894ab-151">-PurchasePlanName</span></span>
<span data-ttu-id="894ab-152">ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="894ab-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="894ab-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="894ab-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="894ab-154">Produkt-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="894ab-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="894ab-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="894ab-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="894ab-156">Publisher-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="894ab-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="894ab-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="894ab-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="894ab-158">URI för release Note.</span><span class="sxs-lookup"><span data-stu-id="894ab-158">The release note uri.</span></span>

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

### <span data-ttu-id="894ab-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="894ab-159">-ResourceGroupName</span></span>
<span data-ttu-id="894ab-160">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="894ab-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="894ab-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="894ab-161">-Sku</span></span>
<span data-ttu-id="894ab-162">Namnet på bild definitions filen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="894ab-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="894ab-163">-Tagg</span><span class="sxs-lookup"><span data-stu-id="894ab-163">-Tag</span></span>
<span data-ttu-id="894ab-164">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="894ab-164">Resource tags</span></span>

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

### <span data-ttu-id="894ab-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="894ab-165">-Confirm</span></span>
<span data-ttu-id="894ab-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="894ab-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="894ab-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="894ab-167">-WhatIf</span></span>
<span data-ttu-id="894ab-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="894ab-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="894ab-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="894ab-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="894ab-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894ab-170">CommonParameters</span></span>
<span data-ttu-id="894ab-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="894ab-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894ab-172">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="894ab-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894ab-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="894ab-173">INPUTS</span></span>

### <span data-ttu-id="894ab-174">System. String</span><span class="sxs-lookup"><span data-stu-id="894ab-174">System.String</span></span>

### <span data-ttu-id="894ab-175">Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="894ab-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="894ab-176">Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="894ab-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="894ab-177">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="894ab-177">System.DateTime</span></span>

### <span data-ttu-id="894ab-178">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="894ab-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="894ab-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="894ab-179">System.Int32</span></span>

### <span data-ttu-id="894ab-180">System. string []</span><span class="sxs-lookup"><span data-stu-id="894ab-180">System.String[]</span></span>

## <span data-ttu-id="894ab-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="894ab-181">OUTPUTS</span></span>

### <span data-ttu-id="894ab-182">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="894ab-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="894ab-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="894ab-183">NOTES</span></span>

## <span data-ttu-id="894ab-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="894ab-184">RELATED LINKS</span></span>
