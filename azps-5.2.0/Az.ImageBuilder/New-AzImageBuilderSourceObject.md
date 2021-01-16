---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397168"
---
# <span data-ttu-id="44069-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="44069-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="44069-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44069-102">SYNOPSIS</span></span>
<span data-ttu-id="44069-103">Beskriver en virtuell dator bild källa för att bygga, anpassa och distribuera.</span><span class="sxs-lookup"><span data-stu-id="44069-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="44069-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44069-104">SYNTAX</span></span>

### <span data-ttu-id="44069-105">ManagedImage (standard)</span><span class="sxs-lookup"><span data-stu-id="44069-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="44069-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="44069-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="44069-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="44069-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="44069-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="44069-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="44069-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44069-109">DESCRIPTION</span></span>
<span data-ttu-id="44069-110">Beskriver en virtuell dator bild källa för att bygga, anpassa och distribuera.</span><span class="sxs-lookup"><span data-stu-id="44069-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="44069-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44069-111">EXAMPLES</span></span>

### <span data-ttu-id="44069-112">Exempel 1: skapa en hanterad bild källa</span><span class="sxs-lookup"><span data-stu-id="44069-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="44069-113">Det här kommandot skapar en hanterad bild källa.</span><span class="sxs-lookup"><span data-stu-id="44069-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="44069-114">Exempel 2: skapa en delad bild källa</span><span class="sxs-lookup"><span data-stu-id="44069-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="44069-115">Det här kommandot skapar en delad bild källa.</span><span class="sxs-lookup"><span data-stu-id="44069-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="44069-116">Exempel 3: skapa en platfrom</span><span class="sxs-lookup"><span data-stu-id="44069-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="44069-117">Det här kommandot skapar en platfrom-bildkälla.</span><span class="sxs-lookup"><span data-stu-id="44069-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="44069-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44069-118">PARAMETERS</span></span>

### <span data-ttu-id="44069-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="44069-119">-ImageId</span></span>
<span data-ttu-id="44069-120">ARM-resurs-ID för den hanterade bilden i kund abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="44069-120">ARM resource id of the managed image in customer subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="44069-121">-ImageVersionId</span></span>
<span data-ttu-id="44069-122">ARM-resurs-ID för bild versionen i galleriet för delad bild.</span><span class="sxs-lookup"><span data-stu-id="44069-122">ARM resource id of the image version in the shared image gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-123">-Ge</span><span class="sxs-lookup"><span data-stu-id="44069-123">-Offer</span></span>
<span data-ttu-id="44069-124">Bild från [Azure Gallery-bilder](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="44069-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="44069-125">-PlanName</span></span>
<span data-ttu-id="44069-126">Namn på inköps planen.</span><span class="sxs-lookup"><span data-stu-id="44069-126">Name of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="44069-127">-PlanProduct</span></span>
<span data-ttu-id="44069-128">Inköps planens produkt.</span><span class="sxs-lookup"><span data-stu-id="44069-128">Product of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="44069-129">-PlanPublisher</span></span>
<span data-ttu-id="44069-130">Utgivare av inköps planen.</span><span class="sxs-lookup"><span data-stu-id="44069-130">Publisher of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="44069-131">-Publisher</span></span>
<span data-ttu-id="44069-132">Bild utgivare i [Azure Gallery-bilder](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="44069-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="44069-133">-Sku</span></span>
<span data-ttu-id="44069-134">Bild-SKU från [Azure Gallery-bilder](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="44069-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="44069-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="44069-136">Beskriver en bild källa som är en hanterad bild i kund abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="44069-136">Describes an image source that is a managed image in customer subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="44069-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="44069-138">Beskriver en bild källa från [Azure Gallery-bilder](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="44069-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="44069-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="44069-140">Beskriver en bild källa som är en bild version i ett galleri för delade bilder.</span><span class="sxs-lookup"><span data-stu-id="44069-140">Describes an image source that is an image version in a shared image gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-141">-Version</span><span class="sxs-lookup"><span data-stu-id="44069-141">-Version</span></span>
<span data-ttu-id="44069-142">Bild version från [bilder i Azure-galleriet](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="44069-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44069-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44069-143">CommonParameters</span></span>
<span data-ttu-id="44069-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44069-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44069-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44069-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44069-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44069-146">INPUTS</span></span>

## <span data-ttu-id="44069-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44069-147">OUTPUTS</span></span>

### <span data-ttu-id="44069-148">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. Api20200214. IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="44069-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="44069-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44069-149">NOTES</span></span>

<span data-ttu-id="44069-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="44069-150">ALIASES</span></span>

## <span data-ttu-id="44069-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44069-151">RELATED LINKS</span></span>

