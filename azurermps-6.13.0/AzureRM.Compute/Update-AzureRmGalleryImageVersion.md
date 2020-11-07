---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageVersion.md
ms.openlocfilehash: e8c50ffb2ac60c65f64806781d9155600c9bbe0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756218"
---
# <span data-ttu-id="a3dfa-101">Update-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a3dfa-101">Update-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="a3dfa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="a3dfa-103">Uppdatera en bild version i galleriet.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-103">Update a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3dfa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3dfa-104">SYNTAX</span></span>

### <span data-ttu-id="a3dfa-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="a3dfa-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-Tag <Hashtable>] [-ReplicaCount <Int32>]
 [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3dfa-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a3dfa-106">ResourceIdParameter</span></span>
```
Update-AzureRmGalleryImageVersion [-ResourceId] <String> [-AsJob] [-Tag <Hashtable>] [-ReplicaCount <Int32>]
 [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3dfa-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a3dfa-107">ObjectParameter</span></span>
```
Update-AzureRmGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob] [-Tag <Hashtable>]
 [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3dfa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3dfa-108">DESCRIPTION</span></span>
<span data-ttu-id="a3dfa-109">Uppdatera en bild version i galleriet.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-109">Update a gallery image version.</span></span>

## <span data-ttu-id="a3dfa-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3dfa-110">EXAMPLES</span></span>

### <span data-ttu-id="a3dfa-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a3dfa-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="a3dfa-112">Uppdatera en bild version i galleriet.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-112">Update a gallery image version.</span></span>

## <span data-ttu-id="a3dfa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3dfa-113">PARAMETERS</span></span>

### <span data-ttu-id="a3dfa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3dfa-114">-AsJob</span></span>
<span data-ttu-id="a3dfa-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a3dfa-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3dfa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3dfa-116">-DefaultProfile</span></span>
<span data-ttu-id="a3dfa-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3dfa-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a3dfa-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="a3dfa-119">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="a3dfa-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="a3dfa-120">-GalleryName</span></span>
<span data-ttu-id="a3dfa-121">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="a3dfa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3dfa-122">-InputObject</span></span>
<span data-ttu-id="a3dfa-123">Versions objekt för PS-galleriet.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="a3dfa-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3dfa-124">-Name</span></span>
<span data-ttu-id="a3dfa-125">Namnet på Galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="a3dfa-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="a3dfa-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="a3dfa-127">Livs cykel datum för bild versionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="a3dfa-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="a3dfa-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="a3dfa-129">Om den är angiven kommer virtuella datorer som distribueras från den senaste versionen av bild definitionen inte att använda denna bild version.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3dfa-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="a3dfa-130">-ReplicaCount</span></span>
<span data-ttu-id="a3dfa-131">Antalet repliker av den bild version som ska skapas per region.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="a3dfa-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3dfa-132">-ResourceGroupName</span></span>
<span data-ttu-id="a3dfa-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="a3dfa-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3dfa-134">-ResourceId</span></span>
<span data-ttu-id="a3dfa-135">Resurs-ID för galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="a3dfa-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a3dfa-136">-Tag</span></span>
<span data-ttu-id="a3dfa-137">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="a3dfa-137">Resource tags</span></span>

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

### <span data-ttu-id="a3dfa-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="a3dfa-138">-TargetRegion</span></span>
<span data-ttu-id="a3dfa-139">De mål områden där bild versionen ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-139">The target regions where the Image Version is going to be replicated to.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3dfa-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3dfa-140">-Confirm</span></span>
<span data-ttu-id="a3dfa-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3dfa-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3dfa-142">-WhatIf</span></span>
<span data-ttu-id="a3dfa-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3dfa-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3dfa-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3dfa-145">CommonParameters</span></span>
<span data-ttu-id="a3dfa-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3dfa-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3dfa-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3dfa-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3dfa-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3dfa-148">INPUTS</span></span>

### <span data-ttu-id="a3dfa-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a3dfa-149">System.String</span></span>

### <span data-ttu-id="a3dfa-150">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a3dfa-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="a3dfa-151">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a3dfa-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a3dfa-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a3dfa-152">System.Int32</span></span>

### <span data-ttu-id="a3dfa-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a3dfa-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a3dfa-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="a3dfa-154">System.DateTime</span></span>

### <span data-ttu-id="a3dfa-155">System. Collections. hash-program []</span><span class="sxs-lookup"><span data-stu-id="a3dfa-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="a3dfa-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3dfa-156">OUTPUTS</span></span>

### <span data-ttu-id="a3dfa-157">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a3dfa-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="a3dfa-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3dfa-158">NOTES</span></span>

## <span data-ttu-id="a3dfa-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3dfa-159">RELATED LINKS</span></span>
