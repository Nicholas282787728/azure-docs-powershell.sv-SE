---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: f80f67270652d9c9edef38c9eb793074acd95a27
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320159"
---
# <span data-ttu-id="83dbd-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="83dbd-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="83dbd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="83dbd-103">Hämtar tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="83dbd-103">Gets the service unit.</span></span>

## <span data-ttu-id="83dbd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83dbd-104">SYNTAX</span></span>

### <span data-ttu-id="83dbd-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="83dbd-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83dbd-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="83dbd-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83dbd-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="83dbd-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83dbd-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="83dbd-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83dbd-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="83dbd-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83dbd-110">ID</span><span class="sxs-lookup"><span data-stu-id="83dbd-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83dbd-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="83dbd-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83dbd-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83dbd-112">DESCRIPTION</span></span>
<span data-ttu-id="83dbd-113">Cmdleten **Get-AzDeploymentManagerServiceUnit** får en tjänst enhet i en tjänst.</span><span class="sxs-lookup"><span data-stu-id="83dbd-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="83dbd-114">Ange tjänst enheten efter dess namn, den tjänst som den har definierats under, namnet på tjänst sto pol Ogin och resurs grupp namnet.</span><span class="sxs-lookup"><span data-stu-id="83dbd-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="83dbd-115">Du kan också ange ServiceUnit-objektet eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="83dbd-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="83dbd-116">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på tjänst enheten genom att använda Set-AzDeploymentManagerServiceUnit cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83dbd-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="83dbd-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83dbd-117">EXAMPLES</span></span>

### <span data-ttu-id="83dbd-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="83dbd-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="83dbd-119">Det här kommandot får en tjänst enhet som heter ContosoService1Storage under en tjänst ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="83dbd-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="83dbd-120">Exempel 2: skaffa en tjänst enhet med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="83dbd-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="83dbd-121">Det här kommandot får en tjänst enhet som heter ContosoService1Storage under en tjänst ContosoService1 i en tjänstmall som heter ContosoServiceTopology i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="83dbd-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="83dbd-122">Exempel 3: skaffa en tjänst enhet med hjälp av objektet tjänst.</span><span class="sxs-lookup"><span data-stu-id="83dbd-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="83dbd-123">Det här kommandot får en tjänst enhet vars namn, tjänst namn, namn på tjänste topologi och ResourceGroup matchar namnet, ServiceName, ServiceTopologyName och ResourceGroupName för $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="83dbd-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="83dbd-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83dbd-124">PARAMETERS</span></span>

### <span data-ttu-id="83dbd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83dbd-125">-DefaultProfile</span></span>
<span data-ttu-id="83dbd-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83dbd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83dbd-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83dbd-127">-InputObject</span></span>
<span data-ttu-id="83dbd-128">Tjänst enhetens resurs objekt.</span><span class="sxs-lookup"><span data-stu-id="83dbd-128">Service unit resource object.</span></span>

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

### <span data-ttu-id="83dbd-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="83dbd-129">-Name</span></span>
<span data-ttu-id="83dbd-130">Namnet på tjänste enheten.</span><span class="sxs-lookup"><span data-stu-id="83dbd-130">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83dbd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83dbd-131">-ResourceGroupName</span></span>
<span data-ttu-id="83dbd-132">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="83dbd-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83dbd-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83dbd-133">-ResourceId</span></span>
<span data-ttu-id="83dbd-134">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="83dbd-134">The resource identifier.</span></span>

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

### <span data-ttu-id="83dbd-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="83dbd-135">-ServiceName</span></span>
<span data-ttu-id="83dbd-136">Namnet på tjänsten som tjänst enheten är en del av.</span><span class="sxs-lookup"><span data-stu-id="83dbd-136">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="83dbd-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="83dbd-137">-ServiceObject</span></span>
<span data-ttu-id="83dbd-138">Serviceobjektet där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="83dbd-138">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="83dbd-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="83dbd-139">-ServiceResourceId</span></span>
<span data-ttu-id="83dbd-140">ID för tjänste resursen där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="83dbd-140">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="83dbd-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="83dbd-141">-ServiceTopologyName</span></span>
<span data-ttu-id="83dbd-142">Namnet på den tjänstmall som tjänst enheten är en del av.</span><span class="sxs-lookup"><span data-stu-id="83dbd-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="83dbd-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="83dbd-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="83dbd-144">Det tjänst Topology-objekt där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="83dbd-144">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="83dbd-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="83dbd-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="83dbd-146">Resurs-ID för tjänste topologi där tjänst enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="83dbd-146">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="83dbd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83dbd-147">CommonParameters</span></span>
<span data-ttu-id="83dbd-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83dbd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83dbd-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83dbd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83dbd-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83dbd-150">INPUTS</span></span>

### <span data-ttu-id="83dbd-151">System. String</span><span class="sxs-lookup"><span data-stu-id="83dbd-151">System.String</span></span>

### <span data-ttu-id="83dbd-152">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="83dbd-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="83dbd-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83dbd-153">OUTPUTS</span></span>

### <span data-ttu-id="83dbd-154">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="83dbd-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="83dbd-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83dbd-155">NOTES</span></span>

## <span data-ttu-id="83dbd-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83dbd-156">RELATED LINKS</span></span>