---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 3dda11ec4fddde67a3ae4300f884290831ac28ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744398"
---
# <span data-ttu-id="06d64-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="06d64-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="06d64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06d64-102">SYNOPSIS</span></span>
<span data-ttu-id="06d64-103">Hämtar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="06d64-103">Gets the service.</span></span>

## <span data-ttu-id="06d64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06d64-104">SYNTAX</span></span>

### <span data-ttu-id="06d64-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="06d64-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06d64-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="06d64-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06d64-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="06d64-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06d64-108">ID</span><span class="sxs-lookup"><span data-stu-id="06d64-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06d64-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="06d64-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06d64-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06d64-110">DESCRIPTION</span></span>
<span data-ttu-id="06d64-111">Cmdleten **Get-AzDeploymentManagerService** får en tjänst under en tjänstmall och returnerar ett objekt som representerar den tjänsten.</span><span class="sxs-lookup"><span data-stu-id="06d64-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="06d64-112">Ange tjänsten med dess namn, topologi den är i och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="06d64-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="06d64-113">Du kan också ange serviceobjektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="06d64-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="06d64-114">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på tjänsten genom att använda Set-AzDeploymentManagerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06d64-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="06d64-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06d64-115">EXAMPLES</span></span>

### <span data-ttu-id="06d64-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06d64-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="06d64-117">Det här kommandot får en tjänst som heter ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="06d64-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="06d64-118">Exempel 2: Hämta en tjänst med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="06d64-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="06d64-119">Det här kommandot får en tjänst som heter ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="06d64-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="06d64-120">Exempel 3: Hämta en tjänst med serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="06d64-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="06d64-121">Det här kommandot får en tjänst vars namn, namn och ResourceGroup matchar namn, ServiceTopologyName och $serviceObject ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="06d64-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="06d64-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06d64-122">PARAMETERS</span></span>

### <span data-ttu-id="06d64-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d64-123">-DefaultProfile</span></span>
<span data-ttu-id="06d64-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06d64-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d64-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06d64-125">-InputObject</span></span>
<span data-ttu-id="06d64-126">Service objekt.</span><span class="sxs-lookup"><span data-stu-id="06d64-126">Service object.</span></span>

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

### <span data-ttu-id="06d64-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="06d64-127">-Name</span></span>
<span data-ttu-id="06d64-128">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="06d64-128">The name of the service.</span></span>

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

### <span data-ttu-id="06d64-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d64-129">-ResourceGroupName</span></span>
<span data-ttu-id="06d64-130">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="06d64-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d64-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06d64-131">-ResourceId</span></span>
<span data-ttu-id="06d64-132">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="06d64-132">The resource identifier.</span></span>

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

### <span data-ttu-id="06d64-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="06d64-133">-ServiceTopologyName</span></span>
<span data-ttu-id="06d64-134">Namnet på tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="06d64-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="06d64-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="06d64-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="06d64-136">Den tjänst Topology-objekt där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="06d64-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="06d64-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="06d64-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="06d64-138">Resurs-ID för tjänste topologi där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="06d64-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="06d64-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d64-139">CommonParameters</span></span>
<span data-ttu-id="06d64-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d64-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d64-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d64-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d64-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06d64-142">INPUTS</span></span>

### <span data-ttu-id="06d64-143">System. String</span><span class="sxs-lookup"><span data-stu-id="06d64-143">System.String</span></span>

### <span data-ttu-id="06d64-144">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="06d64-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="06d64-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06d64-145">OUTPUTS</span></span>

### <span data-ttu-id="06d64-146">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="06d64-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="06d64-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06d64-147">NOTES</span></span>

## <span data-ttu-id="06d64-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06d64-148">RELATED LINKS</span></span>
