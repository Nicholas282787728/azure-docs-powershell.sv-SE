---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 173e84e3587a6844896791ef38a185db522d4e4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411776"
---
# <span data-ttu-id="cd479-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="cd479-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="cd479-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd479-102">SYNOPSIS</span></span>
<span data-ttu-id="cd479-103">Testa vägar i IoT Hub</span><span class="sxs-lookup"><span data-stu-id="cd479-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="cd479-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd479-104">SYNTAX</span></span>

### <span data-ttu-id="cd479-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cd479-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd479-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="cd479-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd479-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="cd479-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd479-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="cd479-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd479-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="cd479-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd479-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="cd479-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd479-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="cd479-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd479-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd479-112">DESCRIPTION</span></span>
<span data-ttu-id="cd479-113">Testa ett specifikt flöde.</span><span class="sxs-lookup"><span data-stu-id="cd479-113">Test a specific route.</span></span>

## <span data-ttu-id="cd479-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd479-114">EXAMPLES</span></span>

### <span data-ttu-id="cd479-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd479-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="cd479-116">Testa alla vägar med source "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="cd479-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="cd479-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cd479-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="cd479-118">Testa ett specifikt flöde.</span><span class="sxs-lookup"><span data-stu-id="cd479-118">Test a specific route.</span></span>

### <span data-ttu-id="cd479-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="cd479-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="cd479-120">Testa ett specifikt flöde och Visa orsaken till felet.</span><span class="sxs-lookup"><span data-stu-id="cd479-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="cd479-121">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="cd479-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="cd479-122">Testa en specifik väg med AppProperty och SystemProperty.</span><span class="sxs-lookup"><span data-stu-id="cd479-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="cd479-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd479-123">PARAMETERS</span></span>

### <span data-ttu-id="cd479-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="cd479-124">-AppProperty</span></span>
<span data-ttu-id="cd479-125">App-egenskaper för Route-meddelandet</span><span class="sxs-lookup"><span data-stu-id="cd479-125">App properties of the route message</span></span>

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

### <span data-ttu-id="cd479-126">-Body</span><span class="sxs-lookup"><span data-stu-id="cd479-126">-Body</span></span>
<span data-ttu-id="cd479-127">Meddelande text</span><span class="sxs-lookup"><span data-stu-id="cd479-127">Body of the route message</span></span>

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

### <span data-ttu-id="cd479-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd479-128">-DefaultProfile</span></span>
<span data-ttu-id="cd479-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd479-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd479-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd479-130">-InputObject</span></span>
<span data-ttu-id="cd479-131">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="cd479-131">IotHub Object</span></span>

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

### <span data-ttu-id="cd479-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd479-132">-Name</span></span>
<span data-ttu-id="cd479-133">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="cd479-133">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cd479-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd479-134">-ResourceGroupName</span></span>
<span data-ttu-id="cd479-135">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="cd479-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cd479-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd479-136">-ResourceId</span></span>
<span data-ttu-id="cd479-137">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="cd479-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cd479-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="cd479-138">-RouteName</span></span>
<span data-ttu-id="cd479-139">Vägens namn</span><span class="sxs-lookup"><span data-stu-id="cd479-139">Name of the Route</span></span>

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

### <span data-ttu-id="cd479-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="cd479-140">-ShowError</span></span>
<span data-ttu-id="cd479-141">Visa detaljerat fel</span><span class="sxs-lookup"><span data-stu-id="cd479-141">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="cd479-142">-Källa</span><span class="sxs-lookup"><span data-stu-id="cd479-142">-Source</span></span>
<span data-ttu-id="cd479-143">Källa för flödet</span><span class="sxs-lookup"><span data-stu-id="cd479-143">Source of the route</span></span>

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

### <span data-ttu-id="cd479-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="cd479-144">-SystemProperty</span></span>
<span data-ttu-id="cd479-145">System egenskaper för väg meddelandet</span><span class="sxs-lookup"><span data-stu-id="cd479-145">System properties of the route message</span></span>

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

### <span data-ttu-id="cd479-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd479-146">CommonParameters</span></span>
<span data-ttu-id="cd479-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd479-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd479-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd479-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd479-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd479-149">INPUTS</span></span>

### <span data-ttu-id="cd479-150">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cd479-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cd479-151">System. String</span><span class="sxs-lookup"><span data-stu-id="cd479-151">System.String</span></span>

## <span data-ttu-id="cd479-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd479-152">OUTPUTS</span></span>

### <span data-ttu-id="cd479-153">Microsoft. Azure. commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="cd479-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="cd479-154">Microsoft. Azure. commands. Management. IotHub. Models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="cd479-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="cd479-155">Microsoft. Azure. commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="cd479-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="cd479-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd479-156">NOTES</span></span>

## <span data-ttu-id="cd479-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd479-157">RELATED LINKS</span></span>
