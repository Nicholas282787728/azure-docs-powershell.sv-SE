---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 54cccbedc45977505b10526d4806b64c8118380e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754241"
---
# <span data-ttu-id="d1f19-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d1f19-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="d1f19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1f19-102">SYNOPSIS</span></span>

<span data-ttu-id="d1f19-103">Hämtar artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="d1f19-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="d1f19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1f19-104">SYNTAX</span></span>

### <span data-ttu-id="d1f19-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="d1f19-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1f19-106">ID</span><span class="sxs-lookup"><span data-stu-id="d1f19-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1f19-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d1f19-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1f19-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1f19-108">DESCRIPTION</span></span>
<span data-ttu-id="d1f19-109">Cmdleten **Get-AzDeploymentManagerArtifactSource** hämtar en artefakt källa och returnerar ett objekt som representerar den artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="d1f19-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="d1f19-110">Ange artefakt källan med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d1f19-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="d1f19-111">Du kan också ange ArtifactSource-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d1f19-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="d1f19-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1f19-112">EXAMPLES</span></span>

### <span data-ttu-id="d1f19-113">Exempel 1: Hämta en artefakt källa</span><span class="sxs-lookup"><span data-stu-id="d1f19-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="d1f19-114">Det här kommandot får en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d1f19-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d1f19-115">Exempel 2: Hämta en artefakt källa med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="d1f19-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="d1f19-116">Det här kommandot får en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d1f19-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d1f19-117">Exempel 3: Hämta en artefakt källa med ett objekt som returneras av New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d1f19-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="d1f19-118">Det här kommandot får en artefakt källa vars namn och ResourceGroup matchar $artifactSourceObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="d1f19-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="d1f19-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1f19-119">PARAMETERS</span></span>

### <span data-ttu-id="d1f19-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f19-120">-DefaultProfile</span></span>
<span data-ttu-id="d1f19-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1f19-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1f19-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1f19-122">-InputObject</span></span>
<span data-ttu-id="d1f19-123">Objekt i artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="d1f19-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="d1f19-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1f19-124">-Name</span></span>
<span data-ttu-id="d1f19-125">Namnet på artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="d1f19-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f19-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1f19-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1f19-127">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d1f19-127">The resource group.</span></span>

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

### <span data-ttu-id="d1f19-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f19-128">-ResourceId</span></span>
<span data-ttu-id="d1f19-129">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d1f19-129">The resource identifier.</span></span>

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

### <span data-ttu-id="d1f19-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f19-130">CommonParameters</span></span>
<span data-ttu-id="d1f19-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1f19-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f19-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1f19-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f19-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1f19-133">INPUTS</span></span>

### <span data-ttu-id="d1f19-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d1f19-134">System.String</span></span>

### <span data-ttu-id="d1f19-135">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d1f19-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="d1f19-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1f19-136">OUTPUTS</span></span>

### <span data-ttu-id="d1f19-137">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d1f19-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="d1f19-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1f19-138">NOTES</span></span>

## <span data-ttu-id="d1f19-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1f19-139">RELATED LINKS</span></span>