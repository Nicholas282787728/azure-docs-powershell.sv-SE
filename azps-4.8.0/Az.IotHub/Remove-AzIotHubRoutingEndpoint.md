---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: f162bf5f22ab435dd0d340bfd96db1ae616ccc96
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262237"
---
# <span data-ttu-id="decf5-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="decf5-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="decf5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="decf5-102">SYNOPSIS</span></span>
<span data-ttu-id="decf5-103">Ta bort en slut punkt för IoT Hub</span><span class="sxs-lookup"><span data-stu-id="decf5-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="decf5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="decf5-104">SYNTAX</span></span>

### <span data-ttu-id="decf5-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="decf5-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="decf5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="decf5-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="decf5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="decf5-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="decf5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="decf5-108">DESCRIPTION</span></span>
<span data-ttu-id="decf5-109">Ta bort en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="decf5-109">Delete an endpoint.</span></span> <span data-ttu-id="decf5-110">Kom ihåg att ta bort alla vägar som använder den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="decf5-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="decf5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="decf5-111">EXAMPLES</span></span>

### <span data-ttu-id="decf5-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="decf5-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="decf5-113">Ta bort slut punkten "E2" från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="decf5-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="decf5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="decf5-114">PARAMETERS</span></span>

### <span data-ttu-id="decf5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="decf5-115">-DefaultProfile</span></span>
<span data-ttu-id="decf5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="decf5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="decf5-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="decf5-117">-EndpointName</span></span>
<span data-ttu-id="decf5-118">Namnet på cirkulations slut punkten</span><span class="sxs-lookup"><span data-stu-id="decf5-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="decf5-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="decf5-119">-EndpointType</span></span>
<span data-ttu-id="decf5-120">Typ av cirkulations slut punkt</span><span class="sxs-lookup"><span data-stu-id="decf5-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="decf5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="decf5-121">-InputObject</span></span>
<span data-ttu-id="decf5-122">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="decf5-122">IotHub Object</span></span>

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

### <span data-ttu-id="decf5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="decf5-123">-Name</span></span>
<span data-ttu-id="decf5-124">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="decf5-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="decf5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="decf5-125">-PassThru</span></span>
<span data-ttu-id="decf5-126">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="decf5-126">Allows to return the boolean object.</span></span> <span data-ttu-id="decf5-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="decf5-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="decf5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="decf5-128">-ResourceGroupName</span></span>
<span data-ttu-id="decf5-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="decf5-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="decf5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="decf5-130">-ResourceId</span></span>
<span data-ttu-id="decf5-131">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="decf5-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="decf5-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="decf5-132">-Confirm</span></span>
<span data-ttu-id="decf5-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="decf5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="decf5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="decf5-134">-WhatIf</span></span>
<span data-ttu-id="decf5-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="decf5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="decf5-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="decf5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="decf5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decf5-137">CommonParameters</span></span>
<span data-ttu-id="decf5-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="decf5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decf5-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="decf5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decf5-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="decf5-140">INPUTS</span></span>

### <span data-ttu-id="decf5-141">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="decf5-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="decf5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="decf5-142">System.String</span></span>

## <span data-ttu-id="decf5-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="decf5-143">OUTPUTS</span></span>

### <span data-ttu-id="decf5-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="decf5-144">System.Boolean</span></span>

## <span data-ttu-id="decf5-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="decf5-145">NOTES</span></span>

## <span data-ttu-id="decf5-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="decf5-146">RELATED LINKS</span></span>
