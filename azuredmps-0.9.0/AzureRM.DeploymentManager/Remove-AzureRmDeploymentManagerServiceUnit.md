---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: 993b250b0c49efc448c0198c4e9a3aea29f77714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572203"
---
# <span data-ttu-id="170d2-101">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="170d2-101">Remove-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="170d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="170d2-102">SYNOPSIS</span></span>
<span data-ttu-id="170d2-103">Tar bort tjänst enheten för en tjänst i en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="170d2-103">Deletes the service unit of a service in a service topology.</span></span>

## <span data-ttu-id="170d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="170d2-104">SYNTAX</span></span>

### <span data-ttu-id="170d2-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="170d2-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170d2-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="170d2-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170d2-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="170d2-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170d2-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="170d2-108">ByServiceObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170d2-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="170d2-109">ByServiceResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170d2-110">ID</span><span class="sxs-lookup"><span data-stu-id="170d2-110">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170d2-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="170d2-111">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="170d2-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="170d2-112">DESCRIPTION</span></span>
<span data-ttu-id="170d2-113">Cmdleten **Remove-AzureRmDeploymentManagerServiceUnit** tar bort en tjänst enhet i en tjänst.</span><span class="sxs-lookup"><span data-stu-id="170d2-113">The **Remove-AzureRmDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="170d2-114">Ange tjänst enheten efter dess namn, den tjänst som den har definierats under, namnet på tjänst sto pol Ogin och resurs grupp namnet.</span><span class="sxs-lookup"><span data-stu-id="170d2-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="170d2-115">Du kan också ange ServiceUnit-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="170d2-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="170d2-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="170d2-116">EXAMPLES</span></span>

### <span data-ttu-id="170d2-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="170d2-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="170d2-118">Det här kommandot tar bort en tjänst enhet med namnet ContosoService1Storage under en tjänst-ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="170d2-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="170d2-119">Exempel 2: ta bort en tjänst enhet med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="170d2-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="170d2-120">Det här kommandot får en tjänst enhet som heter ContosoService1Storage under en tjänst ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="170d2-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="170d2-121">Exempel 3: ta bort en tjänst enhet med hjälp av serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="170d2-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="170d2-122">Det här kommandot tar bort en tjänst enhet vars namn, tjänst namn, namn på tjänste topologi och ResourceGroup matchar namnet, ServiceName, ServiceTopologyName och ResourceGroupName för $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="170d2-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="170d2-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="170d2-123">PARAMETERS</span></span>

### <span data-ttu-id="170d2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170d2-124">-DefaultProfile</span></span>
<span data-ttu-id="170d2-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="170d2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="170d2-126">-Force</span><span class="sxs-lookup"><span data-stu-id="170d2-126">-Force</span></span>
<span data-ttu-id="170d2-127">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="170d2-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="170d2-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="170d2-128">-Name</span></span>
<span data-ttu-id="170d2-129">Namnet på den tjänst enhet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="170d2-129">The name of the service unit to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170d2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="170d2-130">-PassThru</span></span>
<span data-ttu-id="170d2-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="170d2-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="170d2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170d2-132">-ResourceGroupName</span></span>
<span data-ttu-id="170d2-133">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="170d2-133">The resource group.</span></span>

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

### <span data-ttu-id="170d2-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="170d2-134">-ResourceId</span></span>
<span data-ttu-id="170d2-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="170d2-135">The resource identifier.</span></span>

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

### <span data-ttu-id="170d2-136">-Service</span><span class="sxs-lookup"><span data-stu-id="170d2-136">-Service</span></span>
<span data-ttu-id="170d2-137">Serviceobjektet där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="170d2-137">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="170d2-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="170d2-138">-ServiceName</span></span>
<span data-ttu-id="170d2-139">Namnet på tjänsten som tjänste enheten tillhör.</span><span class="sxs-lookup"><span data-stu-id="170d2-139">The name of the service the service unit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170d2-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="170d2-140">-ServiceResourceId</span></span>
<span data-ttu-id="170d2-141">ID för tjänste resursen där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="170d2-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="170d2-142">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="170d2-142">-ServiceTopology</span></span>
<span data-ttu-id="170d2-143">Det tjänst Topology-objekt där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="170d2-143">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="170d2-144">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="170d2-144">-ServiceTopologyName</span></span>
<span data-ttu-id="170d2-145">Namnet på den tjänstmall som tjänste enheten tillhör.</span><span class="sxs-lookup"><span data-stu-id="170d2-145">The name of the service topology the service unit belongs to.</span></span>

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

### <span data-ttu-id="170d2-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="170d2-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="170d2-147">Resurs-ID för tjänste topologi där tjänst enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="170d2-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="170d2-148">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="170d2-148">-ServiceUnit</span></span>
<span data-ttu-id="170d2-149">Resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="170d2-149">The resource to be removed.</span></span>

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

### <span data-ttu-id="170d2-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="170d2-150">-Confirm</span></span>
<span data-ttu-id="170d2-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="170d2-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="170d2-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="170d2-152">-WhatIf</span></span>
<span data-ttu-id="170d2-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="170d2-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="170d2-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="170d2-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="170d2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170d2-155">CommonParameters</span></span>
<span data-ttu-id="170d2-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170d2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170d2-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170d2-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170d2-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="170d2-158">INPUTS</span></span>

### <span data-ttu-id="170d2-159">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="170d2-159">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="170d2-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="170d2-160">OUTPUTS</span></span>

### <span data-ttu-id="170d2-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="170d2-161">System.Boolean</span></span>

## <span data-ttu-id="170d2-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="170d2-162">NOTES</span></span>

## <span data-ttu-id="170d2-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="170d2-163">RELATED LINKS</span></span>

[<span data-ttu-id="170d2-164">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="170d2-164">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="170d2-165">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="170d2-165">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="170d2-166">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="170d2-166">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)