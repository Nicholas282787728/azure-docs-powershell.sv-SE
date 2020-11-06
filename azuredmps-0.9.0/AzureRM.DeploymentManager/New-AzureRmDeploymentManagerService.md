---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 25b4adeb2d62f1e66bd30cd990db27eadb41b405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572188"
---
# <span data-ttu-id="abec5-101">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="abec5-101">New-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="abec5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abec5-102">SYNOPSIS</span></span>
<span data-ttu-id="abec5-103">Skapar en tjänst i en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="abec5-103">Creates a service in a service topology.</span></span>

## <span data-ttu-id="abec5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abec5-104">SYNTAX</span></span>

### <span data-ttu-id="abec5-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="abec5-105">Interactive (Default)</span></span>
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 -Name <String> -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abec5-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="abec5-106">ByServiceTopologyObject</span></span>
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopology] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abec5-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="abec5-107">ByServiceTopologyResourceId</span></span>
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abec5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abec5-108">DESCRIPTION</span></span>
<span data-ttu-id="abec5-109">Cmdleten **New-AzureRmDeploymentManagerService** skapar en tjänst under en tjänstmall och returnerar ett objekt som representerar den tjänsten.</span><span class="sxs-lookup"><span data-stu-id="abec5-109">The **New-AzureRmDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="abec5-110">Ange tjänsten med dess namn, topologi den är i och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="abec5-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="abec5-111">Cmdleten returnerar ett tjänst objekt.</span><span class="sxs-lookup"><span data-stu-id="abec5-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="abec5-112">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på tjänsten genom att använda Set-AzureRmDeploymentManagerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abec5-112">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="abec5-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abec5-113">EXAMPLES</span></span>

### <span data-ttu-id="abec5-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="abec5-114">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="abec5-115">Skapar en ny tjänst med namnet ContosoService1 under topologi för ContosoServiceTopology i resurs grupp ContosoResourceGroup i plats centralen.</span><span class="sxs-lookup"><span data-stu-id="abec5-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="abec5-116">Egenskapen TargetLocation anger att tjänsten ContosoService1 ska distribueras till regionen Östra USA i prenumerationen som anges.</span><span class="sxs-lookup"><span data-stu-id="abec5-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="abec5-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abec5-117">PARAMETERS</span></span>

### <span data-ttu-id="abec5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abec5-118">-DefaultProfile</span></span>
<span data-ttu-id="abec5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="abec5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abec5-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="abec5-120">-Location</span></span>
<span data-ttu-id="abec5-121">Tjänst resursens plats.</span><span class="sxs-lookup"><span data-stu-id="abec5-121">The location of the service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abec5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="abec5-122">-Name</span></span>
<span data-ttu-id="abec5-123">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="abec5-123">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abec5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abec5-124">-ResourceGroupName</span></span>
<span data-ttu-id="abec5-125">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="abec5-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abec5-126">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="abec5-126">-ServiceTopology</span></span>
<span data-ttu-id="abec5-127">Den tjänst Topology-objekt där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="abec5-127">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abec5-128">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="abec5-128">-ServiceTopologyId</span></span>
<span data-ttu-id="abec5-129">Resurs-ID för tjänste topologi där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="abec5-129">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abec5-130">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="abec5-130">-ServiceTopologyName</span></span>
<span data-ttu-id="abec5-131">Namnet på tjänst topologin som denna tjänst tillhör.</span><span class="sxs-lookup"><span data-stu-id="abec5-131">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="abec5-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="abec5-132">-Tag</span></span>
<span data-ttu-id="abec5-133">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="abec5-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abec5-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="abec5-134">-TargetLocation</span></span>
<span data-ttu-id="abec5-135">Bestämmer platsen där resurserna under tjänsten ska distribueras till.</span><span class="sxs-lookup"><span data-stu-id="abec5-135">Determines the location where resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abec5-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="abec5-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="abec5-137">Bestämmer vilken prenumeration som resurserna under tjänsten ska distribueras till.</span><span class="sxs-lookup"><span data-stu-id="abec5-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abec5-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abec5-138">-Confirm</span></span>
<span data-ttu-id="abec5-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abec5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abec5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abec5-140">-WhatIf</span></span>
<span data-ttu-id="abec5-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abec5-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abec5-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abec5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abec5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abec5-143">CommonParameters</span></span>
<span data-ttu-id="abec5-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abec5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abec5-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abec5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abec5-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abec5-146">INPUTS</span></span>

### <span data-ttu-id="abec5-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="abec5-147">None</span></span>

## <span data-ttu-id="abec5-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abec5-148">OUTPUTS</span></span>

### <span data-ttu-id="abec5-149">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="abec5-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="abec5-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abec5-150">NOTES</span></span>

## <span data-ttu-id="abec5-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abec5-151">RELATED LINKS</span></span>

[<span data-ttu-id="abec5-152">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="abec5-152">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="abec5-153">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="abec5-153">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="abec5-154">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="abec5-154">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)