---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3ba27cf26ccc555ea79a2b46100bee6be7e3c7fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744369"
---
# <span data-ttu-id="2ca44-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="2ca44-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="2ca44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ca44-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca44-103">Tar bort tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="2ca44-103">Deletes the service unit.</span></span>

## <span data-ttu-id="2ca44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ca44-104">SYNTAX</span></span>

### <span data-ttu-id="2ca44-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="2ca44-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca44-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="2ca44-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca44-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="2ca44-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca44-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="2ca44-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca44-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="2ca44-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca44-110">ID</span><span class="sxs-lookup"><span data-stu-id="2ca44-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca44-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="2ca44-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca44-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ca44-112">DESCRIPTION</span></span>
<span data-ttu-id="2ca44-113">Cmdleten **Remove-AzDeploymentManagerServiceUnit** tar bort en tjänst enhet i en tjänst.</span><span class="sxs-lookup"><span data-stu-id="2ca44-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="2ca44-114">Ange tjänst enheten efter dess namn, den tjänst som den har definierats under, namnet på tjänst sto pol Ogin och resurs grupp namnet.</span><span class="sxs-lookup"><span data-stu-id="2ca44-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="2ca44-115">Du kan också ange ServiceUnit-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2ca44-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="2ca44-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ca44-116">EXAMPLES</span></span>

### <span data-ttu-id="2ca44-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2ca44-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="2ca44-118">Det här kommandot tar bort en tjänst enhet med namnet ContosoService1Storage under en tjänst-ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2ca44-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2ca44-119">Exempel 2: ta bort en tjänst enhet med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2ca44-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="2ca44-120">Det här kommandot får en tjänst enhet som heter ContosoService1Storage under en tjänst ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2ca44-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2ca44-121">Exempel 3: ta bort en tjänst enhet med hjälp av serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="2ca44-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="2ca44-122">Det här kommandot tar bort en tjänst enhet vars namn, tjänst namn, namn på tjänste topologi och ResourceGroup matchar namnet, ServiceName, ServiceTopologyName och ResourceGroupName för $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="2ca44-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="2ca44-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ca44-123">PARAMETERS</span></span>

### <span data-ttu-id="2ca44-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca44-124">-DefaultProfile</span></span>
<span data-ttu-id="2ca44-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ca44-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ca44-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ca44-126">-InputObject</span></span>
<span data-ttu-id="2ca44-127">Tjänst enhetens resurs objekt.</span><span class="sxs-lookup"><span data-stu-id="2ca44-127">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca44-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="2ca44-128">-Name</span></span>
<span data-ttu-id="2ca44-129">Namnet på tjänste enheten.</span><span class="sxs-lookup"><span data-stu-id="2ca44-129">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca44-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ca44-130">-PassThru</span></span>
<span data-ttu-id="2ca44-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2ca44-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2ca44-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca44-132">-ResourceGroupName</span></span>
<span data-ttu-id="2ca44-133">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2ca44-133">The resource group.</span></span>

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

### <span data-ttu-id="2ca44-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ca44-134">-ResourceId</span></span>
<span data-ttu-id="2ca44-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2ca44-135">The resource identifier.</span></span>

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

### <span data-ttu-id="2ca44-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2ca44-136">-ServiceName</span></span>
<span data-ttu-id="2ca44-137">Namnet på tjänsten som tjänst enheten är en del av.</span><span class="sxs-lookup"><span data-stu-id="2ca44-137">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca44-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="2ca44-138">-ServiceObject</span></span>
<span data-ttu-id="2ca44-139">Serviceobjektet där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2ca44-139">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca44-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="2ca44-140">-ServiceResourceId</span></span>
<span data-ttu-id="2ca44-141">ID för tjänste resursen där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2ca44-141">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca44-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="2ca44-142">-ServiceTopologyName</span></span>
<span data-ttu-id="2ca44-143">Namnet på den tjänstmall som tjänst enheten är en del av.</span><span class="sxs-lookup"><span data-stu-id="2ca44-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="2ca44-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="2ca44-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="2ca44-145">Det tjänst Topology-objekt där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2ca44-145">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca44-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="2ca44-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="2ca44-147">Resurs-ID för tjänste topologi där tjänst enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2ca44-147">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca44-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ca44-148">-Confirm</span></span>
<span data-ttu-id="2ca44-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ca44-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca44-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca44-150">-WhatIf</span></span>
<span data-ttu-id="2ca44-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ca44-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ca44-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ca44-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca44-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca44-153">CommonParameters</span></span>
<span data-ttu-id="2ca44-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ca44-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca44-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca44-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca44-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ca44-156">INPUTS</span></span>

### <span data-ttu-id="2ca44-157">System. String</span><span class="sxs-lookup"><span data-stu-id="2ca44-157">System.String</span></span>

### <span data-ttu-id="2ca44-158">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="2ca44-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="2ca44-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ca44-159">OUTPUTS</span></span>

### <span data-ttu-id="2ca44-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ca44-160">System.Boolean</span></span>

## <span data-ttu-id="2ca44-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ca44-161">NOTES</span></span>

## <span data-ttu-id="2ca44-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ca44-162">RELATED LINKS</span></span>
