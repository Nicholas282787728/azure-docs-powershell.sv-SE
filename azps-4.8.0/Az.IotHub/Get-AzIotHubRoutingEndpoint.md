---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260460"
---
# <span data-ttu-id="c93f3-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="c93f3-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="c93f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c93f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c93f3-103">Få information om alla slut punkter för din IoT Hub</span><span class="sxs-lookup"><span data-stu-id="c93f3-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="c93f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c93f3-104">SYNTAX</span></span>

### <span data-ttu-id="c93f3-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c93f3-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c93f3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c93f3-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c93f3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c93f3-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c93f3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c93f3-108">DESCRIPTION</span></span>
<span data-ttu-id="c93f3-109">Få information om slut punkten.</span><span class="sxs-lookup"><span data-stu-id="c93f3-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="c93f3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c93f3-110">EXAMPLES</span></span>

### <span data-ttu-id="c93f3-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c93f3-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="c93f3-112">Hämta alla slut punkter från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c93f3-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="c93f3-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c93f3-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="c93f3-114">Få alla slut punkter av typen EventHub från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c93f3-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="c93f3-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c93f3-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="c93f3-116">Få alla slut punkter av typen EventHub från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c93f3-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="c93f3-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="c93f3-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="c93f3-118">Hämta en slut punkts information från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c93f3-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="c93f3-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c93f3-119">PARAMETERS</span></span>

### <span data-ttu-id="c93f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c93f3-120">-DefaultProfile</span></span>
<span data-ttu-id="c93f3-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c93f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c93f3-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c93f3-122">-EndpointName</span></span>
<span data-ttu-id="c93f3-123">Namnet på cirkulations slut punkten</span><span class="sxs-lookup"><span data-stu-id="c93f3-123">Name of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93f3-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="c93f3-124">-EndpointType</span></span>
<span data-ttu-id="c93f3-125">Typ av cirkulations slut punkt</span><span class="sxs-lookup"><span data-stu-id="c93f3-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93f3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c93f3-126">-InputObject</span></span>
<span data-ttu-id="c93f3-127">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="c93f3-127">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c93f3-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="c93f3-128">-Name</span></span>
<span data-ttu-id="c93f3-129">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="c93f3-129">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93f3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c93f3-130">-ResourceGroupName</span></span>
<span data-ttu-id="c93f3-131">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c93f3-131">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93f3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c93f3-132">-ResourceId</span></span>
<span data-ttu-id="c93f3-133">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="c93f3-133">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c93f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93f3-134">CommonParameters</span></span>
<span data-ttu-id="c93f3-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c93f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93f3-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c93f3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93f3-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c93f3-137">INPUTS</span></span>

### <span data-ttu-id="c93f3-138">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c93f3-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c93f3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c93f3-139">System.String</span></span>

## <span data-ttu-id="c93f3-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c93f3-140">OUTPUTS</span></span>

### <span data-ttu-id="c93f3-141">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="c93f3-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="c93f3-142">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingEventHubProperties, Microsoft. Azure. PowerShell. cmdletar. IotHub, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c93f3-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c93f3-143">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="c93f3-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="c93f3-144">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="c93f3-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="c93f3-145">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="c93f3-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="c93f3-146">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="c93f3-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="c93f3-147">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c93f3-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="c93f3-148">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingStorageContainerProperties []</span><span class="sxs-lookup"><span data-stu-id="c93f3-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="c93f3-149">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingCustomEndpoint []</span><span class="sxs-lookup"><span data-stu-id="c93f3-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="c93f3-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c93f3-150">NOTES</span></span>

## <span data-ttu-id="c93f3-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c93f3-151">RELATED LINKS</span></span>