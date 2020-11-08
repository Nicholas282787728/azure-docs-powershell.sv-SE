---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 30bcf61f309a400270e9cca378fce6d1149cf66a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090083"
---
# <span data-ttu-id="96124-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="96124-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="96124-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96124-102">SYNOPSIS</span></span>
<span data-ttu-id="96124-103">Länkad IoT Hub till en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="96124-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="96124-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96124-104">SYNTAX</span></span>

### <span data-ttu-id="96124-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="96124-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96124-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="96124-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96124-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="96124-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96124-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96124-108">DESCRIPTION</span></span>
<span data-ttu-id="96124-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="96124-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="96124-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96124-110">EXAMPLES</span></span>

### <span data-ttu-id="96124-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="96124-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="96124-112">Länkad IoT Hub till en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="96124-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="96124-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="96124-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="96124-114">Länkad IoT Hub till en Azure IoT Hub-enhet med AllocationWeight och ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="96124-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="96124-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96124-115">PARAMETERS</span></span>

### <span data-ttu-id="96124-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="96124-116">-AllocationWeight</span></span>
<span data-ttu-id="96124-117">Tilldelnings vikt för IoT Hub</span><span class="sxs-lookup"><span data-stu-id="96124-117">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96124-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="96124-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="96124-119">Ett booleskt värde som anger om tilldelnings policy ska tillämpas på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="96124-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96124-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96124-120">-DefaultProfile</span></span>
<span data-ttu-id="96124-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96124-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96124-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="96124-122">-DpsObject</span></span>
<span data-ttu-id="96124-123">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="96124-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="96124-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="96124-124">-IotHubConnectionString</span></span>
<span data-ttu-id="96124-125">Anslutnings sträng för IoT Hub-resursen.</span><span class="sxs-lookup"><span data-stu-id="96124-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="96124-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="96124-126">-IotHubLocation</span></span>
<span data-ttu-id="96124-127">Plats för IoT Hub</span><span class="sxs-lookup"><span data-stu-id="96124-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96124-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="96124-128">-Name</span></span>
<span data-ttu-id="96124-129">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="96124-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="96124-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96124-130">-ResourceGroupName</span></span>
<span data-ttu-id="96124-131">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="96124-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="96124-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96124-132">-ResourceId</span></span>
<span data-ttu-id="96124-133">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="96124-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="96124-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96124-134">-Confirm</span></span>
<span data-ttu-id="96124-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96124-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96124-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96124-136">-WhatIf</span></span>
<span data-ttu-id="96124-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96124-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96124-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96124-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96124-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96124-139">CommonParameters</span></span>
<span data-ttu-id="96124-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96124-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96124-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96124-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96124-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96124-142">INPUTS</span></span>

### <span data-ttu-id="96124-143">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="96124-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="96124-144">System. String</span><span class="sxs-lookup"><span data-stu-id="96124-144">System.String</span></span>

## <span data-ttu-id="96124-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96124-145">OUTPUTS</span></span>

### <span data-ttu-id="96124-146">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="96124-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="96124-147">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="96124-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="96124-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96124-148">NOTES</span></span>

## <span data-ttu-id="96124-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96124-149">RELATED LINKS</span></span>
