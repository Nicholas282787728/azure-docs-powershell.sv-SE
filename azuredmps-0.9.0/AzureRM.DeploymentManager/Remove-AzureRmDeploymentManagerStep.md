---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 3abceb6c3c270378c911036967698f459cbe063a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571512"
---
# <span data-ttu-id="74246-101">Remove-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="74246-101">Remove-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="74246-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74246-102">SYNOPSIS</span></span>
<span data-ttu-id="74246-103">Tar bort ett steg.</span><span class="sxs-lookup"><span data-stu-id="74246-103">Deletes a step.</span></span>

## <span data-ttu-id="74246-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74246-104">SYNTAX</span></span>

### <span data-ttu-id="74246-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="74246-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74246-106">ID</span><span class="sxs-lookup"><span data-stu-id="74246-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74246-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="74246-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74246-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74246-108">DESCRIPTION</span></span>
<span data-ttu-id="74246-109">Cmdleten **Remove-AzureRmDeploymentManagerStep** tar bort ett steg.</span><span class="sxs-lookup"><span data-stu-id="74246-109">The **Remove-AzureRmDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="74246-110">Ange steget med dess namn och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="74246-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="74246-111">Du kan också ange Step-ID eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="74246-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="74246-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74246-112">EXAMPLES</span></span>
### <span data-ttu-id="74246-113">Exempel 1: ta bort ett steg</span><span class="sxs-lookup"><span data-stu-id="74246-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="74246-114">Det här kommandot tar bort ett steg som heter ContosoService1WaitStep i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="74246-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="74246-115">Exempel 2: ta bort ett steg med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="74246-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="74246-116">Det här kommandot tar bort ett steg som heter ContosoService1WaitStep i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="74246-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="74246-117">Exempel 3: ta bort ett steg med ett objekt som returneras av New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="74246-117">Example 3: Remove a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="74246-118">Det här kommandot tar bort ett steg vars namn och ResourceGroup matchar $stepObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="74246-118">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="74246-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74246-119">PARAMETERS</span></span>

### <span data-ttu-id="74246-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74246-120">-DefaultProfile</span></span>
<span data-ttu-id="74246-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74246-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74246-122">-Force</span><span class="sxs-lookup"><span data-stu-id="74246-122">-Force</span></span>
<span data-ttu-id="74246-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="74246-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="74246-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="74246-124">-Name</span></span>
<span data-ttu-id="74246-125">Namnet på steget.</span><span class="sxs-lookup"><span data-stu-id="74246-125">The name of the step.</span></span>

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

### <span data-ttu-id="74246-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74246-126">-PassThru</span></span>
<span data-ttu-id="74246-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="74246-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="74246-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74246-128">-ResourceGroupName</span></span>
<span data-ttu-id="74246-129">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="74246-129">The resource group.</span></span>

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

### <span data-ttu-id="74246-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74246-130">-ResourceId</span></span>
<span data-ttu-id="74246-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="74246-131">The resource identifier.</span></span>

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

### <span data-ttu-id="74246-132">-Steg</span><span class="sxs-lookup"><span data-stu-id="74246-132">-Step</span></span>
<span data-ttu-id="74246-133">Steget som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="74246-133">The step to be removed.</span></span>

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

### <span data-ttu-id="74246-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74246-134">-Confirm</span></span>
<span data-ttu-id="74246-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74246-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74246-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74246-136">-WhatIf</span></span>
<span data-ttu-id="74246-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74246-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74246-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74246-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74246-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74246-139">CommonParameters</span></span>
<span data-ttu-id="74246-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74246-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="74246-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74246-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74246-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74246-142">INPUTS</span></span>

### <span data-ttu-id="74246-143">System. String</span><span class="sxs-lookup"><span data-stu-id="74246-143">System.String</span></span>

### <span data-ttu-id="74246-144">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="74246-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="74246-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74246-145">OUTPUTS</span></span>

### <span data-ttu-id="74246-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74246-146">System.Boolean</span></span>

## <span data-ttu-id="74246-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74246-147">NOTES</span></span>

## <span data-ttu-id="74246-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74246-148">RELATED LINKS</span></span>
