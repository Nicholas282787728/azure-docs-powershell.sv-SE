---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/restart-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: ee1ef6e5b8bcee4af1d3aef67767269042c552df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572200"
---
# <span data-ttu-id="7ebb9-101">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7ebb9-101">Restart-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="7ebb9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ebb9-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebb9-103">Starta om en misslyckad installation.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-103">Restart a failed rollout.</span></span>

## <span data-ttu-id="7ebb9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ebb9-104">SYNTAX</span></span>

### <span data-ttu-id="7ebb9-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="7ebb9-105">Interactive (Default)</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ebb9-106">ID</span><span class="sxs-lookup"><span data-stu-id="7ebb9-106">ResourceId</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ebb9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7ebb9-107">InputObject</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ebb9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ebb9-108">DESCRIPTION</span></span>
<span data-ttu-id="7ebb9-109">Cmdleten **restart-AzureRmDeploymentManagerRollout** startar om en misslyckad installation och returnerar ett objekt som representerar en installation med all detaljerad information om hur installationen fortskrider.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-109">The **Restart-AzureRmDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="7ebb9-110">Ange utgivningen med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="7ebb9-111">Du kan också ange ett installations objekt eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="7ebb9-112">Med valfri parameter SkipSucceeded kan du hoppa över alla slutförda steg i förra installationen av lanseringen.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="7ebb9-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ebb9-113">EXAMPLES</span></span>

### <span data-ttu-id="7ebb9-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7ebb9-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="7ebb9-115">Det här kommandot startar om en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="7ebb9-116">Flaggan SkipSucceeded anger att alla steg som redan har körts ska hoppas över och att installationen fortsätter från den där den senaste misslyckades.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="7ebb9-117">Exempel 2: starta om en installation med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="7ebb9-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="7ebb9-118">Det här kommandot startar om en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7ebb9-119">Exempel 3: starta om en installation med hjälp av installations objekt.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="7ebb9-120">Det här kommandot startar om en installation vars namn och ResourceGroup matchar $rolloutObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="7ebb9-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ebb9-121">PARAMETERS</span></span>

### <span data-ttu-id="7ebb9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ebb9-122">-DefaultProfile</span></span>
<span data-ttu-id="7ebb9-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ebb9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ebb9-124">-Name</span></span>
<span data-ttu-id="7ebb9-125">Namnet på installationen.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="7ebb9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ebb9-126">-ResourceGroupName</span></span>
<span data-ttu-id="7ebb9-127">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-127">The resource group.</span></span>

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

### <span data-ttu-id="7ebb9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ebb9-128">-ResourceId</span></span>
<span data-ttu-id="7ebb9-129">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-129">The resource identifier.</span></span>

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

### <span data-ttu-id="7ebb9-130">-Lansering</span><span class="sxs-lookup"><span data-stu-id="7ebb9-130">-Rollout</span></span>
<span data-ttu-id="7ebb9-131">Resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-131">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebb9-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="7ebb9-132">-SkipSucceeded</span></span>
<span data-ttu-id="7ebb9-133">Hoppa över steg som har lyckats med installationen.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="7ebb9-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ebb9-134">-Confirm</span></span>
<span data-ttu-id="7ebb9-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ebb9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ebb9-136">-WhatIf</span></span>
<span data-ttu-id="7ebb9-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ebb9-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ebb9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebb9-139">CommonParameters</span></span>
<span data-ttu-id="7ebb9-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ebb9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebb9-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ebb9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebb9-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ebb9-142">INPUTS</span></span>

### <span data-ttu-id="7ebb9-143">Microsoft. Azure. commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="7ebb9-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7ebb9-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ebb9-144">OUTPUTS</span></span>

### <span data-ttu-id="7ebb9-145">Microsoft. Azure. commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="7ebb9-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7ebb9-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ebb9-146">NOTES</span></span>

## <span data-ttu-id="7ebb9-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ebb9-147">RELATED LINKS</span></span>

[<span data-ttu-id="7ebb9-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7ebb9-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="7ebb9-149">Stopp-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7ebb9-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="7ebb9-150">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7ebb9-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)