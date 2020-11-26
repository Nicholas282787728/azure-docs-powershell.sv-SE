---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263242"
---
# <span data-ttu-id="1e6c5-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="1e6c5-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="1e6c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6c5-103">Lista alla eller Visa information om länkade IoT-hubbar i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="1e6c5-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="1e6c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e6c5-104">SYNTAX</span></span>

### <span data-ttu-id="1e6c5-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1e6c5-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e6c5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1e6c5-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e6c5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1e6c5-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e6c5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e6c5-108">DESCRIPTION</span></span>
<span data-ttu-id="1e6c5-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="1e6c5-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="1e6c5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e6c5-110">EXAMPLES</span></span>

### <span data-ttu-id="1e6c5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1e6c5-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="1e6c5-112">Lista alla länkade IoT-nav i "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="1e6c5-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="1e6c5-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1e6c5-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="1e6c5-114">Visa information om länkad IoT Hub "myiothub1" i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="1e6c5-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="1e6c5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e6c5-115">PARAMETERS</span></span>

### <span data-ttu-id="1e6c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c5-116">-DefaultProfile</span></span>
<span data-ttu-id="1e6c5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e6c5-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="1e6c5-118">-DpsObject</span></span>
<span data-ttu-id="1e6c5-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="1e6c5-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1e6c5-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="1e6c5-120">-LinkedHubName</span></span>
<span data-ttu-id="1e6c5-121">Värd namnet på länkad IoT Hub</span><span class="sxs-lookup"><span data-stu-id="1e6c5-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="1e6c5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e6c5-122">-Name</span></span>
<span data-ttu-id="1e6c5-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="1e6c5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1e6c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e6c5-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="1e6c5-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1e6c5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e6c5-126">-ResourceId</span></span>
<span data-ttu-id="1e6c5-127">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="1e6c5-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1e6c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6c5-128">CommonParameters</span></span>
<span data-ttu-id="1e6c5-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e6c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6c5-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e6c5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6c5-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e6c5-131">INPUTS</span></span>

### <span data-ttu-id="1e6c5-132">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1e6c5-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1e6c5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1e6c5-133">System.String</span></span>

## <span data-ttu-id="1e6c5-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e6c5-134">OUTPUTS</span></span>

### <span data-ttu-id="1e6c5-135">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="1e6c5-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="1e6c5-136">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="1e6c5-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="1e6c5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e6c5-137">NOTES</span></span>

## <span data-ttu-id="1e6c5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e6c5-138">RELATED LINKS</span></span>