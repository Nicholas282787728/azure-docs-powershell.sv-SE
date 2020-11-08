---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090307"
---
# <span data-ttu-id="70f6f-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="70f6f-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="70f6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="70f6f-103">Uppdatera en bild version i galleriet.</span><span class="sxs-lookup"><span data-stu-id="70f6f-103">Update a gallery image version.</span></span>

## <span data-ttu-id="70f6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70f6f-104">SYNTAX</span></span>

### <span data-ttu-id="70f6f-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="70f6f-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70f6f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="70f6f-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70f6f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="70f6f-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70f6f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70f6f-108">DESCRIPTION</span></span>
<span data-ttu-id="70f6f-109">Uppdatera en bild version i galleriet.</span><span class="sxs-lookup"><span data-stu-id="70f6f-109">Update a gallery image version.</span></span>

## <span data-ttu-id="70f6f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70f6f-110">EXAMPLES</span></span>

### <span data-ttu-id="70f6f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="70f6f-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="70f6f-112">Uppdatera en bild version i galleriet.</span><span class="sxs-lookup"><span data-stu-id="70f6f-112">Update a gallery image version.</span></span>

## <span data-ttu-id="70f6f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70f6f-113">PARAMETERS</span></span>

### <span data-ttu-id="70f6f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70f6f-114">-AsJob</span></span>
<span data-ttu-id="70f6f-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="70f6f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70f6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f6f-116">-DefaultProfile</span></span>
<span data-ttu-id="70f6f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70f6f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70f6f-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="70f6f-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="70f6f-119">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="70f6f-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="70f6f-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="70f6f-120">-GalleryName</span></span>
<span data-ttu-id="70f6f-121">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="70f6f-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="70f6f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70f6f-122">-InputObject</span></span>
<span data-ttu-id="70f6f-123">Versions objekt för PS-galleriet.</span><span class="sxs-lookup"><span data-stu-id="70f6f-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="70f6f-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="70f6f-124">-Name</span></span>
<span data-ttu-id="70f6f-125">Namnet på Galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="70f6f-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="70f6f-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="70f6f-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="70f6f-127">Livs cykel datum för bild versionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="70f6f-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="70f6f-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="70f6f-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="70f6f-129">Om den är angiven kommer virtuella datorer som distribueras från den senaste versionen av bild definitionen inte att använda denna bild version.</span><span class="sxs-lookup"><span data-stu-id="70f6f-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="70f6f-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="70f6f-130">-ReplicaCount</span></span>
<span data-ttu-id="70f6f-131">Antalet repliker av den bild version som ska skapas per region.</span><span class="sxs-lookup"><span data-stu-id="70f6f-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="70f6f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f6f-132">-ResourceGroupName</span></span>
<span data-ttu-id="70f6f-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="70f6f-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="70f6f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70f6f-134">-ResourceId</span></span>
<span data-ttu-id="70f6f-135">Resurs-ID för galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="70f6f-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="70f6f-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="70f6f-136">-Tag</span></span>
<span data-ttu-id="70f6f-137">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="70f6f-137">Resource tags</span></span>

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

### <span data-ttu-id="70f6f-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="70f6f-138">-TargetRegion</span></span>
<span data-ttu-id="70f6f-139">De mål områden där bild versionen ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="70f6f-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="70f6f-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70f6f-140">-Confirm</span></span>
<span data-ttu-id="70f6f-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70f6f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f6f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f6f-142">-WhatIf</span></span>
<span data-ttu-id="70f6f-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70f6f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70f6f-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70f6f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70f6f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f6f-145">CommonParameters</span></span>
<span data-ttu-id="70f6f-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70f6f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f6f-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70f6f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f6f-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70f6f-148">INPUTS</span></span>

### <span data-ttu-id="70f6f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="70f6f-149">System.String</span></span>

### <span data-ttu-id="70f6f-150">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="70f6f-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="70f6f-151">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="70f6f-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="70f6f-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="70f6f-152">System.Int32</span></span>

### <span data-ttu-id="70f6f-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="70f6f-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="70f6f-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="70f6f-154">System.DateTime</span></span>

### <span data-ttu-id="70f6f-155">System. Collections. hash-program []</span><span class="sxs-lookup"><span data-stu-id="70f6f-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="70f6f-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70f6f-156">OUTPUTS</span></span>

### <span data-ttu-id="70f6f-157">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="70f6f-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="70f6f-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70f6f-158">NOTES</span></span>

## <span data-ttu-id="70f6f-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70f6f-159">RELATED LINKS</span></span>