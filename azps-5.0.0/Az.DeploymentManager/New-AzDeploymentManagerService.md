---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: aec721a3676a6b4510c7fe0eccf5badc4f9ccce2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320148"
---
# <span data-ttu-id="65e91-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="65e91-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="65e91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65e91-102">SYNOPSIS</span></span>
<span data-ttu-id="65e91-103">Skapar en tjänst under den angivna tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="65e91-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="65e91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65e91-104">SYNTAX</span></span>

### <span data-ttu-id="65e91-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="65e91-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65e91-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="65e91-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65e91-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="65e91-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65e91-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65e91-108">DESCRIPTION</span></span>
<span data-ttu-id="65e91-109">Cmdleten **New-AzDeploymentManagerService** skapar en tjänst under en tjänstmall och returnerar ett objekt som representerar den tjänsten.</span><span class="sxs-lookup"><span data-stu-id="65e91-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="65e91-110">Ange tjänsten med dess namn, topologi den är i och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="65e91-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="65e91-111">Cmdleten returnerar ett tjänst objekt.</span><span class="sxs-lookup"><span data-stu-id="65e91-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="65e91-112">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på tjänsten genom att använda Set-AzDeploymentManagerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65e91-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="65e91-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65e91-113">EXAMPLES</span></span>

### <span data-ttu-id="65e91-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="65e91-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="65e91-115">Skapar en ny tjänst med namnet ContosoService1 under topologi för ContosoServiceTopology i resurs grupp ContosoResourceGroup i plats centralen.</span><span class="sxs-lookup"><span data-stu-id="65e91-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="65e91-116">Egenskapen TargetLocation anger att tjänsten ContosoService1 ska distribueras till regionen Östra USA i prenumerationen som anges.</span><span class="sxs-lookup"><span data-stu-id="65e91-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="65e91-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65e91-117">PARAMETERS</span></span>

### <span data-ttu-id="65e91-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e91-118">-DefaultProfile</span></span>
<span data-ttu-id="65e91-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65e91-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65e91-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="65e91-120">-Location</span></span>
<span data-ttu-id="65e91-121">Tjänst resursens plats.</span><span class="sxs-lookup"><span data-stu-id="65e91-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="65e91-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="65e91-122">-Name</span></span>
<span data-ttu-id="65e91-123">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="65e91-123">The name of the service.</span></span>

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

### <span data-ttu-id="65e91-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e91-124">-ResourceGroupName</span></span>
<span data-ttu-id="65e91-125">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="65e91-125">The resource group.</span></span>

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

### <span data-ttu-id="65e91-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="65e91-126">-ServiceTopologyId</span></span>
<span data-ttu-id="65e91-127">Resurs-ID för tjänste topologi där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="65e91-127">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="65e91-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="65e91-128">-ServiceTopologyName</span></span>
<span data-ttu-id="65e91-129">Namnet på tjänst topologin som denna tjänst tillhör.</span><span class="sxs-lookup"><span data-stu-id="65e91-129">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="65e91-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="65e91-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="65e91-131">Den tjänst Topology-objekt där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="65e91-131">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="65e91-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="65e91-132">-Tag</span></span>
<span data-ttu-id="65e91-133">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="65e91-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e91-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="65e91-134">-TargetLocation</span></span>
<span data-ttu-id="65e91-135">Bestämmer platsen där resurserna under tjänsten ska distribueras till.</span><span class="sxs-lookup"><span data-stu-id="65e91-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="65e91-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65e91-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="65e91-137">Bestämmer vilken prenumeration som resurserna under tjänsten ska distribueras till.</span><span class="sxs-lookup"><span data-stu-id="65e91-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="65e91-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="65e91-138">-Confirm</span></span>
<span data-ttu-id="65e91-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65e91-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65e91-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65e91-140">-WhatIf</span></span>
<span data-ttu-id="65e91-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="65e91-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65e91-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="65e91-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65e91-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e91-143">CommonParameters</span></span>
<span data-ttu-id="65e91-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e91-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e91-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65e91-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e91-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65e91-146">INPUTS</span></span>

### <span data-ttu-id="65e91-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="65e91-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="65e91-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65e91-148">OUTPUTS</span></span>

### <span data-ttu-id="65e91-149">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="65e91-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="65e91-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65e91-150">NOTES</span></span>

## <span data-ttu-id="65e91-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65e91-151">RELATED LINKS</span></span>
