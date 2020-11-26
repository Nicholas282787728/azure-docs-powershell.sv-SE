---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259977"
---
# <span data-ttu-id="410d0-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="410d0-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="410d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="410d0-102">SYNOPSIS</span></span>
<span data-ttu-id="410d0-103">Ta bort en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="410d0-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="410d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="410d0-104">SYNTAX</span></span>

### <span data-ttu-id="410d0-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="410d0-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="410d0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="410d0-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="410d0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="410d0-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="410d0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="410d0-108">DESCRIPTION</span></span>
<span data-ttu-id="410d0-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="410d0-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="410d0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="410d0-110">EXAMPLES</span></span>

### <span data-ttu-id="410d0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="410d0-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="410d0-112">Ta bort en Azure IoT Hub-enhet ' myiotdps '.</span><span class="sxs-lookup"><span data-stu-id="410d0-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="410d0-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="410d0-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="410d0-114">Ta bort en Azure IoT Hub-enhet ' myiotdps ' med pipelinen.</span><span class="sxs-lookup"><span data-stu-id="410d0-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="410d0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="410d0-115">PARAMETERS</span></span>

### <span data-ttu-id="410d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="410d0-116">-DefaultProfile</span></span>
<span data-ttu-id="410d0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="410d0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="410d0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="410d0-118">-InputObject</span></span>
<span data-ttu-id="410d0-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="410d0-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="410d0-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="410d0-120">-Name</span></span>
<span data-ttu-id="410d0-121">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="410d0-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="410d0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="410d0-122">-PassThru</span></span>
<span data-ttu-id="410d0-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="410d0-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="410d0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="410d0-124">-ResourceGroupName</span></span>
<span data-ttu-id="410d0-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="410d0-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="410d0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="410d0-126">-ResourceId</span></span>
<span data-ttu-id="410d0-127">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="410d0-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="410d0-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="410d0-128">-Confirm</span></span>
<span data-ttu-id="410d0-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="410d0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="410d0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="410d0-130">-WhatIf</span></span>
<span data-ttu-id="410d0-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="410d0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="410d0-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="410d0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="410d0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410d0-133">CommonParameters</span></span>
<span data-ttu-id="410d0-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="410d0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410d0-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="410d0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410d0-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="410d0-136">INPUTS</span></span>

### <span data-ttu-id="410d0-137">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="410d0-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="410d0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="410d0-138">System.String</span></span>

## <span data-ttu-id="410d0-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="410d0-139">OUTPUTS</span></span>

### <span data-ttu-id="410d0-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="410d0-140">System.Boolean</span></span>

## <span data-ttu-id="410d0-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="410d0-141">NOTES</span></span>

## <span data-ttu-id="410d0-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="410d0-142">RELATED LINKS</span></span>