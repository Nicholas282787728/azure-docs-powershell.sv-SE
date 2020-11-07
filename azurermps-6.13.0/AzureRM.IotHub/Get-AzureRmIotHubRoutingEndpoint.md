---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 2aa49f01b16547987604a7ee978018596c7d9647
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757621"
---
# <span data-ttu-id="13c3d-101">Get-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="13c3d-101">Get-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="13c3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="13c3d-103">Få information om alla slut punkter för din IoT Hub</span><span class="sxs-lookup"><span data-stu-id="13c3d-103">Get information on all the endpoints for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13c3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13c3d-104">SYNTAX</span></span>

### <span data-ttu-id="13c3d-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="13c3d-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String>
 [-EndpointType <PSEndpointType>] [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13c3d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="13c3d-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13c3d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="13c3d-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13c3d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13c3d-108">DESCRIPTION</span></span>
<span data-ttu-id="13c3d-109">Få information om slut punkten.</span><span class="sxs-lookup"><span data-stu-id="13c3d-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="13c3d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13c3d-110">EXAMPLES</span></span>

### <span data-ttu-id="13c3d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="13c3d-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="13c3d-112">Hämta alla slut punkter från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="13c3d-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="13c3d-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="13c3d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="13c3d-114">Få alla slut punkter av typen EventHub från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="13c3d-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="13c3d-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="13c3d-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="13c3d-116">Få alla slut punkter av typen EventHub från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="13c3d-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="13c3d-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="13c3d-117">Example 4</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="13c3d-118">Hämta en slut punkts information från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="13c3d-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="13c3d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13c3d-119">PARAMETERS</span></span>

### <span data-ttu-id="13c3d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c3d-120">-DefaultProfile</span></span>
<span data-ttu-id="13c3d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13c3d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13c3d-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="13c3d-122">-EndpointName</span></span>
<span data-ttu-id="13c3d-123">Namnet på cirkulations slut punkten</span><span class="sxs-lookup"><span data-stu-id="13c3d-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="13c3d-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="13c3d-124">-EndpointType</span></span>
<span data-ttu-id="13c3d-125">Typ av cirkulations slut punkt</span><span class="sxs-lookup"><span data-stu-id="13c3d-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="13c3d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13c3d-126">-InputObject</span></span>
<span data-ttu-id="13c3d-127">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="13c3d-127">IotHub Object</span></span>

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

### <span data-ttu-id="13c3d-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="13c3d-128">-Name</span></span>
<span data-ttu-id="13c3d-129">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="13c3d-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="13c3d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13c3d-130">-ResourceGroupName</span></span>
<span data-ttu-id="13c3d-131">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="13c3d-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="13c3d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13c3d-132">-ResourceId</span></span>
<span data-ttu-id="13c3d-133">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="13c3d-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="13c3d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c3d-134">CommonParameters</span></span>
<span data-ttu-id="13c3d-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13c3d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c3d-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13c3d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c3d-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13c3d-137">INPUTS</span></span>

### <span data-ttu-id="13c3d-138">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="13c3d-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="13c3d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="13c3d-139">System.String</span></span>

## <span data-ttu-id="13c3d-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13c3d-140">OUTPUTS</span></span>

### <span data-ttu-id="13c3d-141">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="13c3d-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="13c3d-142">System. Collections. Generic. list `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. kommandon. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure. commands. IotHub, version = 3.1.3.0, Culture = neutralt, PublicKeyToken = null]] Microsoft. Azure. commands Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint system. Collections. Generic. list `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` 1 [Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingStorageContainerProperties, Microsoft. Azure. commands. IotHub, version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] system. Collections. genered. list ' 1 [[Microsoft. Azure. commands Management. IotHub. Models. PSRoutingCustomEndpoint, Microsoft. Azure</span><span class="sxs-lookup"><span data-stu-id="13c3d-142">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="13c3d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13c3d-143">NOTES</span></span>

## <span data-ttu-id="13c3d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13c3d-144">RELATED LINKS</span></span>
