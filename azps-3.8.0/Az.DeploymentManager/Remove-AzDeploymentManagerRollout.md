---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092126"
---
# <span data-ttu-id="10c61-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="10c61-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="10c61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10c61-102">SYNOPSIS</span></span>
<span data-ttu-id="10c61-103">Tar bort installationen.</span><span class="sxs-lookup"><span data-stu-id="10c61-103">Deletes the rollout.</span></span>

## <span data-ttu-id="10c61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10c61-104">SYNTAX</span></span>

### <span data-ttu-id="10c61-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="10c61-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c61-106">ID</span><span class="sxs-lookup"><span data-stu-id="10c61-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c61-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="10c61-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10c61-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10c61-108">DESCRIPTION</span></span>
<span data-ttu-id="10c61-109">Cmdleten **Remove-AzDeploymentManagerRollout** tar bort en installation i ett Terminal-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="10c61-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="10c61-110">Ange utgivningen med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="10c61-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="10c61-111">Du kan också ange ett installations objekt eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="10c61-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="10c61-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10c61-112">EXAMPLES</span></span>

### <span data-ttu-id="10c61-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="10c61-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="10c61-114">Det här kommandot tar bort en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="10c61-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="10c61-115">Exempel 2: ta bort en lansering med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="10c61-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="10c61-116">Det här kommandot tar bort en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="10c61-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="10c61-117">Exempel 3: ta bort en lansering med hjälp av installations objekt.</span><span class="sxs-lookup"><span data-stu-id="10c61-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="10c61-118">Det här kommandot tar bort en installation vars namn och ResourceGroup matchar $rolloutObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="10c61-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="10c61-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10c61-119">PARAMETERS</span></span>

### <span data-ttu-id="10c61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c61-120">-DefaultProfile</span></span>
<span data-ttu-id="10c61-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10c61-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10c61-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10c61-122">-InputObject</span></span>
<span data-ttu-id="10c61-123">Resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="10c61-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="10c61-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="10c61-124">-Name</span></span>
<span data-ttu-id="10c61-125">Namnet på installationen.</span><span class="sxs-lookup"><span data-stu-id="10c61-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="10c61-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10c61-126">-PassThru</span></span>
<span data-ttu-id="10c61-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="10c61-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="10c61-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c61-128">-ResourceGroupName</span></span>
<span data-ttu-id="10c61-129">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="10c61-129">The resource group.</span></span>

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

### <span data-ttu-id="10c61-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10c61-130">-ResourceId</span></span>
<span data-ttu-id="10c61-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="10c61-131">The resource identifier.</span></span>

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

### <span data-ttu-id="10c61-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10c61-132">-Confirm</span></span>
<span data-ttu-id="10c61-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10c61-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10c61-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10c61-134">-WhatIf</span></span>
<span data-ttu-id="10c61-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10c61-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10c61-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10c61-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10c61-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c61-137">CommonParameters</span></span>
<span data-ttu-id="10c61-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c61-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c61-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10c61-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c61-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10c61-140">INPUTS</span></span>

### <span data-ttu-id="10c61-141">System. String</span><span class="sxs-lookup"><span data-stu-id="10c61-141">System.String</span></span>

### <span data-ttu-id="10c61-142">Microsoft. Azure. commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="10c61-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="10c61-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10c61-143">OUTPUTS</span></span>

### <span data-ttu-id="10c61-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10c61-144">System.Boolean</span></span>

## <span data-ttu-id="10c61-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10c61-145">NOTES</span></span>

## <span data-ttu-id="10c61-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10c61-146">RELATED LINKS</span></span>