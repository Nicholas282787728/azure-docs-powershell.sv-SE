---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: eb9d6a7b847c360861fd13bb285bc6f09bb70fbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319955"
---
# <span data-ttu-id="16955-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="16955-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="16955-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16955-102">SYNOPSIS</span></span>
<span data-ttu-id="16955-103">Testa vägar i IoT Hub</span><span class="sxs-lookup"><span data-stu-id="16955-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="16955-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16955-104">SYNTAX</span></span>

### <span data-ttu-id="16955-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="16955-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16955-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="16955-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16955-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="16955-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16955-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="16955-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16955-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="16955-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16955-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="16955-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16955-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="16955-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16955-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16955-112">DESCRIPTION</span></span>
<span data-ttu-id="16955-113">Testa ett specifikt flöde.</span><span class="sxs-lookup"><span data-stu-id="16955-113">Test a specific route.</span></span>

## <span data-ttu-id="16955-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16955-114">EXAMPLES</span></span>

### <span data-ttu-id="16955-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="16955-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="16955-116">Testa alla vägar med source "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="16955-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="16955-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="16955-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="16955-118">Testa ett specifikt flöde.</span><span class="sxs-lookup"><span data-stu-id="16955-118">Test a specific route.</span></span>

### <span data-ttu-id="16955-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="16955-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="16955-120">Testa ett specifikt flöde och Visa orsaken till felet.</span><span class="sxs-lookup"><span data-stu-id="16955-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="16955-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16955-121">PARAMETERS</span></span>

### <span data-ttu-id="16955-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="16955-122">-AppProperty</span></span>
<span data-ttu-id="16955-123">App-egenskaper för Route-meddelandet</span><span class="sxs-lookup"><span data-stu-id="16955-123">App properties of the route message</span></span>

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

### <span data-ttu-id="16955-124">-Body</span><span class="sxs-lookup"><span data-stu-id="16955-124">-Body</span></span>
<span data-ttu-id="16955-125">Meddelande text</span><span class="sxs-lookup"><span data-stu-id="16955-125">Body of the route message</span></span>

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

### <span data-ttu-id="16955-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16955-126">-DefaultProfile</span></span>
<span data-ttu-id="16955-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16955-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16955-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16955-128">-InputObject</span></span>
<span data-ttu-id="16955-129">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="16955-129">IotHub Object</span></span>

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

### <span data-ttu-id="16955-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="16955-130">-Name</span></span>
<span data-ttu-id="16955-131">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="16955-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="16955-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16955-132">-ResourceGroupName</span></span>
<span data-ttu-id="16955-133">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="16955-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="16955-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16955-134">-ResourceId</span></span>
<span data-ttu-id="16955-135">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="16955-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="16955-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="16955-136">-RouteName</span></span>
<span data-ttu-id="16955-137">Vägens namn</span><span class="sxs-lookup"><span data-stu-id="16955-137">Name of the Route</span></span>

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

### <span data-ttu-id="16955-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="16955-138">-ShowError</span></span>
<span data-ttu-id="16955-139">Visa detaljerat fel</span><span class="sxs-lookup"><span data-stu-id="16955-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="16955-140">-Källa</span><span class="sxs-lookup"><span data-stu-id="16955-140">-Source</span></span>
<span data-ttu-id="16955-141">Källa för flödet</span><span class="sxs-lookup"><span data-stu-id="16955-141">Source of the route</span></span>

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

### <span data-ttu-id="16955-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="16955-142">-SystemProperty</span></span>
<span data-ttu-id="16955-143">System egenskaper för väg meddelandet</span><span class="sxs-lookup"><span data-stu-id="16955-143">System properties of the route message</span></span>

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

### <span data-ttu-id="16955-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16955-144">CommonParameters</span></span>
<span data-ttu-id="16955-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16955-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16955-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16955-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16955-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16955-147">INPUTS</span></span>

### <span data-ttu-id="16955-148">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="16955-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="16955-149">System. String</span><span class="sxs-lookup"><span data-stu-id="16955-149">System.String</span></span>

## <span data-ttu-id="16955-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16955-150">OUTPUTS</span></span>

### <span data-ttu-id="16955-151">Microsoft. Azure. commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="16955-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="16955-152">Microsoft. Azure. commands. Management. IotHub. Models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="16955-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="16955-153">Microsoft. Azure. commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="16955-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="16955-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16955-154">NOTES</span></span>

## <span data-ttu-id="16955-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16955-155">RELATED LINKS</span></span>
