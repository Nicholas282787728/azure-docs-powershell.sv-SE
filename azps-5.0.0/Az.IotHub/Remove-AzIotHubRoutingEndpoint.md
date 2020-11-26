---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: f162bf5f22ab435dd0d340bfd96db1ae616ccc96
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270963"
---
# <span data-ttu-id="ab63a-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab63a-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="ab63a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab63a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab63a-103">Ta bort en slut punkt för IoT Hub</span><span class="sxs-lookup"><span data-stu-id="ab63a-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="ab63a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab63a-104">SYNTAX</span></span>

### <span data-ttu-id="ab63a-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ab63a-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab63a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ab63a-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab63a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ab63a-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab63a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab63a-108">DESCRIPTION</span></span>
<span data-ttu-id="ab63a-109">Ta bort en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="ab63a-109">Delete an endpoint.</span></span> <span data-ttu-id="ab63a-110">Kom ihåg att ta bort alla vägar som använder den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="ab63a-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="ab63a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab63a-111">EXAMPLES</span></span>

### <span data-ttu-id="ab63a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ab63a-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="ab63a-113">Ta bort slut punkten "E2" från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="ab63a-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="ab63a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab63a-114">PARAMETERS</span></span>

### <span data-ttu-id="ab63a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab63a-115">-DefaultProfile</span></span>
<span data-ttu-id="ab63a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab63a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab63a-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ab63a-117">-EndpointName</span></span>
<span data-ttu-id="ab63a-118">Namnet på cirkulations slut punkten</span><span class="sxs-lookup"><span data-stu-id="ab63a-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="ab63a-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="ab63a-119">-EndpointType</span></span>
<span data-ttu-id="ab63a-120">Typ av cirkulations slut punkt</span><span class="sxs-lookup"><span data-stu-id="ab63a-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="ab63a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab63a-121">-InputObject</span></span>
<span data-ttu-id="ab63a-122">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="ab63a-122">IotHub Object</span></span>

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

### <span data-ttu-id="ab63a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab63a-123">-Name</span></span>
<span data-ttu-id="ab63a-124">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="ab63a-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ab63a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab63a-125">-PassThru</span></span>
<span data-ttu-id="ab63a-126">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="ab63a-126">Allows to return the boolean object.</span></span> <span data-ttu-id="ab63a-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ab63a-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ab63a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab63a-128">-ResourceGroupName</span></span>
<span data-ttu-id="ab63a-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="ab63a-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ab63a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab63a-130">-ResourceId</span></span>
<span data-ttu-id="ab63a-131">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="ab63a-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ab63a-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab63a-132">-Confirm</span></span>
<span data-ttu-id="ab63a-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab63a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab63a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab63a-134">-WhatIf</span></span>
<span data-ttu-id="ab63a-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ab63a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab63a-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ab63a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab63a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab63a-137">CommonParameters</span></span>
<span data-ttu-id="ab63a-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab63a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab63a-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab63a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab63a-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab63a-140">INPUTS</span></span>

### <span data-ttu-id="ab63a-141">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ab63a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ab63a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ab63a-142">System.String</span></span>

## <span data-ttu-id="ab63a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab63a-143">OUTPUTS</span></span>

### <span data-ttu-id="ab63a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab63a-144">System.Boolean</span></span>

## <span data-ttu-id="ab63a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab63a-145">NOTES</span></span>

## <span data-ttu-id="ab63a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab63a-146">RELATED LINKS</span></span>