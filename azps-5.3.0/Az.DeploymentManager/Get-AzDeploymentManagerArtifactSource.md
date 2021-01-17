---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426488"
---
# <span data-ttu-id="55593-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="55593-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="55593-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55593-102">SYNOPSIS</span></span>

<span data-ttu-id="55593-103">Hämtar artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="55593-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="55593-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55593-104">SYNTAX</span></span>

### <span data-ttu-id="55593-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="55593-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55593-106">ID</span><span class="sxs-lookup"><span data-stu-id="55593-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55593-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="55593-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55593-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55593-108">DESCRIPTION</span></span>
<span data-ttu-id="55593-109">Cmdleten **Get-AzDeploymentManagerArtifactSource** hämtar en artefakt källa och returnerar ett objekt som representerar den artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="55593-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="55593-110">Ange artefakt källan med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="55593-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="55593-111">Du kan också ange ArtifactSource-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="55593-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="55593-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55593-112">EXAMPLES</span></span>

### <span data-ttu-id="55593-113">Exempel 1: Hämta en artefakt källa</span><span class="sxs-lookup"><span data-stu-id="55593-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="55593-114">Det här kommandot får en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="55593-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="55593-115">Exempel 2: Hämta en artefakt källa med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="55593-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="55593-116">Det här kommandot får en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="55593-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="55593-117">Exempel 3: Hämta en artefakt källa med ett objekt som returneras av New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="55593-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="55593-118">Det här kommandot får en artefakt källa vars namn och ResourceGroup matchar $artifactSourceObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="55593-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="55593-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55593-119">PARAMETERS</span></span>

### <span data-ttu-id="55593-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55593-120">-DefaultProfile</span></span>
<span data-ttu-id="55593-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55593-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55593-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55593-122">-InputObject</span></span>
<span data-ttu-id="55593-123">Objekt i artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="55593-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="55593-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="55593-124">-Name</span></span>
<span data-ttu-id="55593-125">Namnet på artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="55593-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55593-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55593-126">-ResourceGroupName</span></span>
<span data-ttu-id="55593-127">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="55593-127">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55593-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55593-128">-ResourceId</span></span>
<span data-ttu-id="55593-129">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="55593-129">The resource identifier.</span></span>

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

### <span data-ttu-id="55593-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55593-130">CommonParameters</span></span>
<span data-ttu-id="55593-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55593-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55593-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55593-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55593-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55593-133">INPUTS</span></span>

### <span data-ttu-id="55593-134">System. String</span><span class="sxs-lookup"><span data-stu-id="55593-134">System.String</span></span>

### <span data-ttu-id="55593-135">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="55593-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="55593-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55593-136">OUTPUTS</span></span>

### <span data-ttu-id="55593-137">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="55593-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="55593-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55593-138">NOTES</span></span>

## <span data-ttu-id="55593-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55593-139">RELATED LINKS</span></span>
