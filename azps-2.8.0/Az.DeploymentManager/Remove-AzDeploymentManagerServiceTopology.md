---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 695a10eb71cc2c4bd1a6bc7eef6cba265d524fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744371"
---
# <span data-ttu-id="93f51-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="93f51-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="93f51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93f51-102">SYNOPSIS</span></span>
<span data-ttu-id="93f51-103">Tar bort tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="93f51-103">Deletes the service topology.</span></span> <span data-ttu-id="93f51-104">Alla tjänster som skapas under en tjänst topologi måste tas bort innan tjänste sto pol Ogin tas bort.</span><span class="sxs-lookup"><span data-stu-id="93f51-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="93f51-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93f51-105">SYNTAX</span></span>

### <span data-ttu-id="93f51-106">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="93f51-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93f51-107">ID</span><span class="sxs-lookup"><span data-stu-id="93f51-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93f51-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="93f51-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93f51-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93f51-109">DESCRIPTION</span></span>
<span data-ttu-id="93f51-110">Cmdleten **Remove-AzDeploymentManagerServiceTopology** tar bort en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="93f51-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="93f51-111">Ange tjänst sto pol Ogin efter dess namn och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="93f51-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="93f51-112">Du kan också ange ServiceTopology-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="93f51-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="93f51-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93f51-113">EXAMPLES</span></span>

### <span data-ttu-id="93f51-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="93f51-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="93f51-115">Det här kommandot tar bort en tjänst sto pol ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="93f51-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="93f51-116">Exempel 2: ta bort en tjänst sto pol Ogin med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="93f51-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="93f51-117">Det här kommandot tar bort en tjänst sto pol ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="93f51-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="93f51-118">Exempel 3: ta bort en tjänst topologi med hjälp av objektet tjänst Topology.</span><span class="sxs-lookup"><span data-stu-id="93f51-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="93f51-119">Det här kommandot tar bort en tjänst sto pol Ogin vars namn och ResourceGroup matchar $serviceTopologyObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="93f51-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="93f51-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93f51-120">PARAMETERS</span></span>

### <span data-ttu-id="93f51-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f51-121">-DefaultProfile</span></span>
<span data-ttu-id="93f51-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93f51-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93f51-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93f51-123">-InputObject</span></span>
<span data-ttu-id="93f51-124">Resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="93f51-124">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93f51-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="93f51-125">-Name</span></span>
<span data-ttu-id="93f51-126">Namnet på tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="93f51-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="93f51-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93f51-127">-PassThru</span></span>
<span data-ttu-id="93f51-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="93f51-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="93f51-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f51-129">-ResourceGroupName</span></span>
<span data-ttu-id="93f51-130">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="93f51-130">The resource group.</span></span>

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

### <span data-ttu-id="93f51-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93f51-131">-ResourceId</span></span>
<span data-ttu-id="93f51-132">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="93f51-132">The resource identifier.</span></span>

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

### <span data-ttu-id="93f51-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="93f51-133">-Confirm</span></span>
<span data-ttu-id="93f51-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93f51-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93f51-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93f51-135">-WhatIf</span></span>
<span data-ttu-id="93f51-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93f51-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93f51-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="93f51-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93f51-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f51-138">CommonParameters</span></span>
<span data-ttu-id="93f51-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f51-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f51-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f51-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f51-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93f51-141">INPUTS</span></span>

### <span data-ttu-id="93f51-142">System. String</span><span class="sxs-lookup"><span data-stu-id="93f51-142">System.String</span></span>

### <span data-ttu-id="93f51-143">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="93f51-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="93f51-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93f51-144">OUTPUTS</span></span>

### <span data-ttu-id="93f51-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93f51-145">System.Boolean</span></span>

## <span data-ttu-id="93f51-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93f51-146">NOTES</span></span>

## <span data-ttu-id="93f51-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93f51-147">RELATED LINKS</span></span>
