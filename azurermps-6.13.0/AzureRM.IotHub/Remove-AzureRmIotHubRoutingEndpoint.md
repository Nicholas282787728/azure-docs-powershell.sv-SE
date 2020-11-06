---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 6caad4faec3dd292f902689757b82b90091afcde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584232"
---
# <span data-ttu-id="f36d0-101">Remove-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="f36d0-101">Remove-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="f36d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f36d0-102">SYNOPSIS</span></span>
<span data-ttu-id="f36d0-103">Ta bort en slut punkt för IoT Hub</span><span class="sxs-lookup"><span data-stu-id="f36d0-103">Delete an endpoint for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f36d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f36d0-104">SYNTAX</span></span>

### <span data-ttu-id="f36d0-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f36d0-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f36d0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f36d0-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f36d0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f36d0-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f36d0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f36d0-108">DESCRIPTION</span></span>
<span data-ttu-id="f36d0-109">Ta bort en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="f36d0-109">Delete an endpoint.</span></span> <span data-ttu-id="f36d0-110">Kom ihåg att ta bort alla vägar som använder den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="f36d0-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="f36d0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f36d0-111">EXAMPLES</span></span>

### <span data-ttu-id="f36d0-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f36d0-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="f36d0-113">Ta bort slut punkten "E2" från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="f36d0-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="f36d0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f36d0-114">PARAMETERS</span></span>

### <span data-ttu-id="f36d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36d0-115">-DefaultProfile</span></span>
<span data-ttu-id="f36d0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f36d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f36d0-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f36d0-117">-EndpointName</span></span>
<span data-ttu-id="f36d0-118">Namnet på cirkulations slut punkten</span><span class="sxs-lookup"><span data-stu-id="f36d0-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="f36d0-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="f36d0-119">-EndpointType</span></span>
<span data-ttu-id="f36d0-120">Typ av cirkulations slut punkt</span><span class="sxs-lookup"><span data-stu-id="f36d0-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36d0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f36d0-121">-InputObject</span></span>
<span data-ttu-id="f36d0-122">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="f36d0-122">IotHub Object</span></span>

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

### <span data-ttu-id="f36d0-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="f36d0-123">-Name</span></span>
<span data-ttu-id="f36d0-124">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="f36d0-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f36d0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f36d0-125">-PassThru</span></span>
<span data-ttu-id="f36d0-126">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="f36d0-126">Allows to return the boolean object.</span></span> <span data-ttu-id="f36d0-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f36d0-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36d0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36d0-128">-ResourceGroupName</span></span>
<span data-ttu-id="f36d0-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="f36d0-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f36d0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f36d0-130">-ResourceId</span></span>
<span data-ttu-id="f36d0-131">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="f36d0-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f36d0-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f36d0-132">-Confirm</span></span>
<span data-ttu-id="f36d0-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f36d0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f36d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f36d0-134">-WhatIf</span></span>
<span data-ttu-id="f36d0-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f36d0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f36d0-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f36d0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f36d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36d0-137">CommonParameters</span></span>
<span data-ttu-id="f36d0-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f36d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f36d0-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f36d0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36d0-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f36d0-140">INPUTS</span></span>

### <span data-ttu-id="f36d0-141">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f36d0-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="f36d0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f36d0-142">System.String</span></span>

## <span data-ttu-id="f36d0-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f36d0-143">OUTPUTS</span></span>

### <span data-ttu-id="f36d0-144">Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="f36d0-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="f36d0-145">System. Collections. Generic. list `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. kommandon. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure. commands. IotHub, version = 3.1.3.0, Culture = neutralt, PublicKeyToken = null]] Microsoft. Azure. commands Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint system. Collections. Generic. list `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` 1 [Microsoft. Azure. commands. Management. IotHub. Models. PSRoutingStorageContainerProperties, Microsoft. Azure. commands. IotHub, version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] system. Collections. genered. list ' 1 [[Microsoft. Azure. commands Management. IotHub. Models. PSRoutingCustomEndpoint, Microsoft. Azure</span><span class="sxs-lookup"><span data-stu-id="f36d0-145">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f36d0-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f36d0-146">NOTES</span></span>

## <span data-ttu-id="f36d0-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f36d0-147">RELATED LINKS</span></span>
