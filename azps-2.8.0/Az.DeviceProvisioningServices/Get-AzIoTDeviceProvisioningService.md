---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 264978e5cf66436667434c265a7a3ae0c5a31a5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744317"
---
# <span data-ttu-id="aa85f-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="aa85f-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="aa85f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa85f-102">SYNOPSIS</span></span>
<span data-ttu-id="aa85f-103">Lista alla eller Visa information om konfigurations tjänsterna för Azure IoT Hub-enheter.</span><span class="sxs-lookup"><span data-stu-id="aa85f-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="aa85f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa85f-104">SYNTAX</span></span>

### <span data-ttu-id="aa85f-105">ListIotDpsByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="aa85f-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa85f-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="aa85f-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa85f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa85f-107">DESCRIPTION</span></span>
<span data-ttu-id="aa85f-108">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="aa85f-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="aa85f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa85f-109">EXAMPLES</span></span>

### <span data-ttu-id="aa85f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="aa85f-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="aa85f-111">Lista alla tjänste etablerings tjänster för Azure IoT Hub-enheter i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="aa85f-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="aa85f-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="aa85f-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="aa85f-113">Lista alla konfigurations tjänster för Azure IoT Hub-enheter i resurs gruppen ' myresourcegroup '.</span><span class="sxs-lookup"><span data-stu-id="aa85f-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="aa85f-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="aa85f-114">Example 3</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="aa85f-115">Visa information om en Azure IoT Hub-enhets etablerings tjänst ' myiotdps '.</span><span class="sxs-lookup"><span data-stu-id="aa85f-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="aa85f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa85f-116">PARAMETERS</span></span>

### <span data-ttu-id="aa85f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa85f-117">-DefaultProfile</span></span>
<span data-ttu-id="aa85f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aa85f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa85f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="aa85f-119">-Name</span></span>
<span data-ttu-id="aa85f-120">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="aa85f-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa85f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa85f-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa85f-122">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="aa85f-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotDpsByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa85f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa85f-123">CommonParameters</span></span>
<span data-ttu-id="aa85f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa85f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa85f-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa85f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa85f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa85f-126">INPUTS</span></span>

### <span data-ttu-id="aa85f-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="aa85f-127">None</span></span>

## <span data-ttu-id="aa85f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa85f-128">OUTPUTS</span></span>

### <span data-ttu-id="aa85f-129">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="aa85f-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="aa85f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa85f-130">NOTES</span></span>

## <span data-ttu-id="aa85f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa85f-131">RELATED LINKS</span></span>