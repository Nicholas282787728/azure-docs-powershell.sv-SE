---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092103"
---
# <span data-ttu-id="2979e-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="2979e-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="2979e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2979e-102">SYNOPSIS</span></span>
<span data-ttu-id="2979e-103">Tar bort steget.</span><span class="sxs-lookup"><span data-stu-id="2979e-103">Deletes the step.</span></span>

## <span data-ttu-id="2979e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2979e-104">SYNTAX</span></span>

### <span data-ttu-id="2979e-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="2979e-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2979e-106">ID</span><span class="sxs-lookup"><span data-stu-id="2979e-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2979e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2979e-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2979e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2979e-108">DESCRIPTION</span></span>
<span data-ttu-id="2979e-109">Cmdleten **Remove-AzDeploymentManagerStep** tar bort ett steg.</span><span class="sxs-lookup"><span data-stu-id="2979e-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="2979e-110">Ange steget med dess namn och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2979e-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="2979e-111">Du kan också ange Step-ID eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2979e-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="2979e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2979e-112">EXAMPLES</span></span>

### <span data-ttu-id="2979e-113">Exempel 1: ta bort ett steg</span><span class="sxs-lookup"><span data-stu-id="2979e-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="2979e-114">Det här kommandot tar bort ett steg som heter ContosoService1WaitStep i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2979e-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="2979e-115">Exempel 2: ta bort ett steg med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="2979e-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="2979e-116">Det här kommandot tar bort ett steg som heter ContosoService1WaitStep i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2979e-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="2979e-117">Exempel 3: ta bort ett steg med ett objekt som returneras av New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="2979e-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="2979e-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2979e-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="2979e-119">Det här kommandot tar bort ett steg vars namn och ResourceGroup matchar $stepObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="2979e-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="2979e-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2979e-120">PARAMETERS</span></span>

### <span data-ttu-id="2979e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2979e-121">-DefaultProfile</span></span>
<span data-ttu-id="2979e-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2979e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2979e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2979e-123">-InputObject</span></span>
<span data-ttu-id="2979e-124">Steget som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2979e-124">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2979e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="2979e-125">-Name</span></span>
<span data-ttu-id="2979e-126">Namnet på steget.</span><span class="sxs-lookup"><span data-stu-id="2979e-126">The name of the step.</span></span>

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

### <span data-ttu-id="2979e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2979e-127">-PassThru</span></span>
<span data-ttu-id="2979e-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2979e-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2979e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2979e-129">-ResourceGroupName</span></span>
<span data-ttu-id="2979e-130">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2979e-130">The resource group.</span></span>

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

### <span data-ttu-id="2979e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2979e-131">-ResourceId</span></span>
<span data-ttu-id="2979e-132">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2979e-132">The resource identifier.</span></span>

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

### <span data-ttu-id="2979e-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2979e-133">-Confirm</span></span>
<span data-ttu-id="2979e-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2979e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2979e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2979e-135">-WhatIf</span></span>
<span data-ttu-id="2979e-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2979e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2979e-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2979e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2979e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2979e-138">CommonParameters</span></span>
<span data-ttu-id="2979e-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2979e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2979e-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2979e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2979e-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2979e-141">INPUTS</span></span>

### <span data-ttu-id="2979e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2979e-142">System.String</span></span>

### <span data-ttu-id="2979e-143">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="2979e-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="2979e-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2979e-144">OUTPUTS</span></span>

### <span data-ttu-id="2979e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2979e-145">System.Boolean</span></span>

## <span data-ttu-id="2979e-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2979e-146">NOTES</span></span>

## <span data-ttu-id="2979e-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2979e-147">RELATED LINKS</span></span>