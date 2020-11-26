---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259978"
---
# <span data-ttu-id="fefd0-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="fefd0-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="fefd0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fefd0-102">SYNOPSIS</span></span>
<span data-ttu-id="fefd0-103">Lista alla eller Visa information om länkade IoT-hubbar i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="fefd0-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="fefd0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fefd0-104">SYNTAX</span></span>

### <span data-ttu-id="fefd0-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fefd0-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fefd0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fefd0-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fefd0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fefd0-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fefd0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fefd0-108">DESCRIPTION</span></span>
<span data-ttu-id="fefd0-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="fefd0-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="fefd0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fefd0-110">EXAMPLES</span></span>

### <span data-ttu-id="fefd0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fefd0-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="fefd0-112">Lista alla länkade IoT-nav i "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="fefd0-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="fefd0-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fefd0-113">Example 2</span></span>
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

<span data-ttu-id="fefd0-114">Visa information om länkad IoT Hub "myiothub1" i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="fefd0-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="fefd0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fefd0-115">PARAMETERS</span></span>

### <span data-ttu-id="fefd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fefd0-116">-DefaultProfile</span></span>
<span data-ttu-id="fefd0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fefd0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fefd0-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="fefd0-118">-DpsObject</span></span>
<span data-ttu-id="fefd0-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="fefd0-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="fefd0-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="fefd0-120">-LinkedHubName</span></span>
<span data-ttu-id="fefd0-121">Värd namnet på länkad IoT Hub</span><span class="sxs-lookup"><span data-stu-id="fefd0-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="fefd0-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="fefd0-122">-Name</span></span>
<span data-ttu-id="fefd0-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="fefd0-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fefd0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fefd0-124">-ResourceGroupName</span></span>
<span data-ttu-id="fefd0-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="fefd0-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fefd0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fefd0-126">-ResourceId</span></span>
<span data-ttu-id="fefd0-127">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="fefd0-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="fefd0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fefd0-128">CommonParameters</span></span>
<span data-ttu-id="fefd0-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fefd0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fefd0-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fefd0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fefd0-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fefd0-131">INPUTS</span></span>

### <span data-ttu-id="fefd0-132">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="fefd0-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="fefd0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fefd0-133">System.String</span></span>

## <span data-ttu-id="fefd0-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fefd0-134">OUTPUTS</span></span>

### <span data-ttu-id="fefd0-135">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="fefd0-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="fefd0-136">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="fefd0-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="fefd0-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fefd0-137">NOTES</span></span>

## <span data-ttu-id="fefd0-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fefd0-138">RELATED LINKS</span></span>