---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: 97304a55c75291e03d92aae1436344819402fcff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743957"
---
# <span data-ttu-id="6b327-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="6b327-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="6b327-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b327-102">SYNOPSIS</span></span>
<span data-ttu-id="6b327-103">Uppdatera en väg i IoT Hub</span><span class="sxs-lookup"><span data-stu-id="6b327-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="6b327-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b327-104">SYNTAX</span></span>

### <span data-ttu-id="6b327-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6b327-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b327-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6b327-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b327-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6b327-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b327-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b327-108">DESCRIPTION</span></span>
<span data-ttu-id="6b327-109">Redigera ett flöde.</span><span class="sxs-lookup"><span data-stu-id="6b327-109">Edit a route.</span></span> <span data-ttu-id="6b327-110">Du kan uppdatera alla fält i en väg inklusive data källan, slut punkten, operationsföljden och även aktivera och inaktivera flödet.</span><span class="sxs-lookup"><span data-stu-id="6b327-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="6b327-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b327-111">EXAMPLES</span></span>

### <span data-ttu-id="6b327-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6b327-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="6b327-113">Uppdaterar routningsinformation.</span><span class="sxs-lookup"><span data-stu-id="6b327-113">Updating the route information.</span></span>

### <span data-ttu-id="6b327-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6b327-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="6b327-115">Uppdaterar routningsinformation.</span><span class="sxs-lookup"><span data-stu-id="6b327-115">Updating the route information.</span></span>

### <span data-ttu-id="6b327-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6b327-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="6b327-117">Uppdaterar routningsinformation.</span><span class="sxs-lookup"><span data-stu-id="6b327-117">Updating the route information.</span></span>

## <span data-ttu-id="6b327-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b327-118">PARAMETERS</span></span>

### <span data-ttu-id="6b327-119">-Villkor</span><span class="sxs-lookup"><span data-stu-id="6b327-119">-Condition</span></span>
<span data-ttu-id="6b327-120">Villkor som utvärderas för att tillämpa regeln för routning</span><span class="sxs-lookup"><span data-stu-id="6b327-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="6b327-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b327-121">-DefaultProfile</span></span>
<span data-ttu-id="6b327-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b327-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b327-123">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="6b327-123">-Enabled</span></span>
<span data-ttu-id="6b327-124">Aktivera väg</span><span class="sxs-lookup"><span data-stu-id="6b327-124">Enable route</span></span>

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

### <span data-ttu-id="6b327-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6b327-125">-EndpointName</span></span>
<span data-ttu-id="6b327-126">Namnet på cirkulations slut punkten</span><span class="sxs-lookup"><span data-stu-id="6b327-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="6b327-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b327-127">-InputObject</span></span>
<span data-ttu-id="6b327-128">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="6b327-128">IotHub Object</span></span>

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

### <span data-ttu-id="6b327-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="6b327-129">-Name</span></span>
<span data-ttu-id="6b327-130">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="6b327-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6b327-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b327-131">-ResourceGroupName</span></span>
<span data-ttu-id="6b327-132">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="6b327-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6b327-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b327-133">-ResourceId</span></span>
<span data-ttu-id="6b327-134">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="6b327-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6b327-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="6b327-135">-RouteName</span></span>
<span data-ttu-id="6b327-136">Vägens namn</span><span class="sxs-lookup"><span data-stu-id="6b327-136">Name of the Route</span></span>

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

### <span data-ttu-id="6b327-137">-Källa</span><span class="sxs-lookup"><span data-stu-id="6b327-137">-Source</span></span>
<span data-ttu-id="6b327-138">Källa för flödet</span><span class="sxs-lookup"><span data-stu-id="6b327-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b327-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b327-139">-Confirm</span></span>
<span data-ttu-id="6b327-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b327-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b327-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b327-141">-WhatIf</span></span>
<span data-ttu-id="6b327-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b327-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b327-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b327-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b327-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b327-144">CommonParameters</span></span>
<span data-ttu-id="6b327-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b327-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b327-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b327-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b327-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b327-147">INPUTS</span></span>

### <span data-ttu-id="6b327-148">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6b327-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6b327-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6b327-149">System.String</span></span>

## <span data-ttu-id="6b327-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b327-150">OUTPUTS</span></span>

### <span data-ttu-id="6b327-151">Microsoft. Azure. commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="6b327-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="6b327-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b327-152">NOTES</span></span>

## <span data-ttu-id="6b327-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b327-153">RELATED LINKS</span></span>
