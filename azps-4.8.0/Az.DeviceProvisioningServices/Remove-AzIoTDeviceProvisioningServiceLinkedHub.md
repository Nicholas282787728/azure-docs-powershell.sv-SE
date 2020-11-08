---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261338"
---
# <span data-ttu-id="a2773-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="a2773-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="a2773-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2773-102">SYNOPSIS</span></span>
<span data-ttu-id="a2773-103">Ta bort en länkad IoT Hub i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="a2773-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="a2773-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2773-104">SYNTAX</span></span>

### <span data-ttu-id="a2773-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a2773-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2773-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2773-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2773-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a2773-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2773-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2773-108">DESCRIPTION</span></span>
<span data-ttu-id="a2773-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="a2773-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="a2773-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2773-110">EXAMPLES</span></span>

### <span data-ttu-id="a2773-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a2773-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="a2773-112">Ta bort länkad IoT Hub "myiothub" i en Azure IoT Hub-enhets etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="a2773-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="a2773-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a2773-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="a2773-114">Ta bort länkad IoT Hub "myiothub" i en konfigurations tjänst för Azure IoT Hub-enheter med pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2773-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="a2773-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2773-115">PARAMETERS</span></span>

### <span data-ttu-id="a2773-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2773-116">-DefaultProfile</span></span>
<span data-ttu-id="a2773-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2773-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2773-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2773-118">-InputObject</span></span>
<span data-ttu-id="a2773-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="a2773-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a2773-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="a2773-120">-LinkedHubName</span></span>
<span data-ttu-id="a2773-121">Värd namnet på länkad IoT Hub</span><span class="sxs-lookup"><span data-stu-id="a2773-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="a2773-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="a2773-122">-Name</span></span>
<span data-ttu-id="a2773-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="a2773-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a2773-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2773-124">-PassThru</span></span>
<span data-ttu-id="a2773-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a2773-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a2773-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2773-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2773-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="a2773-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a2773-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2773-128">-ResourceId</span></span>
<span data-ttu-id="a2773-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="a2773-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a2773-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2773-130">-Confirm</span></span>
<span data-ttu-id="a2773-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2773-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2773-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2773-132">-WhatIf</span></span>
<span data-ttu-id="a2773-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a2773-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2773-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a2773-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2773-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2773-135">CommonParameters</span></span>
<span data-ttu-id="a2773-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2773-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2773-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2773-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2773-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2773-138">INPUTS</span></span>

### <span data-ttu-id="a2773-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="a2773-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="a2773-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a2773-140">System.String</span></span>

## <span data-ttu-id="a2773-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2773-141">OUTPUTS</span></span>

### <span data-ttu-id="a2773-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2773-142">System.Boolean</span></span>

## <span data-ttu-id="a2773-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2773-143">NOTES</span></span>

## <span data-ttu-id="a2773-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2773-144">RELATED LINKS</span></span>
