---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 1385d4fe93157715ffdd521cfb62ed963b86e1ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392936"
---
# <span data-ttu-id="5ea6f-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5ea6f-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="5ea6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ea6f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea6f-103">Bild versioner för hämta eller lista</span><span class="sxs-lookup"><span data-stu-id="5ea6f-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="5ea6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ea6f-104">SYNTAX</span></span>

### <span data-ttu-id="5ea6f-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="5ea6f-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ea6f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="5ea6f-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ea6f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ea6f-107">DESCRIPTION</span></span>
<span data-ttu-id="5ea6f-108">Bild versioner för hämta eller lista</span><span class="sxs-lookup"><span data-stu-id="5ea6f-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="5ea6f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ea6f-109">EXAMPLES</span></span>

### <span data-ttu-id="5ea6f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5ea6f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1.0.0

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="5ea6f-111">Hämta bild versionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="5ea6f-111">Get the gallery image version.</span></span>

### <span data-ttu-id="5ea6f-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5ea6f-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1*

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="5ea6f-113">Hämta bild versioner för galleriet som börjar med "1".</span><span class="sxs-lookup"><span data-stu-id="5ea6f-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="5ea6f-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="5ea6f-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="5ea6f-115">Hämta alla bild versioner av galleriet.</span><span class="sxs-lookup"><span data-stu-id="5ea6f-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="5ea6f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ea6f-116">PARAMETERS</span></span>

### <span data-ttu-id="5ea6f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea6f-117">-DefaultProfile</span></span>
<span data-ttu-id="5ea6f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea6f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ea6f-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="5ea6f-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="5ea6f-120">Visa replikeringsstatus.</span><span class="sxs-lookup"><span data-stu-id="5ea6f-120">Show replication status.</span></span>

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

### <span data-ttu-id="5ea6f-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="5ea6f-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="5ea6f-122">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="5ea6f-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="5ea6f-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="5ea6f-123">-GalleryName</span></span>
<span data-ttu-id="5ea6f-124">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="5ea6f-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="5ea6f-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ea6f-125">-Name</span></span>
<span data-ttu-id="5ea6f-126">Namnet på Galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="5ea6f-126">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5ea6f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea6f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ea6f-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5ea6f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="5ea6f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ea6f-129">-ResourceId</span></span>
<span data-ttu-id="5ea6f-130">Resurs-ID för galleri bild versionen</span><span class="sxs-lookup"><span data-stu-id="5ea6f-130">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="5ea6f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea6f-131">CommonParameters</span></span>
<span data-ttu-id="5ea6f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ea6f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea6f-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ea6f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea6f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ea6f-134">INPUTS</span></span>

### <span data-ttu-id="5ea6f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5ea6f-135">System.String</span></span>

### <span data-ttu-id="5ea6f-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5ea6f-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5ea6f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ea6f-137">OUTPUTS</span></span>

### <span data-ttu-id="5ea6f-138">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5ea6f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="5ea6f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ea6f-139">NOTES</span></span>

## <span data-ttu-id="5ea6f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ea6f-140">RELATED LINKS</span></span>
