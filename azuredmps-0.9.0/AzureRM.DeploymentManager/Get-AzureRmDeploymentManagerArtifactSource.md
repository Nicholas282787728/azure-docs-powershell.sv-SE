---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93755012"
---
# <span data-ttu-id="9f65b-101">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9f65b-101">Get-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="9f65b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f65b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f65b-103">Hämtar en artefakt källa.</span><span class="sxs-lookup"><span data-stu-id="9f65b-103">Gets an artifact source.</span></span>

## <span data-ttu-id="9f65b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f65b-104">SYNTAX</span></span>

### <span data-ttu-id="9f65b-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="9f65b-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f65b-106">ID</span><span class="sxs-lookup"><span data-stu-id="9f65b-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f65b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9f65b-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f65b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f65b-108">DESCRIPTION</span></span>
<span data-ttu-id="9f65b-109">Cmdleten **Get-AzureRmDeploymentManagerArtifactSource** hämtar en artefakt källa och returnerar ett objekt som representerar den artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="9f65b-109">The **Get-AzureRmDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="9f65b-110">Ange artefakt källan med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9f65b-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="9f65b-111">Du kan också ange ArtifactSource-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9f65b-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

<span data-ttu-id="9f65b-112">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på artefakt källan med hjälp av Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f65b-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

## <span data-ttu-id="9f65b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f65b-113">EXAMPLES</span></span>

### <span data-ttu-id="9f65b-114">Exempel 1: Hämta en artefakt källa</span><span class="sxs-lookup"><span data-stu-id="9f65b-114">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="9f65b-115">Det här kommandot får en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9f65b-115">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="9f65b-116">Exempel 2: Hämta en artefakt källa med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="9f65b-116">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="9f65b-117">Det här kommandot får en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9f65b-117">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="9f65b-118">Exempel 3: Hämta en artefakt källa med ett objekt som returneras av New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9f65b-118">Example 3: Get an artifact source using an object returned by New-AzureRmDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="9f65b-119">Det här kommandot får en artefakt källa vars namn och ResourceGroup matchar $artifactSourceObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9f65b-119">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="9f65b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f65b-120">PARAMETERS</span></span>

### <span data-ttu-id="9f65b-121">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9f65b-121">-ArtifactSource</span></span>
<span data-ttu-id="9f65b-122">Objekt i artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="9f65b-122">Artifact Source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f65b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f65b-123">-DefaultProfile</span></span>
<span data-ttu-id="9f65b-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f65b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f65b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f65b-125">-Name</span></span>
<span data-ttu-id="9f65b-126">Namnet på artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="9f65b-126">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f65b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f65b-127">-ResourceGroupName</span></span>
<span data-ttu-id="9f65b-128">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9f65b-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f65b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f65b-129">-ResourceId</span></span>
<span data-ttu-id="9f65b-130">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9f65b-130">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f65b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f65b-131">CommonParameters</span></span>
<span data-ttu-id="9f65b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f65b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f65b-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f65b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f65b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f65b-134">INPUTS</span></span>

### <span data-ttu-id="9f65b-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="9f65b-135">None</span></span>

## <span data-ttu-id="9f65b-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f65b-136">OUTPUTS</span></span>

### <span data-ttu-id="9f65b-137">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9f65b-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="9f65b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f65b-138">NOTES</span></span>

## <span data-ttu-id="9f65b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f65b-139">RELATED LINKS</span></span>

[<span data-ttu-id="9f65b-140">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9f65b-140">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="9f65b-141">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9f65b-141">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="9f65b-142">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9f65b-142">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)