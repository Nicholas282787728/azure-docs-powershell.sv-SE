---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: ecc91bb19b3d5d40f8c5aa3e4f25812a9999e45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576283"
---
# <span data-ttu-id="abb3f-101">Remove-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="abb3f-101">Remove-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="abb3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="abb3f-103">Ta bort en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="abb3f-103">Delete an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abb3f-104">SYNTAX</span></span>

### <span data-ttu-id="abb3f-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="abb3f-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abb3f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="abb3f-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abb3f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="abb3f-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abb3f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abb3f-108">DESCRIPTION</span></span>
<span data-ttu-id="abb3f-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="abb3f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="abb3f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abb3f-110">EXAMPLES</span></span>

### <span data-ttu-id="abb3f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="abb3f-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="abb3f-112">Ta bort en Azure IoT Hub-enhet ' myiotdps '.</span><span class="sxs-lookup"><span data-stu-id="abb3f-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="abb3f-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="abb3f-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzureRmIotDps
```

<span data-ttu-id="abb3f-114">Ta bort en Azure IoT Hub-enhet ' myiotdps ' med pipelinen.</span><span class="sxs-lookup"><span data-stu-id="abb3f-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="abb3f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abb3f-115">PARAMETERS</span></span>

### <span data-ttu-id="abb3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb3f-116">-DefaultProfile</span></span>
<span data-ttu-id="abb3f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="abb3f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abb3f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abb3f-118">-InputObject</span></span>
<span data-ttu-id="abb3f-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="abb3f-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="abb3f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="abb3f-120">-Name</span></span>
<span data-ttu-id="abb3f-121">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="abb3f-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="abb3f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abb3f-122">-PassThru</span></span>
<span data-ttu-id="abb3f-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="abb3f-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="abb3f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb3f-124">-ResourceGroupName</span></span>
<span data-ttu-id="abb3f-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="abb3f-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="abb3f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abb3f-126">-ResourceId</span></span>
<span data-ttu-id="abb3f-127">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="abb3f-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="abb3f-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abb3f-128">-Confirm</span></span>
<span data-ttu-id="abb3f-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abb3f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abb3f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abb3f-130">-WhatIf</span></span>
<span data-ttu-id="abb3f-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abb3f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abb3f-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abb3f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abb3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb3f-133">CommonParameters</span></span>
<span data-ttu-id="abb3f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb3f-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb3f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb3f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abb3f-136">INPUTS</span></span>

### <span data-ttu-id="abb3f-137">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="abb3f-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="abb3f-138">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="abb3f-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="abb3f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="abb3f-139">System.String</span></span>

## <span data-ttu-id="abb3f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abb3f-140">OUTPUTS</span></span>

### <span data-ttu-id="abb3f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="abb3f-141">System.Boolean</span></span>

## <span data-ttu-id="abb3f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abb3f-142">NOTES</span></span>

## <span data-ttu-id="abb3f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abb3f-143">RELATED LINKS</span></span>
