---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408432"
---
# <span data-ttu-id="a1dca-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a1dca-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="a1dca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1dca-102">SYNOPSIS</span></span>

<span data-ttu-id="a1dca-103">Hämtar artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="a1dca-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="a1dca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1dca-104">SYNTAX</span></span>

### <span data-ttu-id="a1dca-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="a1dca-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1dca-106">ID</span><span class="sxs-lookup"><span data-stu-id="a1dca-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1dca-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a1dca-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1dca-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1dca-108">DESCRIPTION</span></span>
<span data-ttu-id="a1dca-109">Cmdleten **Get-AzDeploymentManagerArtifactSource** hämtar en artefakt källa och returnerar ett objekt som representerar den artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="a1dca-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="a1dca-110">Ange artefakt källan med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a1dca-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="a1dca-111">Du kan också ange ArtifactSource-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a1dca-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="a1dca-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1dca-112">EXAMPLES</span></span>

### <span data-ttu-id="a1dca-113">Exempel 1: Hämta en artefakt källa</span><span class="sxs-lookup"><span data-stu-id="a1dca-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="a1dca-114">Det här kommandot får en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a1dca-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="a1dca-115">Exempel 2: Hämta en artefakt källa med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="a1dca-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="a1dca-116">Det här kommandot får en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a1dca-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="a1dca-117">Exempel 3: Hämta en artefakt källa med ett objekt som returneras av New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a1dca-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="a1dca-118">Det här kommandot får en artefakt källa vars namn och ResourceGroup matchar $artifactSourceObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a1dca-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="a1dca-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1dca-119">PARAMETERS</span></span>

### <span data-ttu-id="a1dca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1dca-120">-DefaultProfile</span></span>
<span data-ttu-id="a1dca-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1dca-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1dca-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1dca-122">-InputObject</span></span>
<span data-ttu-id="a1dca-123">Objekt i artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="a1dca-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="a1dca-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1dca-124">-Name</span></span>
<span data-ttu-id="a1dca-125">Namnet på artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="a1dca-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="a1dca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1dca-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1dca-127">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a1dca-127">The resource group.</span></span>

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

### <span data-ttu-id="a1dca-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1dca-128">-ResourceId</span></span>
<span data-ttu-id="a1dca-129">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a1dca-129">The resource identifier.</span></span>

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

### <span data-ttu-id="a1dca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1dca-130">CommonParameters</span></span>
<span data-ttu-id="a1dca-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1dca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1dca-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1dca-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1dca-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1dca-133">INPUTS</span></span>

### <span data-ttu-id="a1dca-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a1dca-134">System.String</span></span>

### <span data-ttu-id="a1dca-135">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a1dca-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="a1dca-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1dca-136">OUTPUTS</span></span>

### <span data-ttu-id="a1dca-137">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a1dca-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="a1dca-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1dca-138">NOTES</span></span>

## <span data-ttu-id="a1dca-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1dca-139">RELATED LINKS</span></span>
