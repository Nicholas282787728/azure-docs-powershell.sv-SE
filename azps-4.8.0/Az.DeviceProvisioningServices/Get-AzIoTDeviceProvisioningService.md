---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ab6dd43cff746d670fe05d66d983836433323728
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101531"
---
# <span data-ttu-id="23c98-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="23c98-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="23c98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23c98-102">SYNOPSIS</span></span>
<span data-ttu-id="23c98-103">Lista alla eller Visa information om konfigurations tjänsterna för Azure IoT Hub-enheter.</span><span class="sxs-lookup"><span data-stu-id="23c98-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="23c98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23c98-104">SYNTAX</span></span>

### <span data-ttu-id="23c98-105">ListIotDpsByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="23c98-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23c98-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="23c98-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23c98-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23c98-107">DESCRIPTION</span></span>
<span data-ttu-id="23c98-108">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="23c98-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="23c98-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23c98-109">EXAMPLES</span></span>

### <span data-ttu-id="23c98-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="23c98-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="23c98-111">Lista alla tjänste etablerings tjänster för Azure IoT Hub-enheter i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="23c98-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="23c98-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="23c98-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="23c98-113">Lista alla konfigurations tjänster för Azure IoT Hub-enheter i resurs gruppen ' myresourcegroup '.</span><span class="sxs-lookup"><span data-stu-id="23c98-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="23c98-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="23c98-114">Example 3</span></span>
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

<span data-ttu-id="23c98-115">Visa information om en Azure IoT Hub-enhets etablerings tjänst ' myiotdps '.</span><span class="sxs-lookup"><span data-stu-id="23c98-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="23c98-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23c98-116">PARAMETERS</span></span>

### <span data-ttu-id="23c98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c98-117">-DefaultProfile</span></span>
<span data-ttu-id="23c98-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="23c98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23c98-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="23c98-119">-Name</span></span>
<span data-ttu-id="23c98-120">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="23c98-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="23c98-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c98-121">-ResourceGroupName</span></span>
<span data-ttu-id="23c98-122">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="23c98-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="23c98-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c98-123">CommonParameters</span></span>
<span data-ttu-id="23c98-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23c98-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c98-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23c98-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c98-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23c98-126">INPUTS</span></span>

### <span data-ttu-id="23c98-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="23c98-127">None</span></span>

## <span data-ttu-id="23c98-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23c98-128">OUTPUTS</span></span>

### <span data-ttu-id="23c98-129">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="23c98-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="23c98-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23c98-130">NOTES</span></span>

## <span data-ttu-id="23c98-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23c98-131">RELATED LINKS</span></span>
