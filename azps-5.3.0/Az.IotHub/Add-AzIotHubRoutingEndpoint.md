---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526036"
---
# <span data-ttu-id="8cee9-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cee9-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="8cee9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8cee9-102">SYNOPSIS</span></span>
<span data-ttu-id="8cee9-103">Lägga till en slut punkt till IoT Hub</span><span class="sxs-lookup"><span data-stu-id="8cee9-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="8cee9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8cee9-104">SYNTAX</span></span>

### <span data-ttu-id="8cee9-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8cee9-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cee9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8cee9-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cee9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8cee9-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cee9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8cee9-108">DESCRIPTION</span></span>
<span data-ttu-id="8cee9-109">Lägg till en ny slut punkt i IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="8cee9-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="8cee9-110">Information om vilka slut punkter som stöds finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="8cee9-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="8cee9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8cee9-111">EXAMPLES</span></span>

### <span data-ttu-id="8cee9-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8cee9-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="8cee9-113">Lägg till en ny slut punkt "E2" av typen EventHub till en "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="8cee9-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="8cee9-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8cee9-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container -Encoding json

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : json
```

<span data-ttu-id="8cee9-115">Lägg till en ny slut punkt "S1" av typen AzureStorageContainer till en "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="8cee9-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="8cee9-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8cee9-116">PARAMETERS</span></span>

### <span data-ttu-id="8cee9-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="8cee9-117">-ConnectionString</span></span>
<span data-ttu-id="8cee9-118">Anslutnings sträng för cirkulations slut punkt</span><span class="sxs-lookup"><span data-stu-id="8cee9-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="8cee9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cee9-119">-DefaultProfile</span></span>
<span data-ttu-id="8cee9-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8cee9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cee9-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8cee9-121">-EndpointName</span></span>
<span data-ttu-id="8cee9-122">Namnet på cirkulations slut punkten</span><span class="sxs-lookup"><span data-stu-id="8cee9-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="8cee9-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8cee9-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="8cee9-124">Resurs grupp för slut punkts resursen</span><span class="sxs-lookup"><span data-stu-id="8cee9-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="8cee9-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8cee9-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="8cee9-126">SubscriptionId för slut punkts resursen</span><span class="sxs-lookup"><span data-stu-id="8cee9-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="8cee9-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="8cee9-127">-EndpointType</span></span>
<span data-ttu-id="8cee9-128">Typ av cirkulations slut punkt</span><span class="sxs-lookup"><span data-stu-id="8cee9-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cee9-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8cee9-129">-ContainerName</span></span>
<span data-ttu-id="8cee9-130">Namn på lagrings behållaren</span><span class="sxs-lookup"><span data-stu-id="8cee9-130">Name of the storage container</span></span>

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

### <span data-ttu-id="8cee9-131">-Kodning</span><span class="sxs-lookup"><span data-stu-id="8cee9-131">-Encoding</span></span>
<span data-ttu-id="8cee9-132">Välj det format som du vill cirkulera data i.</span><span class="sxs-lookup"><span data-stu-id="8cee9-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="8cee9-133">Du kan välja JSON eller AVRO.</span><span class="sxs-lookup"><span data-stu-id="8cee9-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="8cee9-134">Standardinställningen är AVRO.</span><span class="sxs-lookup"><span data-stu-id="8cee9-134">The default is set to AVRO.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:
Accepted values: JSON, AVRO

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cee9-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cee9-135">-InputObject</span></span>
<span data-ttu-id="8cee9-136">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="8cee9-136">IotHub Object</span></span>

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

### <span data-ttu-id="8cee9-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="8cee9-137">-Name</span></span>
<span data-ttu-id="8cee9-138">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="8cee9-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8cee9-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cee9-139">-ResourceGroupName</span></span>
<span data-ttu-id="8cee9-140">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="8cee9-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8cee9-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cee9-141">-ResourceId</span></span>
<span data-ttu-id="8cee9-142">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="8cee9-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8cee9-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8cee9-143">-Confirm</span></span>
<span data-ttu-id="8cee9-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8cee9-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cee9-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cee9-145">-WhatIf</span></span>
<span data-ttu-id="8cee9-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8cee9-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cee9-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8cee9-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cee9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cee9-148">CommonParameters</span></span>
<span data-ttu-id="8cee9-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cee9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cee9-150">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cee9-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cee9-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8cee9-151">INPUTS</span></span>

### <span data-ttu-id="8cee9-152">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8cee9-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8cee9-153">System. String</span><span class="sxs-lookup"><span data-stu-id="8cee9-153">System.String</span></span>

## <span data-ttu-id="8cee9-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8cee9-154">OUTPUTS</span></span>

### <span data-ttu-id="8cee9-155">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cee9-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="8cee9-156">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cee9-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="8cee9-157">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cee9-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="8cee9-158">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cee9-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="8cee9-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8cee9-159">NOTES</span></span>

## <span data-ttu-id="8cee9-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8cee9-160">RELATED LINKS</span></span>
