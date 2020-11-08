---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: cc8d2ec0602213bdbfd50ac89e5199952cea424c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263208"
---
# <span data-ttu-id="a3dc4-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="a3dc4-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="a3dc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="a3dc4-103">Uppdatera en länkad IoT-hubb i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="a3dc4-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="a3dc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3dc4-104">SYNTAX</span></span>

### <span data-ttu-id="a3dc4-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a3dc4-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3dc4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a3dc4-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3dc4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a3dc4-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3dc4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3dc4-108">DESCRIPTION</span></span>
<span data-ttu-id="a3dc4-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="a3dc4-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="a3dc4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3dc4-110">EXAMPLES</span></span>

### <span data-ttu-id="a3dc4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a3dc4-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="a3dc4-112">Uppdatera länkad IoT Hub "myiothub.azure-devices.net" i en Azure IoT Hub-enhets etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="a3dc4-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="a3dc4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3dc4-113">PARAMETERS</span></span>

### <span data-ttu-id="a3dc4-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="a3dc4-114">-AllocationWeight</span></span>
<span data-ttu-id="a3dc4-115">Tilldelnings vikt för IoT Hub</span><span class="sxs-lookup"><span data-stu-id="a3dc4-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="a3dc4-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="a3dc4-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="a3dc4-117">Tillämpa en allokeringsregel på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="a3dc4-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="a3dc4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3dc4-118">-DefaultProfile</span></span>
<span data-ttu-id="a3dc4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3dc4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3dc4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3dc4-120">-InputObject</span></span>
<span data-ttu-id="a3dc4-121">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="a3dc4-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3dc4-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="a3dc4-122">-LinkedHubName</span></span>
<span data-ttu-id="a3dc4-123">Värd namnet på länkad IoT Hub</span><span class="sxs-lookup"><span data-stu-id="a3dc4-123">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3dc4-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3dc4-124">-Name</span></span>
<span data-ttu-id="a3dc4-125">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="a3dc4-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a3dc4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3dc4-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3dc4-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="a3dc4-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a3dc4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3dc4-128">-ResourceId</span></span>
<span data-ttu-id="a3dc4-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="a3dc4-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a3dc4-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3dc4-130">-Confirm</span></span>
<span data-ttu-id="a3dc4-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3dc4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3dc4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3dc4-132">-WhatIf</span></span>
<span data-ttu-id="a3dc4-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3dc4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3dc4-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3dc4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3dc4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3dc4-135">CommonParameters</span></span>
<span data-ttu-id="a3dc4-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3dc4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3dc4-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3dc4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3dc4-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3dc4-138">INPUTS</span></span>

### <span data-ttu-id="a3dc4-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="a3dc4-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="a3dc4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a3dc4-140">System.String</span></span>

## <span data-ttu-id="a3dc4-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3dc4-141">OUTPUTS</span></span>

### <span data-ttu-id="a3dc4-142">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="a3dc4-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="a3dc4-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3dc4-143">NOTES</span></span>

## <span data-ttu-id="a3dc4-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3dc4-144">RELATED LINKS</span></span>
