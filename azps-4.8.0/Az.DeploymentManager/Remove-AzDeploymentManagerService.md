---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 4828471d684e82d67a10bed7340cc560e843210a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101026"
---
# <span data-ttu-id="aa3af-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="aa3af-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="aa3af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa3af-102">SYNOPSIS</span></span>
<span data-ttu-id="aa3af-103">Tar bort tjänsten..</span><span class="sxs-lookup"><span data-stu-id="aa3af-103">Deletes the service..</span></span> <span data-ttu-id="aa3af-104">Alla tjänste enheter som har skapats under en tjänst måste tas bort innan tjänsten tas bort.</span><span class="sxs-lookup"><span data-stu-id="aa3af-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="aa3af-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa3af-105">SYNTAX</span></span>

### <span data-ttu-id="aa3af-106">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="aa3af-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa3af-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="aa3af-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa3af-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="aa3af-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa3af-109">ID</span><span class="sxs-lookup"><span data-stu-id="aa3af-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa3af-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="aa3af-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa3af-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa3af-111">DESCRIPTION</span></span>
<span data-ttu-id="aa3af-112">Cmdleten **Remove-AzDeploymentManagerService** tar bort en tjänst under en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="aa3af-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="aa3af-113">Ange tjänsten med dess namn, topologi den är i och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="aa3af-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="aa3af-114">Du kan också ange serviceobjektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="aa3af-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="aa3af-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa3af-115">EXAMPLES</span></span>

### <span data-ttu-id="aa3af-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="aa3af-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="aa3af-117">Det här kommandot tar bort en tjänst som heter ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="aa3af-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="aa3af-118">Exempel 2: ta bort en tjänst med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="aa3af-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="aa3af-119">Det här kommandot tar bort en tjänst som heter ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="aa3af-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="aa3af-120">Exempel 3: ta bort en tjänst med serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="aa3af-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="aa3af-121">Det här kommandot tar bort en tjänst vars namn, namn och ResourceGroup matchar namn, ServiceTopologyName och $serviceObject ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="aa3af-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="aa3af-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa3af-122">PARAMETERS</span></span>

### <span data-ttu-id="aa3af-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa3af-123">-DefaultProfile</span></span>
<span data-ttu-id="aa3af-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aa3af-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa3af-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa3af-125">-InputObject</span></span>
<span data-ttu-id="aa3af-126">Service objekt.</span><span class="sxs-lookup"><span data-stu-id="aa3af-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa3af-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="aa3af-127">-Name</span></span>
<span data-ttu-id="aa3af-128">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="aa3af-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa3af-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa3af-129">-PassThru</span></span>
<span data-ttu-id="aa3af-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="aa3af-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="aa3af-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa3af-131">-ResourceGroupName</span></span>
<span data-ttu-id="aa3af-132">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="aa3af-132">The resource group.</span></span>

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

### <span data-ttu-id="aa3af-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa3af-133">-ResourceId</span></span>
<span data-ttu-id="aa3af-134">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="aa3af-134">The resource identifier.</span></span>

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

### <span data-ttu-id="aa3af-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="aa3af-135">-ServiceTopologyName</span></span>
<span data-ttu-id="aa3af-136">Namnet på tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="aa3af-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="aa3af-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="aa3af-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="aa3af-138">Den tjänst Topology-objekt där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="aa3af-138">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa3af-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="aa3af-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="aa3af-140">Resurs-ID för tjänste topologi där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="aa3af-140">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa3af-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aa3af-141">-Confirm</span></span>
<span data-ttu-id="aa3af-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aa3af-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa3af-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa3af-143">-WhatIf</span></span>
<span data-ttu-id="aa3af-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aa3af-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa3af-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aa3af-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa3af-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3af-146">CommonParameters</span></span>
<span data-ttu-id="aa3af-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa3af-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa3af-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa3af-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa3af-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa3af-149">INPUTS</span></span>

### <span data-ttu-id="aa3af-150">System. String</span><span class="sxs-lookup"><span data-stu-id="aa3af-150">System.String</span></span>

### <span data-ttu-id="aa3af-151">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="aa3af-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="aa3af-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa3af-152">OUTPUTS</span></span>

### <span data-ttu-id="aa3af-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa3af-153">System.Boolean</span></span>

## <span data-ttu-id="aa3af-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa3af-154">NOTES</span></span>

## <span data-ttu-id="aa3af-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa3af-155">RELATED LINKS</span></span>
