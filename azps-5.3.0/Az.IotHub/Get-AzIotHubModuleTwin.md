---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526011"
---
# <span data-ttu-id="bd0d4-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="bd0d4-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="bd0d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0d4-103">Får en IoT-modul till en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="bd0d4-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="bd0d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd0d4-104">SYNTAX</span></span>

### <span data-ttu-id="bd0d4-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bd0d4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd0d4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bd0d4-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd0d4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bd0d4-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd0d4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd0d4-108">DESCRIPTION</span></span>
<span data-ttu-id="bd0d4-109">Får en IoT-modul till en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="bd0d4-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="bd0d4-110">Mer https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins information finns i.</span><span class="sxs-lookup"><span data-stu-id="bd0d4-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="bd0d4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd0d4-111">EXAMPLES</span></span>

### <span data-ttu-id="bd0d4-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bd0d4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="bd0d4-113">Returnerar enhets modulens dubbla objekt.</span><span class="sxs-lookup"><span data-stu-id="bd0d4-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="bd0d4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd0d4-114">PARAMETERS</span></span>

### <span data-ttu-id="bd0d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0d4-115">-DefaultProfile</span></span>
<span data-ttu-id="bd0d4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd0d4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd0d4-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="bd0d4-117">-DeviceId</span></span>
<span data-ttu-id="bd0d4-118">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="bd0d4-118">Target Device Id.</span></span>

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

### <span data-ttu-id="bd0d4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd0d4-119">-InputObject</span></span>
<span data-ttu-id="bd0d4-120">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="bd0d4-120">IotHub object</span></span>

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

### <span data-ttu-id="bd0d4-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="bd0d4-121">-IotHubName</span></span>
<span data-ttu-id="bd0d4-122">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="bd0d4-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bd0d4-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="bd0d4-123">-ModuleId</span></span>
<span data-ttu-id="bd0d4-124">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="bd0d4-124">Target Module Id.</span></span>

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

### <span data-ttu-id="bd0d4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd0d4-125">-ResourceGroupName</span></span>
<span data-ttu-id="bd0d4-126">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="bd0d4-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bd0d4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd0d4-127">-ResourceId</span></span>
<span data-ttu-id="bd0d4-128">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="bd0d4-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bd0d4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0d4-129">CommonParameters</span></span>
<span data-ttu-id="bd0d4-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd0d4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd0d4-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd0d4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0d4-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd0d4-132">INPUTS</span></span>

### <span data-ttu-id="bd0d4-133">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bd0d4-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bd0d4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bd0d4-134">System.String</span></span>

## <span data-ttu-id="bd0d4-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd0d4-135">OUTPUTS</span></span>

### <span data-ttu-id="bd0d4-136">Microsoft. Azure. commands. Management. IotHub. Models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="bd0d4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="bd0d4-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd0d4-137">NOTES</span></span>

## <span data-ttu-id="bd0d4-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd0d4-138">RELATED LINKS</span></span>
