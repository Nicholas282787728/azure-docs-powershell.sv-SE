---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320163"
---
# <span data-ttu-id="3c192-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="3c192-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="3c192-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c192-102">SYNOPSIS</span></span>
<span data-ttu-id="3c192-103">Hämtar tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="3c192-103">Gets the service topology.</span></span>

## <span data-ttu-id="3c192-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c192-104">SYNTAX</span></span>

### <span data-ttu-id="3c192-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="3c192-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c192-106">ID</span><span class="sxs-lookup"><span data-stu-id="3c192-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c192-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3c192-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c192-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c192-108">DESCRIPTION</span></span>
<span data-ttu-id="3c192-109">Cmdleten **Get-AzDeploymentManagerServiceTopology** får en tjänst sto rad topologi.</span><span class="sxs-lookup"><span data-stu-id="3c192-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="3c192-110">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på topologin med hjälp av Set-AzDeploymentManagerServiceTopology cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c192-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="3c192-111">Ange tjänst sto pol Ogin efter dess namn och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3c192-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="3c192-112">Du kan också ange ServiceTopology-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="3c192-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="3c192-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c192-113">EXAMPLES</span></span>

### <span data-ttu-id="3c192-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3c192-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="3c192-115">Det här kommandot får en tjänst sto pol ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3c192-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3c192-116">Exempel 2: Hämta en tjänst sto pol Ogin med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3c192-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="3c192-117">Det här kommandot får en tjänst sto pol ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3c192-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3c192-118">Exempel 3: Hämta en tjänst sto pol using the tjänst Topology-objektet.</span><span class="sxs-lookup"><span data-stu-id="3c192-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="3c192-119">Det här kommandot får en tjänst sto ras vars namn och ResourceGroup matchar $serviceTopologyObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="3c192-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="3c192-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c192-120">PARAMETERS</span></span>

### <span data-ttu-id="3c192-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c192-121">-DefaultProfile</span></span>
<span data-ttu-id="3c192-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c192-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c192-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c192-123">-InputObject</span></span>
<span data-ttu-id="3c192-124">Resurs objekt för tjänst topologi.</span><span class="sxs-lookup"><span data-stu-id="3c192-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="3c192-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="3c192-125">-Name</span></span>
<span data-ttu-id="3c192-126">Namnet på tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="3c192-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c192-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c192-127">-ResourceGroupName</span></span>
<span data-ttu-id="3c192-128">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3c192-128">The resource group.</span></span>

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

### <span data-ttu-id="3c192-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c192-129">-ResourceId</span></span>
<span data-ttu-id="3c192-130">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3c192-130">The resource identifier.</span></span>

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

### <span data-ttu-id="3c192-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c192-131">CommonParameters</span></span>
<span data-ttu-id="3c192-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c192-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c192-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c192-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c192-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c192-134">INPUTS</span></span>

### <span data-ttu-id="3c192-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3c192-135">System.String</span></span>

### <span data-ttu-id="3c192-136">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="3c192-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="3c192-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c192-137">OUTPUTS</span></span>

### <span data-ttu-id="3c192-138">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="3c192-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="3c192-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c192-139">NOTES</span></span>

## <span data-ttu-id="3c192-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c192-140">RELATED LINKS</span></span>
