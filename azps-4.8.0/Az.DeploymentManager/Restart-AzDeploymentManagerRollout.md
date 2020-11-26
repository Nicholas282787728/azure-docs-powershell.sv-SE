---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260534"
---
# <span data-ttu-id="7bd0b-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7bd0b-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="7bd0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bd0b-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd0b-103">Startar om en misslyckad installation.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="7bd0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bd0b-104">SYNTAX</span></span>

### <span data-ttu-id="7bd0b-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="7bd0b-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd0b-106">ID</span><span class="sxs-lookup"><span data-stu-id="7bd0b-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd0b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7bd0b-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bd0b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bd0b-108">DESCRIPTION</span></span>
<span data-ttu-id="7bd0b-109">Cmdleten **restart-AzDeploymentManagerRollout** startar om en misslyckad installation och returnerar ett objekt som representerar en installation med all detaljerad information om hur installationen fortskrider.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="7bd0b-110">Ange utgivningen med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="7bd0b-111">Du kan också ange ett installations objekt eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="7bd0b-112">Med valfri parameter SkipSucceeded kan du hoppa över alla slutförda steg i förra installationen av lanseringen.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="7bd0b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bd0b-113">EXAMPLES</span></span>

### <span data-ttu-id="7bd0b-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7bd0b-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="7bd0b-115">Det här kommandot startar om en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="7bd0b-116">Flaggan SkipSucceeded anger att alla steg som redan har körts ska hoppas över och att installationen fortsätter från den där den senaste misslyckades.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="7bd0b-117">Exempel 2: starta om en installation med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="7bd0b-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="7bd0b-118">Det här kommandot startar om en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7bd0b-119">Exempel 3: starta om en installation med hjälp av installations objekt.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="7bd0b-120">Det här kommandot startar om en installation vars namn och ResourceGroup matchar $rolloutObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="7bd0b-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bd0b-121">PARAMETERS</span></span>

### <span data-ttu-id="7bd0b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd0b-122">-DefaultProfile</span></span>
<span data-ttu-id="7bd0b-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd0b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bd0b-124">-InputObject</span></span>
<span data-ttu-id="7bd0b-125">Resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="7bd0b-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="7bd0b-126">-Name</span></span>
<span data-ttu-id="7bd0b-127">Namnet på installationen.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="7bd0b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd0b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7bd0b-129">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-129">The resource group.</span></span>

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

### <span data-ttu-id="7bd0b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bd0b-130">-ResourceId</span></span>
<span data-ttu-id="7bd0b-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-131">The resource identifier.</span></span>

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

### <span data-ttu-id="7bd0b-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="7bd0b-132">-SkipSucceeded</span></span>
<span data-ttu-id="7bd0b-133">Hoppa över steg som har lyckats med installationen.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="7bd0b-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7bd0b-134">-Confirm</span></span>
<span data-ttu-id="7bd0b-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd0b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd0b-136">-WhatIf</span></span>
<span data-ttu-id="7bd0b-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bd0b-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd0b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd0b-139">CommonParameters</span></span>
<span data-ttu-id="7bd0b-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd0b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd0b-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bd0b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd0b-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bd0b-142">INPUTS</span></span>

### <span data-ttu-id="7bd0b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7bd0b-143">System.String</span></span>

### <span data-ttu-id="7bd0b-144">Microsoft. Azure. commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="7bd0b-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7bd0b-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bd0b-145">OUTPUTS</span></span>

### <span data-ttu-id="7bd0b-146">Microsoft. Azure. commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="7bd0b-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7bd0b-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bd0b-147">NOTES</span></span>

## <span data-ttu-id="7bd0b-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bd0b-148">RELATED LINKS</span></span>