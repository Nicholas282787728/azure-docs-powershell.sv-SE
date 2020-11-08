---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: cc8d2ec0602213bdbfd50ac89e5199952cea424c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090068"
---
# <span data-ttu-id="52387-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="52387-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="52387-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52387-102">SYNOPSIS</span></span>
<span data-ttu-id="52387-103">Uppdatera en länkad IoT-hubb i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="52387-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="52387-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52387-104">SYNTAX</span></span>

### <span data-ttu-id="52387-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="52387-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52387-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="52387-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52387-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="52387-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52387-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52387-108">DESCRIPTION</span></span>
<span data-ttu-id="52387-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="52387-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="52387-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52387-110">EXAMPLES</span></span>

### <span data-ttu-id="52387-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52387-111">Example 1</span></span>
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

<span data-ttu-id="52387-112">Uppdatera länkad IoT Hub "myiothub.azure-devices.net" i en Azure IoT Hub-enhets etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="52387-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="52387-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52387-113">PARAMETERS</span></span>

### <span data-ttu-id="52387-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="52387-114">-AllocationWeight</span></span>
<span data-ttu-id="52387-115">Tilldelnings vikt för IoT Hub</span><span class="sxs-lookup"><span data-stu-id="52387-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="52387-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="52387-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="52387-117">Tillämpa en allokeringsregel på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="52387-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="52387-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52387-118">-DefaultProfile</span></span>
<span data-ttu-id="52387-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52387-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52387-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52387-120">-InputObject</span></span>
<span data-ttu-id="52387-121">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="52387-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="52387-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="52387-122">-LinkedHubName</span></span>
<span data-ttu-id="52387-123">Värd namnet på länkad IoT Hub</span><span class="sxs-lookup"><span data-stu-id="52387-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="52387-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="52387-124">-Name</span></span>
<span data-ttu-id="52387-125">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="52387-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="52387-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52387-126">-ResourceGroupName</span></span>
<span data-ttu-id="52387-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="52387-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="52387-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52387-128">-ResourceId</span></span>
<span data-ttu-id="52387-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="52387-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="52387-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52387-130">-Confirm</span></span>
<span data-ttu-id="52387-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52387-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52387-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52387-132">-WhatIf</span></span>
<span data-ttu-id="52387-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52387-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52387-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52387-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52387-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52387-135">CommonParameters</span></span>
<span data-ttu-id="52387-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52387-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52387-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52387-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52387-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52387-138">INPUTS</span></span>

### <span data-ttu-id="52387-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="52387-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="52387-140">System. String</span><span class="sxs-lookup"><span data-stu-id="52387-140">System.String</span></span>

## <span data-ttu-id="52387-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52387-141">OUTPUTS</span></span>

### <span data-ttu-id="52387-142">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="52387-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="52387-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52387-143">NOTES</span></span>

## <span data-ttu-id="52387-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52387-144">RELATED LINKS</span></span>
