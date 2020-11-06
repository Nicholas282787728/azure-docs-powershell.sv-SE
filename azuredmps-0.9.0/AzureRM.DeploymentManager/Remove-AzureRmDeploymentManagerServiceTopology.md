---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: be95f5fffe4483c74d8b1438819cf084eaa0693b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571508"
---
# <span data-ttu-id="02d36-101">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="02d36-101">Remove-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="02d36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02d36-102">SYNOPSIS</span></span>
<span data-ttu-id="02d36-103">Tar bort en tjänst sto pol Ogin och alla dess resurser.</span><span class="sxs-lookup"><span data-stu-id="02d36-103">Deletes a service topology and all its resources.</span></span>

## <span data-ttu-id="02d36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02d36-104">SYNTAX</span></span>

### <span data-ttu-id="02d36-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="02d36-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02d36-106">ID</span><span class="sxs-lookup"><span data-stu-id="02d36-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02d36-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="02d36-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02d36-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02d36-108">DESCRIPTION</span></span>
<span data-ttu-id="02d36-109">Cmdleten **Remove-AzureRmDeploymentManagerServiceTopology** tar bort en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="02d36-109">The **Remove-AzureRmDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="02d36-110">Ange tjänst sto pol Ogin efter dess namn och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="02d36-110">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="02d36-111">Du kan också ange ServiceTopology-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="02d36-111">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="02d36-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02d36-112">EXAMPLES</span></span>

### <span data-ttu-id="02d36-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="02d36-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="02d36-114">Det här kommandot tar bort en tjänst sto pol ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="02d36-114">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="02d36-115">Exempel 2: ta bort en tjänst sto pol Ogin med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="02d36-115">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="02d36-116">Det här kommandot tar bort en tjänst sto pol ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="02d36-116">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="02d36-117">Exempel 3: ta bort en tjänst topologi med hjälp av objektet tjänst Topology.</span><span class="sxs-lookup"><span data-stu-id="02d36-117">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="02d36-118">Det här kommandot tar bort en tjänst sto pol Ogin vars namn och ResourceGroup matchar $serviceTopologyObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="02d36-118">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="02d36-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02d36-119">PARAMETERS</span></span>

### <span data-ttu-id="02d36-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d36-120">-DefaultProfile</span></span>
<span data-ttu-id="02d36-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02d36-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02d36-122">-Force</span><span class="sxs-lookup"><span data-stu-id="02d36-122">-Force</span></span>
<span data-ttu-id="02d36-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="02d36-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="02d36-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="02d36-124">-Name</span></span>
<span data-ttu-id="02d36-125">Namnet på tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="02d36-125">The name of the service topology.</span></span>

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

### <span data-ttu-id="02d36-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02d36-126">-PassThru</span></span>
<span data-ttu-id="02d36-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="02d36-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="02d36-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d36-128">-ResourceGroupName</span></span>
<span data-ttu-id="02d36-129">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="02d36-129">The resource group.</span></span>

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

### <span data-ttu-id="02d36-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02d36-130">-ResourceId</span></span>
<span data-ttu-id="02d36-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="02d36-131">The resource identifier.</span></span>

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

### <span data-ttu-id="02d36-132">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="02d36-132">-ServiceTopology</span></span>
<span data-ttu-id="02d36-133">Resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="02d36-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="02d36-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02d36-134">-Confirm</span></span>
<span data-ttu-id="02d36-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02d36-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02d36-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02d36-136">-WhatIf</span></span>
<span data-ttu-id="02d36-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02d36-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02d36-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02d36-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02d36-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d36-139">CommonParameters</span></span>
<span data-ttu-id="02d36-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d36-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d36-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d36-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d36-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02d36-142">INPUTS</span></span>

### <span data-ttu-id="02d36-143">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="02d36-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="02d36-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02d36-144">OUTPUTS</span></span>

### <span data-ttu-id="02d36-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02d36-145">System.Boolean</span></span>

## <span data-ttu-id="02d36-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02d36-146">NOTES</span></span>

## <span data-ttu-id="02d36-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02d36-147">RELATED LINKS</span></span>

[<span data-ttu-id="02d36-148">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="02d36-148">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="02d36-149">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="02d36-149">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="02d36-150">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="02d36-150">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)