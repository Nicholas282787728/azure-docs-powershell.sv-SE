---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: f50c0955d56b42c341b6a1a6b64b1993ee66175e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757889"
---
# <span data-ttu-id="5e02f-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="5e02f-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="5e02f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e02f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e02f-103">Ta bort en länkad IoT Hub i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="5e02f-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e02f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e02f-104">SYNTAX</span></span>

### <span data-ttu-id="5e02f-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5e02f-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e02f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5e02f-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e02f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5e02f-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e02f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e02f-108">DESCRIPTION</span></span>
<span data-ttu-id="5e02f-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5e02f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5e02f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e02f-110">EXAMPLES</span></span>

### <span data-ttu-id="5e02f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5e02f-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="5e02f-112">Ta bort länkad IoT Hub "myiothub" i en Azure IoT Hub-enhets etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="5e02f-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="5e02f-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5e02f-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzureRmIoTDpsHub
```

<span data-ttu-id="5e02f-114">Ta bort länkad IoT Hub "myiothub" i en konfigurations tjänst för Azure IoT Hub-enheter med pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e02f-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="5e02f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e02f-115">PARAMETERS</span></span>

### <span data-ttu-id="5e02f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e02f-116">-DefaultProfile</span></span>
<span data-ttu-id="5e02f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e02f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e02f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e02f-118">-InputObject</span></span>
<span data-ttu-id="5e02f-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="5e02f-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5e02f-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="5e02f-120">-LinkedHubName</span></span>
<span data-ttu-id="5e02f-121">Värd namnet på länkad IoT Hub</span><span class="sxs-lookup"><span data-stu-id="5e02f-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="5e02f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e02f-122">-Name</span></span>
<span data-ttu-id="5e02f-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="5e02f-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5e02f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e02f-124">-PassThru</span></span>
<span data-ttu-id="5e02f-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5e02f-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5e02f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e02f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5e02f-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5e02f-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5e02f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e02f-128">-ResourceId</span></span>
<span data-ttu-id="5e02f-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="5e02f-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5e02f-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e02f-130">-Confirm</span></span>
<span data-ttu-id="5e02f-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e02f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e02f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e02f-132">-WhatIf</span></span>
<span data-ttu-id="5e02f-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e02f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e02f-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e02f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e02f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e02f-135">CommonParameters</span></span>
<span data-ttu-id="5e02f-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e02f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e02f-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e02f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e02f-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e02f-138">INPUTS</span></span>

### <span data-ttu-id="5e02f-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="5e02f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="5e02f-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5e02f-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5e02f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5e02f-141">System.String</span></span>

## <span data-ttu-id="5e02f-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e02f-142">OUTPUTS</span></span>

### <span data-ttu-id="5e02f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e02f-143">System.Boolean</span></span>

## <span data-ttu-id="5e02f-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e02f-144">NOTES</span></span>

## <span data-ttu-id="5e02f-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e02f-145">RELATED LINKS</span></span>
