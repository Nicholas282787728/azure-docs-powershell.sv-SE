---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4b2cd4ef2dde674b10d51dc378578acbd13c4a7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571424"
---
# <span data-ttu-id="65442-101">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="65442-101">Remove-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="65442-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65442-102">SYNOPSIS</span></span>
<span data-ttu-id="65442-103">Tar bort en tjänst i en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="65442-103">Deletes a service in a service topology.</span></span>

## <span data-ttu-id="65442-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65442-104">SYNTAX</span></span>

### <span data-ttu-id="65442-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="65442-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65442-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="65442-106">ByServiceTopologyObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65442-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="65442-107">ByServiceTopologyResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65442-108">ID</span><span class="sxs-lookup"><span data-stu-id="65442-108">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65442-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="65442-109">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65442-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65442-110">DESCRIPTION</span></span>
<span data-ttu-id="65442-111">Cmdleten **Remove-AzureRmDeploymentManagerService** tar bort en tjänst under en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="65442-111">The **Remove-AzureRmDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="65442-112">Ange tjänsten med dess namn, topologi den är i och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="65442-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="65442-113">Du kan också ange serviceobjektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="65442-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="65442-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65442-114">EXAMPLES</span></span>

### <span data-ttu-id="65442-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="65442-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="65442-116">Det här kommandot tar bort en tjänst som heter ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="65442-116">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="65442-117">Exempel 2: ta bort en tjänst med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="65442-117">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="65442-118">Det här kommandot tar bort en tjänst som heter ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="65442-118">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="65442-119">Exempel 3: ta bort en tjänst med serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="65442-119">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="65442-120">Det här kommandot tar bort en tjänst vars namn, namn och ResourceGroup matchar namn, ServiceTopologyName och $serviceObject ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="65442-120">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="65442-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65442-121">PARAMETERS</span></span>

### <span data-ttu-id="65442-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65442-122">-DefaultProfile</span></span>
<span data-ttu-id="65442-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65442-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65442-124">-Force</span><span class="sxs-lookup"><span data-stu-id="65442-124">-Force</span></span>
<span data-ttu-id="65442-125">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="65442-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="65442-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="65442-126">-Name</span></span>
<span data-ttu-id="65442-127">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="65442-127">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65442-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65442-128">-PassThru</span></span>
<span data-ttu-id="65442-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="65442-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="65442-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65442-130">-ResourceGroupName</span></span>
<span data-ttu-id="65442-131">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="65442-131">The resource group.</span></span>

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

### <span data-ttu-id="65442-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65442-132">-ResourceId</span></span>
<span data-ttu-id="65442-133">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="65442-133">The resource identifier.</span></span>

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

### <span data-ttu-id="65442-134">-Service</span><span class="sxs-lookup"><span data-stu-id="65442-134">-Service</span></span>
<span data-ttu-id="65442-135">Resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="65442-135">The resource to be removed.</span></span>

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

### <span data-ttu-id="65442-136">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="65442-136">-ServiceTopology</span></span>
<span data-ttu-id="65442-137">Den tjänst Topology-objekt där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="65442-137">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="65442-138">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="65442-138">-ServiceTopologyName</span></span>
<span data-ttu-id="65442-139">Namnet på tjänst sto pol Ogin tjänsten tillhör.</span><span class="sxs-lookup"><span data-stu-id="65442-139">The name of the service topology the service belongs to.</span></span>

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

### <span data-ttu-id="65442-140">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="65442-140">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="65442-141">Resurs-ID för tjänste topologi där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="65442-141">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="65442-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="65442-142">-Confirm</span></span>
<span data-ttu-id="65442-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65442-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65442-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65442-144">-WhatIf</span></span>
<span data-ttu-id="65442-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="65442-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65442-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="65442-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65442-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65442-147">CommonParameters</span></span>
<span data-ttu-id="65442-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65442-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65442-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65442-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65442-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65442-150">INPUTS</span></span>

### <span data-ttu-id="65442-151">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="65442-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="65442-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65442-152">OUTPUTS</span></span>

### <span data-ttu-id="65442-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65442-153">System.Boolean</span></span>

## <span data-ttu-id="65442-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65442-154">NOTES</span></span>

## <span data-ttu-id="65442-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65442-155">RELATED LINKS</span></span>

[<span data-ttu-id="65442-156">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="65442-156">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="65442-157">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="65442-157">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="65442-158">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="65442-158">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)