---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
content_git_url: ''
ms.openlocfilehash: 655cfeeae35d1b48bbfe2149fd4262dffe72ae09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572440"
---
# <span data-ttu-id="75570-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="75570-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="75570-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75570-102">SYNOPSIS</span></span>
<span data-ttu-id="75570-103">Hämtar en tjänst i en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="75570-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="75570-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75570-104">SYNTAX</span></span>

### <span data-ttu-id="75570-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="75570-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75570-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="75570-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75570-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="75570-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75570-108">ID</span><span class="sxs-lookup"><span data-stu-id="75570-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75570-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="75570-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75570-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75570-110">DESCRIPTION</span></span>
<span data-ttu-id="75570-111">Cmdleten **Get-AzureRmDeploymentManagerService** får en tjänst under en tjänstmall och returnerar ett objekt som representerar den tjänsten.</span><span class="sxs-lookup"><span data-stu-id="75570-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="75570-112">Ange tjänsten med dess namn, topologi den är i och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="75570-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="75570-113">Du kan också ange serviceobjektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="75570-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="75570-114">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på tjänsten genom att använda Set-AzureRmDeploymentManagerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75570-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="75570-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75570-115">EXAMPLES</span></span>

### <span data-ttu-id="75570-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="75570-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="75570-117">Det här kommandot får en tjänst som heter ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="75570-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="75570-118">Exempel 2: Hämta en tjänst med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="75570-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="75570-119">Det här kommandot får en tjänst som heter ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="75570-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="75570-120">Exempel 3: Hämta en tjänst med serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="75570-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="75570-121">Det här kommandot får en tjänst vars namn, namn och ResourceGroup matchar namn, ServiceTopologyName och $serviceObject ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="75570-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="75570-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75570-122">PARAMETERS</span></span>

### <span data-ttu-id="75570-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75570-123">-DefaultProfile</span></span>
<span data-ttu-id="75570-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75570-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75570-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="75570-125">-Name</span></span>
<span data-ttu-id="75570-126">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="75570-126">The name of the service.</span></span>

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

### <span data-ttu-id="75570-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75570-127">-ResourceGroupName</span></span>
<span data-ttu-id="75570-128">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="75570-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75570-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75570-129">-ResourceId</span></span>
<span data-ttu-id="75570-130">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="75570-130">The resource identifier.</span></span>

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

### <span data-ttu-id="75570-131">-Service</span><span class="sxs-lookup"><span data-stu-id="75570-131">-Service</span></span>
<span data-ttu-id="75570-132">Service objekt.</span><span class="sxs-lookup"><span data-stu-id="75570-132">Service object.</span></span>

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

### <span data-ttu-id="75570-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="75570-133">-ServiceTopology</span></span>
<span data-ttu-id="75570-134">Den tjänst Topology-objekt där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="75570-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="75570-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="75570-135">-ServiceTopologyName</span></span>
<span data-ttu-id="75570-136">Namnet på tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="75570-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="75570-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="75570-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="75570-138">Resurs-ID för tjänste topologi där tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="75570-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="75570-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75570-139">CommonParameters</span></span>
<span data-ttu-id="75570-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75570-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75570-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75570-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75570-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75570-142">INPUTS</span></span>

### <span data-ttu-id="75570-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="75570-143">None</span></span>

## <span data-ttu-id="75570-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75570-144">OUTPUTS</span></span>

### <span data-ttu-id="75570-145">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="75570-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="75570-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75570-146">NOTES</span></span>

## <span data-ttu-id="75570-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75570-147">RELATED LINKS</span></span>

[<span data-ttu-id="75570-148">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="75570-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="75570-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="75570-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="75570-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="75570-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)