---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: d251d3159111437cd06880a49069aee7aca6d80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576263"
---
# <span data-ttu-id="3622c-101">Add-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="3622c-101">Add-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="3622c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3622c-102">SYNOPSIS</span></span>
<span data-ttu-id="3622c-103">Lägga till en slut punkt till IoT Hub</span><span class="sxs-lookup"><span data-stu-id="3622c-103">Add an endpoint to your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3622c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3622c-104">SYNTAX</span></span>

### <span data-ttu-id="3622c-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3622c-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3622c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3622c-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3622c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3622c-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3622c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3622c-108">DESCRIPTION</span></span>
<span data-ttu-id="3622c-109">Lägg till en ny slut punkt i IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3622c-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="3622c-110">Information om vilka slut punkter som stöds finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="3622c-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="3622c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3622c-111">EXAMPLES</span></span>

### <span data-ttu-id="3622c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3622c-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="3622c-113">Lägg till en ny slut punkt "E2" av typen EventHub till en "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3622c-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="3622c-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3622c-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : avro
```

<span data-ttu-id="3622c-115">Lägg till en ny slut punkt "S1" av typen AzureStorageContainer till en "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3622c-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="3622c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3622c-116">PARAMETERS</span></span>

### <span data-ttu-id="3622c-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="3622c-117">-ConnectionString</span></span>
<span data-ttu-id="3622c-118">Anslutnings sträng för cirkulations slut punkt</span><span class="sxs-lookup"><span data-stu-id="3622c-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3622c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3622c-119">-DefaultProfile</span></span>
<span data-ttu-id="3622c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3622c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3622c-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3622c-121">-EndpointName</span></span>
<span data-ttu-id="3622c-122">Namnet på cirkulations slut punkten</span><span class="sxs-lookup"><span data-stu-id="3622c-122">Name of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3622c-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3622c-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="3622c-124">Resurs grupp för slut punktens resurs</span><span class="sxs-lookup"><span data-stu-id="3622c-124">Resource group of the Endpoint resoure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3622c-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3622c-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="3622c-126">SubscriptionId för slut punkts resursen</span><span class="sxs-lookup"><span data-stu-id="3622c-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3622c-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="3622c-127">-EndpointType</span></span>
<span data-ttu-id="3622c-128">Typ av cirkulations slut punkt</span><span class="sxs-lookup"><span data-stu-id="3622c-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3622c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3622c-129">-InputObject</span></span>
<span data-ttu-id="3622c-130">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="3622c-130">IotHub Object</span></span>

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

### <span data-ttu-id="3622c-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="3622c-131">-Name</span></span>
<span data-ttu-id="3622c-132">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="3622c-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3622c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3622c-133">-ResourceGroupName</span></span>
<span data-ttu-id="3622c-134">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="3622c-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3622c-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3622c-135">-ResourceId</span></span>
<span data-ttu-id="3622c-136">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="3622c-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3622c-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3622c-137">-Confirm</span></span>
<span data-ttu-id="3622c-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3622c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3622c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3622c-139">-WhatIf</span></span>
<span data-ttu-id="3622c-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3622c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3622c-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3622c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3622c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3622c-142">CommonParameters</span></span>
<span data-ttu-id="3622c-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3622c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3622c-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3622c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3622c-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3622c-145">INPUTS</span></span>

### <span data-ttu-id="3622c-146">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3622c-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="3622c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3622c-147">System.String</span></span>

## <span data-ttu-id="3622c-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3622c-148">OUTPUTS</span></span>

### <span data-ttu-id="3622c-149">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="3622c-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="3622c-150">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3622c-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="3622c-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3622c-151">NOTES</span></span>

## <span data-ttu-id="3622c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3622c-152">RELATED LINKS</span></span>
