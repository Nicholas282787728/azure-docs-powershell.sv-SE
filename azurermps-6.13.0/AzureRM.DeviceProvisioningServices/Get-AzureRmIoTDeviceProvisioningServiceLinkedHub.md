---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: bae363b984f148ff55f34eaa04b1ba85eaad4449
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572775"
---
# <span data-ttu-id="fba6b-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="fba6b-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="fba6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fba6b-102">SYNOPSIS</span></span>
<span data-ttu-id="fba6b-103">Lista alla eller Visa information om länkade IoT-hubbar i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="fba6b-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fba6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fba6b-104">SYNTAX</span></span>

### <span data-ttu-id="fba6b-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fba6b-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fba6b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fba6b-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fba6b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fba6b-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fba6b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fba6b-108">DESCRIPTION</span></span>
<span data-ttu-id="fba6b-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="fba6b-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="fba6b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fba6b-110">EXAMPLES</span></span>

### <span data-ttu-id="fba6b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fba6b-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="fba6b-112">Lista alla länkade IoT-nav i "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="fba6b-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="fba6b-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fba6b-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="fba6b-114">Visa information om länkad IoT Hub "myiothub1" i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="fba6b-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="fba6b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fba6b-115">PARAMETERS</span></span>

### <span data-ttu-id="fba6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba6b-116">-DefaultProfile</span></span>
<span data-ttu-id="fba6b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fba6b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fba6b-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="fba6b-118">-DpsObject</span></span>
<span data-ttu-id="fba6b-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="fba6b-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fba6b-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="fba6b-120">-LinkedHubName</span></span>
<span data-ttu-id="fba6b-121">Värd namnet på länkad IoT Hub</span><span class="sxs-lookup"><span data-stu-id="fba6b-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="fba6b-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="fba6b-122">-Name</span></span>
<span data-ttu-id="fba6b-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="fba6b-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fba6b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba6b-124">-ResourceGroupName</span></span>
<span data-ttu-id="fba6b-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="fba6b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fba6b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fba6b-126">-ResourceId</span></span>
<span data-ttu-id="fba6b-127">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="fba6b-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="fba6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba6b-128">CommonParameters</span></span>
<span data-ttu-id="fba6b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba6b-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fba6b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba6b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fba6b-131">INPUTS</span></span>

### <span data-ttu-id="fba6b-132">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="fba6b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="fba6b-133">Parametrar: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fba6b-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="fba6b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fba6b-134">System.String</span></span>

## <span data-ttu-id="fba6b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fba6b-135">OUTPUTS</span></span>

### <span data-ttu-id="fba6b-136">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="fba6b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="fba6b-137">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="fba6b-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="fba6b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fba6b-138">NOTES</span></span>

## <span data-ttu-id="fba6b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fba6b-139">RELATED LINKS</span></span>
