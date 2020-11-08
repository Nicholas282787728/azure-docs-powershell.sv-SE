---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: eb9d6a7b847c360861fd13bb285bc6f09bb70fbc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259618"
---
# <span data-ttu-id="3e816-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="3e816-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="3e816-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e816-102">SYNOPSIS</span></span>
<span data-ttu-id="3e816-103">Testa vägar i IoT Hub</span><span class="sxs-lookup"><span data-stu-id="3e816-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="3e816-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e816-104">SYNTAX</span></span>

### <span data-ttu-id="3e816-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3e816-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e816-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="3e816-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e816-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="3e816-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e816-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="3e816-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e816-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="3e816-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e816-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="3e816-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e816-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="3e816-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e816-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e816-112">DESCRIPTION</span></span>
<span data-ttu-id="3e816-113">Testa ett specifikt flöde.</span><span class="sxs-lookup"><span data-stu-id="3e816-113">Test a specific route.</span></span>

## <span data-ttu-id="3e816-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e816-114">EXAMPLES</span></span>

### <span data-ttu-id="3e816-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e816-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="3e816-116">Testa alla vägar med source "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="3e816-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="3e816-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3e816-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="3e816-118">Testa ett specifikt flöde.</span><span class="sxs-lookup"><span data-stu-id="3e816-118">Test a specific route.</span></span>

### <span data-ttu-id="3e816-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3e816-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="3e816-120">Testa ett specifikt flöde och Visa orsaken till felet.</span><span class="sxs-lookup"><span data-stu-id="3e816-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="3e816-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e816-121">PARAMETERS</span></span>

### <span data-ttu-id="3e816-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="3e816-122">-AppProperty</span></span>
<span data-ttu-id="3e816-123">App-egenskaper för Route-meddelandet</span><span class="sxs-lookup"><span data-stu-id="3e816-123">App properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e816-124">-Body</span><span class="sxs-lookup"><span data-stu-id="3e816-124">-Body</span></span>
<span data-ttu-id="3e816-125">Meddelande text</span><span class="sxs-lookup"><span data-stu-id="3e816-125">Body of the route message</span></span>

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

### <span data-ttu-id="3e816-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e816-126">-DefaultProfile</span></span>
<span data-ttu-id="3e816-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e816-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e816-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e816-128">-InputObject</span></span>
<span data-ttu-id="3e816-129">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="3e816-129">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectTestRouteSet, InputObjectTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e816-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e816-130">-Name</span></span>
<span data-ttu-id="3e816-131">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="3e816-131">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e816-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e816-132">-ResourceGroupName</span></span>
<span data-ttu-id="3e816-133">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="3e816-133">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e816-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e816-134">-ResourceId</span></span>
<span data-ttu-id="3e816-135">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="3e816-135">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdTestRouteSet, ResourceIdTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e816-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="3e816-136">-RouteName</span></span>
<span data-ttu-id="3e816-137">Vägens namn</span><span class="sxs-lookup"><span data-stu-id="3e816-137">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e816-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="3e816-138">-ShowError</span></span>
<span data-ttu-id="3e816-139">Visa detaljerat fel</span><span class="sxs-lookup"><span data-stu-id="3e816-139">Show detailed error, if exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e816-140">-Källa</span><span class="sxs-lookup"><span data-stu-id="3e816-140">-Source</span></span>
<span data-ttu-id="3e816-141">Källa för flödet</span><span class="sxs-lookup"><span data-stu-id="3e816-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e816-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="3e816-142">-SystemProperty</span></span>
<span data-ttu-id="3e816-143">System egenskaper för väg meddelandet</span><span class="sxs-lookup"><span data-stu-id="3e816-143">System properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e816-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e816-144">CommonParameters</span></span>
<span data-ttu-id="3e816-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e816-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e816-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e816-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e816-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e816-147">INPUTS</span></span>

### <span data-ttu-id="3e816-148">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3e816-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3e816-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3e816-149">System.String</span></span>

## <span data-ttu-id="3e816-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e816-150">OUTPUTS</span></span>

### <span data-ttu-id="3e816-151">Microsoft. Azure. commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="3e816-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="3e816-152">Microsoft. Azure. commands. Management. IotHub. Models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="3e816-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="3e816-153">Microsoft. Azure. commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="3e816-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="3e816-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e816-154">NOTES</span></span>

## <span data-ttu-id="3e816-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e816-155">RELATED LINKS</span></span>
