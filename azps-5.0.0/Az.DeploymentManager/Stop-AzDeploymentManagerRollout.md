---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320083"
---
# <span data-ttu-id="af7f6-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="af7f6-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="af7f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="af7f6-103">Avslutar installationen.</span><span class="sxs-lookup"><span data-stu-id="af7f6-103">Stops the rollout.</span></span>

## <span data-ttu-id="af7f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af7f6-104">SYNTAX</span></span>

### <span data-ttu-id="af7f6-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="af7f6-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af7f6-106">ID</span><span class="sxs-lookup"><span data-stu-id="af7f6-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af7f6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="af7f6-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af7f6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af7f6-108">DESCRIPTION</span></span>
<span data-ttu-id="af7f6-109">Cmdleten **Stop-AzDeploymentManagerRollout** stoppar en pågående installation och returnerar ett objekt som representerar det aktuella tillståndet för installationen.</span><span class="sxs-lookup"><span data-stu-id="af7f6-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="af7f6-110">Ange utgivningen med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="af7f6-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="af7f6-111">Du kan också ange ett installations objekt eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="af7f6-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="af7f6-112">Observera att när en introduktion har stoppats kan den inte återupptas eller startas om.</span><span class="sxs-lookup"><span data-stu-id="af7f6-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="af7f6-113">Du kan bara skapa en ny installation.</span><span class="sxs-lookup"><span data-stu-id="af7f6-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="af7f6-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af7f6-114">EXAMPLES</span></span>

### <span data-ttu-id="af7f6-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="af7f6-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="af7f6-116">Det här kommandot stoppar en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="af7f6-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="af7f6-117">Exempel 2: stoppa en lansering med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="af7f6-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="af7f6-118">Det här kommandot stoppar en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="af7f6-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="af7f6-119">Exempel 3: stoppa en installation med hjälp av installations objekt.</span><span class="sxs-lookup"><span data-stu-id="af7f6-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="af7f6-120">Det här kommandot stoppar en installation vars namn och ResourceGroup matchar $rolloutObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="af7f6-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="af7f6-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af7f6-121">PARAMETERS</span></span>

### <span data-ttu-id="af7f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7f6-122">-DefaultProfile</span></span>
<span data-ttu-id="af7f6-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af7f6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af7f6-124">-Force</span><span class="sxs-lookup"><span data-stu-id="af7f6-124">-Force</span></span>
<span data-ttu-id="af7f6-125">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="af7f6-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="af7f6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af7f6-126">-InputObject</span></span>
<span data-ttu-id="af7f6-127">Installations filen ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="af7f6-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="af7f6-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="af7f6-128">-Name</span></span>
<span data-ttu-id="af7f6-129">Namnet på installationen.</span><span class="sxs-lookup"><span data-stu-id="af7f6-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="af7f6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af7f6-130">-ResourceGroupName</span></span>
<span data-ttu-id="af7f6-131">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="af7f6-131">The resource group.</span></span>

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

### <span data-ttu-id="af7f6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af7f6-132">-ResourceId</span></span>
<span data-ttu-id="af7f6-133">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="af7f6-133">The resource identifier.</span></span>

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

### <span data-ttu-id="af7f6-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af7f6-134">-Confirm</span></span>
<span data-ttu-id="af7f6-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af7f6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af7f6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af7f6-136">-WhatIf</span></span>
<span data-ttu-id="af7f6-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af7f6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af7f6-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af7f6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af7f6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7f6-139">CommonParameters</span></span>
<span data-ttu-id="af7f6-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af7f6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7f6-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af7f6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7f6-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af7f6-142">INPUTS</span></span>

### <span data-ttu-id="af7f6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="af7f6-143">System.String</span></span>

### <span data-ttu-id="af7f6-144">Microsoft. Azure. commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="af7f6-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="af7f6-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af7f6-145">OUTPUTS</span></span>

### <span data-ttu-id="af7f6-146">Microsoft. Azure. commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="af7f6-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="af7f6-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af7f6-147">NOTES</span></span>

## <span data-ttu-id="af7f6-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af7f6-148">RELATED LINKS</span></span>
