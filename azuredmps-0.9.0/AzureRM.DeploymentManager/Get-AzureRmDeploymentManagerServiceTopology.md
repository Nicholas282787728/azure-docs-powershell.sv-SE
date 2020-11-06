---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572444"
---
# <span data-ttu-id="1a068-101">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1a068-101">Get-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="1a068-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a068-102">SYNOPSIS</span></span>
<span data-ttu-id="1a068-103">Hämtar en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="1a068-103">Gets a service topology.</span></span>

## <span data-ttu-id="1a068-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a068-104">SYNTAX</span></span>

### <span data-ttu-id="1a068-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="1a068-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a068-106">ID</span><span class="sxs-lookup"><span data-stu-id="1a068-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a068-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1a068-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a068-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a068-108">DESCRIPTION</span></span>
<span data-ttu-id="1a068-109">Cmdleten **Get-AzureRmDeploymentManagerServiceTopology** får en tjänst sto rad topologi.</span><span class="sxs-lookup"><span data-stu-id="1a068-109">The **Get-AzureRmDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="1a068-110">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på topologin med hjälp av Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a068-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="1a068-111">Ange tjänst sto pol Ogin efter dess namn och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1a068-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="1a068-112">Du kan också ange ServiceTopology-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1a068-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="1a068-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a068-113">EXAMPLES</span></span>

### <span data-ttu-id="1a068-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1a068-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="1a068-115">Det här kommandot får en tjänst sto pol ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1a068-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1a068-116">Exempel 2: Hämta en tjänst sto pol Ogin med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1a068-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="1a068-117">Det här kommandot får en tjänst sto pol ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1a068-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1a068-118">Exempel 3: Hämta en tjänst sto pol using the tjänst Topology-objektet.</span><span class="sxs-lookup"><span data-stu-id="1a068-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="1a068-119">Det här kommandot får en tjänst sto ras vars namn och ResourceGroup matchar $serviceTopologyObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="1a068-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="1a068-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a068-120">PARAMETERS</span></span>

### <span data-ttu-id="1a068-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a068-121">-DefaultProfile</span></span>
<span data-ttu-id="1a068-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a068-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a068-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a068-123">-Name</span></span>
<span data-ttu-id="1a068-124">Namnet på tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="1a068-124">The name of the service topology.</span></span>

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

### <span data-ttu-id="1a068-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a068-125">-ResourceGroupName</span></span>
<span data-ttu-id="1a068-126">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1a068-126">The resource group.</span></span>

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

### <span data-ttu-id="1a068-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a068-127">-ResourceId</span></span>
<span data-ttu-id="1a068-128">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1a068-128">The resource identifier.</span></span>

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

### <span data-ttu-id="1a068-129">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1a068-129">-ServiceTopology</span></span>
<span data-ttu-id="1a068-130">Resurs objekt för tjänst topologi.</span><span class="sxs-lookup"><span data-stu-id="1a068-130">Service topology resource object.</span></span>

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

### <span data-ttu-id="1a068-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a068-131">CommonParameters</span></span>
<span data-ttu-id="1a068-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a068-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a068-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a068-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a068-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a068-134">INPUTS</span></span>

### <span data-ttu-id="1a068-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="1a068-135">None</span></span>

## <span data-ttu-id="1a068-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a068-136">OUTPUTS</span></span>

### <span data-ttu-id="1a068-137">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="1a068-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="1a068-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a068-138">NOTES</span></span>

## <span data-ttu-id="1a068-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a068-139">RELATED LINKS</span></span>

[<span data-ttu-id="1a068-140">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1a068-140">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="1a068-141">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1a068-141">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="1a068-142">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1a068-142">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)