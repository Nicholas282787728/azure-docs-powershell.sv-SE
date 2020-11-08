---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 1cc1bb46909260bd23cfa3f72e675251a011072d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916449"
---
# <span data-ttu-id="edb41-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="edb41-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="edb41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="edb41-102">SYNOPSIS</span></span>
<span data-ttu-id="edb41-103">Få information om vägen i IoT Hub</span><span class="sxs-lookup"><span data-stu-id="edb41-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="edb41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="edb41-104">SYNTAX</span></span>

### <span data-ttu-id="edb41-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="edb41-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edb41-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="edb41-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="edb41-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="edb41-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edb41-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="edb41-108">DESCRIPTION</span></span>
<span data-ttu-id="edb41-109">Få information om vägen. Du kan hämta alla vägar från en IoT Hub, Hämta vägar till en typ av slut punkt eller hämta vägar till en viss slut punkt.</span><span class="sxs-lookup"><span data-stu-id="edb41-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="edb41-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="edb41-110">EXAMPLES</span></span>

### <span data-ttu-id="edb41-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="edb41-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="edb41-112">Få vägen från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="edb41-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="edb41-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="edb41-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="edb41-114">Få väg information från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="edb41-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="edb41-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="edb41-115">PARAMETERS</span></span>

### <span data-ttu-id="edb41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb41-116">-DefaultProfile</span></span>
<span data-ttu-id="edb41-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="edb41-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edb41-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edb41-118">-InputObject</span></span>
<span data-ttu-id="edb41-119">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="edb41-119">IotHub Object</span></span>

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

### <span data-ttu-id="edb41-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="edb41-120">-Name</span></span>
<span data-ttu-id="edb41-121">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="edb41-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="edb41-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb41-122">-ResourceGroupName</span></span>
<span data-ttu-id="edb41-123">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="edb41-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="edb41-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edb41-124">-ResourceId</span></span>
<span data-ttu-id="edb41-125">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="edb41-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="edb41-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="edb41-126">-RouteName</span></span>
<span data-ttu-id="edb41-127">Vägens namn</span><span class="sxs-lookup"><span data-stu-id="edb41-127">Name of the Route</span></span>

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

### <span data-ttu-id="edb41-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb41-128">CommonParameters</span></span>
<span data-ttu-id="edb41-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb41-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb41-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edb41-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb41-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="edb41-131">INPUTS</span></span>

### <span data-ttu-id="edb41-132">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="edb41-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="edb41-133">System. String</span><span class="sxs-lookup"><span data-stu-id="edb41-133">System.String</span></span>

## <span data-ttu-id="edb41-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="edb41-134">OUTPUTS</span></span>

### <span data-ttu-id="edb41-135">Microsoft. Azure. commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="edb41-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="edb41-136">Microsoft. Azure. commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="edb41-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="edb41-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="edb41-137">NOTES</span></span>

## <span data-ttu-id="edb41-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="edb41-138">RELATED LINKS</span></span>