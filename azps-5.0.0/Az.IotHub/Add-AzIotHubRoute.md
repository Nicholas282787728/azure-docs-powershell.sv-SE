---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: a84d432e5771b5f04a7d9f478cd8ef446e08620a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271003"
---
# <span data-ttu-id="3fb4a-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="3fb4a-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="3fb4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3fb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb4a-103">Skapa en väg i IoT Hub</span><span class="sxs-lookup"><span data-stu-id="3fb4a-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="3fb4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3fb4a-104">SYNTAX</span></span>

### <span data-ttu-id="3fb4a-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3fb4a-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fb4a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3fb4a-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fb4a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3fb4a-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3fb4a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3fb4a-108">DESCRIPTION</span></span>
<span data-ttu-id="3fb4a-109">Skapa en väg för att skicka specifik data källa och villkor till en önskad slut punkt.</span><span class="sxs-lookup"><span data-stu-id="3fb4a-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="3fb4a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3fb4a-110">EXAMPLES</span></span>

### <span data-ttu-id="3fb4a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3fb4a-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="3fb4a-112">Skapa en ny väg "R1".</span><span class="sxs-lookup"><span data-stu-id="3fb4a-112">Create a new route "R1".</span></span>

## <span data-ttu-id="3fb4a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3fb4a-113">PARAMETERS</span></span>

### <span data-ttu-id="3fb4a-114">-Villkor</span><span class="sxs-lookup"><span data-stu-id="3fb4a-114">-Condition</span></span>
<span data-ttu-id="3fb4a-115">Villkor som utvärderas för att tillämpa regeln för routning</span><span class="sxs-lookup"><span data-stu-id="3fb4a-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="3fb4a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fb4a-116">-DefaultProfile</span></span>
<span data-ttu-id="3fb4a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3fb4a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fb4a-118">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="3fb4a-118">-Enabled</span></span>
<span data-ttu-id="3fb4a-119">Aktivera väg</span><span class="sxs-lookup"><span data-stu-id="3fb4a-119">Enable route</span></span>

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

### <span data-ttu-id="3fb4a-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3fb4a-120">-EndpointName</span></span>
<span data-ttu-id="3fb4a-121">Namnet på cirkulations slut punkten</span><span class="sxs-lookup"><span data-stu-id="3fb4a-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="3fb4a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fb4a-122">-InputObject</span></span>
<span data-ttu-id="3fb4a-123">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="3fb4a-123">IotHub Object</span></span>

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

### <span data-ttu-id="3fb4a-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3fb4a-124">-Name</span></span>
<span data-ttu-id="3fb4a-125">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="3fb4a-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3fb4a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fb4a-126">-ResourceGroupName</span></span>
<span data-ttu-id="3fb4a-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="3fb4a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3fb4a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fb4a-128">-ResourceId</span></span>
<span data-ttu-id="3fb4a-129">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="3fb4a-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3fb4a-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="3fb4a-130">-RouteName</span></span>
<span data-ttu-id="3fb4a-131">Vägens namn</span><span class="sxs-lookup"><span data-stu-id="3fb4a-131">Name of the Route</span></span>

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

### <span data-ttu-id="3fb4a-132">-Källa</span><span class="sxs-lookup"><span data-stu-id="3fb4a-132">-Source</span></span>
<span data-ttu-id="3fb4a-133">Källa för flödet</span><span class="sxs-lookup"><span data-stu-id="3fb4a-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb4a-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3fb4a-134">-Confirm</span></span>
<span data-ttu-id="3fb4a-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3fb4a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fb4a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fb4a-136">-WhatIf</span></span>
<span data-ttu-id="3fb4a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3fb4a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fb4a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3fb4a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fb4a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb4a-139">CommonParameters</span></span>
<span data-ttu-id="3fb4a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fb4a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb4a-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fb4a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb4a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3fb4a-142">INPUTS</span></span>

### <span data-ttu-id="3fb4a-143">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3fb4a-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3fb4a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3fb4a-144">System.String</span></span>

## <span data-ttu-id="3fb4a-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3fb4a-145">OUTPUTS</span></span>

### <span data-ttu-id="3fb4a-146">Microsoft. Azure. commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="3fb4a-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="3fb4a-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3fb4a-147">NOTES</span></span>

## <span data-ttu-id="3fb4a-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3fb4a-148">RELATED LINKS</span></span>