---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426448"
---
# <span data-ttu-id="2755a-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2755a-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="2755a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2755a-102">SYNOPSIS</span></span>
<span data-ttu-id="2755a-103">Tar bort angiven artefakt källa.</span><span class="sxs-lookup"><span data-stu-id="2755a-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="2755a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2755a-104">SYNTAX</span></span>

### <span data-ttu-id="2755a-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="2755a-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2755a-106">ID</span><span class="sxs-lookup"><span data-stu-id="2755a-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2755a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2755a-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2755a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2755a-108">DESCRIPTION</span></span>
<span data-ttu-id="2755a-109">Cmdleten **Remove-AzDeploymentManagerArtifactSource** tar bort en artefakt källa ange artefakt källan med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2755a-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="2755a-110">Du kan också ange ArtifactSource-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2755a-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="2755a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2755a-111">EXAMPLES</span></span>

### <span data-ttu-id="2755a-112">Exempel 1: ta bort en artefakt källa</span><span class="sxs-lookup"><span data-stu-id="2755a-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="2755a-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2755a-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="2755a-114">Det här kommandot tar bort en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2755a-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="2755a-115">Exempel 2: ta bort en artefakt källa med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="2755a-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="2755a-116">Det här kommandot tar bort en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2755a-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="2755a-117">Exempel 3: ta bort en artefakt källa med hjälp av ett objekt</span><span class="sxs-lookup"><span data-stu-id="2755a-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="2755a-118">Det här kommandot tar bort en artefakt källa vars namn och ResourceGroup matchar $artifactSourceObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="2755a-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="2755a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2755a-119">PARAMETERS</span></span>

### <span data-ttu-id="2755a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2755a-120">-DefaultProfile</span></span>
<span data-ttu-id="2755a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2755a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2755a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2755a-122">-InputObject</span></span>
<span data-ttu-id="2755a-123">Den artefakt källa som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2755a-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="2755a-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="2755a-124">-Name</span></span>
<span data-ttu-id="2755a-125">Namnet på artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="2755a-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="2755a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2755a-126">-PassThru</span></span>
<span data-ttu-id="2755a-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2755a-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2755a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2755a-128">-ResourceGroupName</span></span>
<span data-ttu-id="2755a-129">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2755a-129">The resource group.</span></span>

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

### <span data-ttu-id="2755a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2755a-130">-ResourceId</span></span>
<span data-ttu-id="2755a-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2755a-131">The resource identifier.</span></span>

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

### <span data-ttu-id="2755a-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2755a-132">-Confirm</span></span>
<span data-ttu-id="2755a-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2755a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2755a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2755a-134">-WhatIf</span></span>
<span data-ttu-id="2755a-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2755a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2755a-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2755a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2755a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2755a-137">CommonParameters</span></span>
<span data-ttu-id="2755a-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2755a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2755a-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2755a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2755a-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2755a-140">INPUTS</span></span>

### <span data-ttu-id="2755a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2755a-141">System.String</span></span>

### <span data-ttu-id="2755a-142">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2755a-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="2755a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2755a-143">OUTPUTS</span></span>

### <span data-ttu-id="2755a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2755a-144">System.Boolean</span></span>

## <span data-ttu-id="2755a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2755a-145">NOTES</span></span>

## <span data-ttu-id="2755a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2755a-146">RELATED LINKS</span></span>
