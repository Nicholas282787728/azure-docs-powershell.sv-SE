---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 7473f125511995efb1f6273d3b8adb675a58d06d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571428"
---
# <span data-ttu-id="3a6be-101">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="3a6be-101">Remove-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="3a6be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3a6be-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6be-103">Tar bort en artefakt källa.</span><span class="sxs-lookup"><span data-stu-id="3a6be-103">Deletes an artifact source.</span></span>

## <span data-ttu-id="3a6be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3a6be-104">SYNTAX</span></span>

### <span data-ttu-id="3a6be-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="3a6be-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a6be-106">ID</span><span class="sxs-lookup"><span data-stu-id="3a6be-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a6be-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3a6be-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a6be-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3a6be-108">DESCRIPTION</span></span>
<span data-ttu-id="3a6be-109">Cmdleten **Remove-AzureRmDeploymentManagerArtifactSource** tar bort en artefakt källa ange artefakt källan med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3a6be-109">The **Remove-AzureRmDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="3a6be-110">Du kan också ange ArtifactSource-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="3a6be-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="3a6be-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3a6be-111">EXAMPLES</span></span>

### <span data-ttu-id="3a6be-112">Exempel 1: ta bort en artefakt källa</span><span class="sxs-lookup"><span data-stu-id="3a6be-112">Example 1: Delete an artifact source</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="3a6be-113">Det här kommandot tar bort en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3a6be-113">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="3a6be-114">Exempel 2: ta bort en artefakt källa med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="3a6be-114">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="3a6be-115">Det här kommandot tar bort en artefakt källa som heter ContosoArtifactSource i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3a6be-115">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="3a6be-116">Exempel 3: ta bort en artefakt källa med hjälp av ett objekt</span><span class="sxs-lookup"><span data-stu-id="3a6be-116">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="3a6be-117">Det här kommandot tar bort en artefakt källa vars namn och ResourceGroup matchar $artifactSourceObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="3a6be-117">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="3a6be-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3a6be-118">PARAMETERS</span></span>

### <span data-ttu-id="3a6be-119">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="3a6be-119">-ArtifactSource</span></span>
<span data-ttu-id="3a6be-120">Artefakt arkivet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3a6be-120">The artifact store to be removed.</span></span>

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

### <span data-ttu-id="3a6be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6be-121">-DefaultProfile</span></span>
<span data-ttu-id="3a6be-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6be-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a6be-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3a6be-123">-Force</span></span>
<span data-ttu-id="3a6be-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3a6be-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3a6be-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="3a6be-125">-Name</span></span>
<span data-ttu-id="3a6be-126">Namnet på artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="3a6be-126">The name of the artifact source.</span></span>

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

### <span data-ttu-id="3a6be-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a6be-127">-PassThru</span></span>
<span data-ttu-id="3a6be-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3a6be-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3a6be-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a6be-129">-ResourceGroupName</span></span>
<span data-ttu-id="3a6be-130">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3a6be-130">The resource group.</span></span>

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

### <span data-ttu-id="3a6be-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a6be-131">-ResourceId</span></span>
<span data-ttu-id="3a6be-132">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3a6be-132">The resource identifier.</span></span>

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

### <span data-ttu-id="3a6be-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3a6be-133">-Confirm</span></span>
<span data-ttu-id="3a6be-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3a6be-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a6be-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a6be-135">-WhatIf</span></span>
<span data-ttu-id="3a6be-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3a6be-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a6be-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3a6be-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a6be-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6be-138">CommonParameters</span></span>
<span data-ttu-id="3a6be-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a6be-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6be-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a6be-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6be-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3a6be-141">INPUTS</span></span>

### <span data-ttu-id="3a6be-142">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="3a6be-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="3a6be-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3a6be-143">OUTPUTS</span></span>

### <span data-ttu-id="3a6be-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a6be-144">System.Boolean</span></span>

## <span data-ttu-id="3a6be-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3a6be-145">NOTES</span></span>

## <span data-ttu-id="3a6be-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3a6be-146">RELATED LINKS</span></span>

[<span data-ttu-id="3a6be-147">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="3a6be-147">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="3a6be-148">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="3a6be-148">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="3a6be-149">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="3a6be-149">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)