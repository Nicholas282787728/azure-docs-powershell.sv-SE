---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 8dcfe4adedd7da375e888dade108125d7899d7d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585075"
---
# <span data-ttu-id="06c1f-101">New-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="06c1f-101">New-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="06c1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="06c1f-103">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="06c1f-103">Create a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06c1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06c1f-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Location] <String> -Publisher <String> -Offer <String> -Sku <String>
 -OsState <OperatingSystemStateTypes> -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06c1f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="06c1f-106">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="06c1f-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="06c1f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06c1f-107">EXAMPLES</span></span>

### <span data-ttu-id="06c1f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06c1f-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="06c1f-109">Skapa en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="06c1f-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="06c1f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06c1f-110">PARAMETERS</span></span>

### <span data-ttu-id="06c1f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06c1f-111">-AsJob</span></span>
<span data-ttu-id="06c1f-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="06c1f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06c1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c1f-113">-DefaultProfile</span></span>
<span data-ttu-id="06c1f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06c1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06c1f-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="06c1f-115">-Description</span></span>
<span data-ttu-id="06c1f-116">Beskrivning av bild definitions resursen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="06c1f-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="06c1f-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="06c1f-117">-DisallowedDiskType</span></span>
<span data-ttu-id="06c1f-118">De otillåtna disk typerna.</span><span class="sxs-lookup"><span data-stu-id="06c1f-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="06c1f-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="06c1f-119">-EndOfLifeDate</span></span>
<span data-ttu-id="06c1f-120">Livs cykel datum för bild definitionen för galleriet</span><span class="sxs-lookup"><span data-stu-id="06c1f-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="06c1f-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="06c1f-121">-Eula</span></span>
<span data-ttu-id="06c1f-122">EULA-avtalet för bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="06c1f-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="06c1f-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="06c1f-123">-GalleryName</span></span>
<span data-ttu-id="06c1f-124">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="06c1f-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="06c1f-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="06c1f-125">-Location</span></span>
<span data-ttu-id="06c1f-126">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="06c1f-126">Resource location</span></span>

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

### <span data-ttu-id="06c1f-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="06c1f-127">-MaximumMemory</span></span>
<span data-ttu-id="06c1f-128">Det högsta av det rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="06c1f-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="06c1f-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="06c1f-129">-MaximumVCPU</span></span>
<span data-ttu-id="06c1f-130">Max för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="06c1f-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="06c1f-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="06c1f-131">-MinimumMemory</span></span>
<span data-ttu-id="06c1f-132">Det minsta rekommenderade minnet</span><span class="sxs-lookup"><span data-stu-id="06c1f-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="06c1f-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="06c1f-133">-MinimumVCPU</span></span>
<span data-ttu-id="06c1f-134">Minimum för Rekommenderad processor kärna</span><span class="sxs-lookup"><span data-stu-id="06c1f-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="06c1f-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="06c1f-135">-Name</span></span>
<span data-ttu-id="06c1f-136">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="06c1f-136">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="06c1f-137">-Ge</span><span class="sxs-lookup"><span data-stu-id="06c1f-137">-Offer</span></span>
<span data-ttu-id="06c1f-138">Namnet på galleriet med bild definitions förslag.</span><span class="sxs-lookup"><span data-stu-id="06c1f-138">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="06c1f-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="06c1f-139">-OsState</span></span>
<span data-ttu-id="06c1f-140">Tillståndet för operativ systemet</span><span class="sxs-lookup"><span data-stu-id="06c1f-140">The state of OS</span></span>

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

### <span data-ttu-id="06c1f-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="06c1f-141">-OsType</span></span>
<span data-ttu-id="06c1f-142">OS-typen</span><span class="sxs-lookup"><span data-stu-id="06c1f-142">The type of OS</span></span>

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

### <span data-ttu-id="06c1f-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="06c1f-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="06c1f-144">URL för integritets policyn.</span><span class="sxs-lookup"><span data-stu-id="06c1f-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="06c1f-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="06c1f-145">-Publisher</span></span>
<span data-ttu-id="06c1f-146">Namnet på Galleri bild definitions utgivaren.</span><span class="sxs-lookup"><span data-stu-id="06c1f-146">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="06c1f-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="06c1f-147">-PurchasePlanName</span></span>
<span data-ttu-id="06c1f-148">ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="06c1f-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="06c1f-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="06c1f-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="06c1f-150">Produkt-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="06c1f-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="06c1f-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="06c1f-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="06c1f-152">Publisher-ID för inköps planen.</span><span class="sxs-lookup"><span data-stu-id="06c1f-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="06c1f-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="06c1f-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="06c1f-154">URI för release Note.</span><span class="sxs-lookup"><span data-stu-id="06c1f-154">The release note uri.</span></span>

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

### <span data-ttu-id="06c1f-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06c1f-155">-ResourceGroupName</span></span>
<span data-ttu-id="06c1f-156">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="06c1f-156">The name of the resource group.</span></span>

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

### <span data-ttu-id="06c1f-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="06c1f-157">-Sku</span></span>
<span data-ttu-id="06c1f-158">Namnet på bild definitions filen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="06c1f-158">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="06c1f-159">-Tagg</span><span class="sxs-lookup"><span data-stu-id="06c1f-159">-Tag</span></span>
<span data-ttu-id="06c1f-160">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="06c1f-160">Resource tags</span></span>

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

### <span data-ttu-id="06c1f-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06c1f-161">-Confirm</span></span>
<span data-ttu-id="06c1f-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06c1f-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06c1f-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06c1f-163">-WhatIf</span></span>
<span data-ttu-id="06c1f-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06c1f-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06c1f-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06c1f-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06c1f-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c1f-166">CommonParameters</span></span>
<span data-ttu-id="06c1f-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06c1f-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c1f-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c1f-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c1f-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06c1f-169">INPUTS</span></span>

### <span data-ttu-id="06c1f-170">System. String</span><span class="sxs-lookup"><span data-stu-id="06c1f-170">System.String</span></span>

### <span data-ttu-id="06c1f-171">Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="06c1f-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="06c1f-172">Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="06c1f-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="06c1f-173">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="06c1f-173">System.DateTime</span></span>

### <span data-ttu-id="06c1f-174">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="06c1f-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="06c1f-175">System. Int32</span><span class="sxs-lookup"><span data-stu-id="06c1f-175">System.Int32</span></span>

### <span data-ttu-id="06c1f-176">System. string []</span><span class="sxs-lookup"><span data-stu-id="06c1f-176">System.String[]</span></span>

## <span data-ttu-id="06c1f-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06c1f-177">OUTPUTS</span></span>

### <span data-ttu-id="06c1f-178">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="06c1f-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="06c1f-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06c1f-179">NOTES</span></span>

## <span data-ttu-id="06c1f-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06c1f-180">RELATED LINKS</span></span>
