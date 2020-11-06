---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: 9665b0ae486c12aec350db572aee6fc4f718ed43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576285"
---
# <span data-ttu-id="3280e-101">New-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="3280e-101">New-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="3280e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3280e-102">SYNOPSIS</span></span>
<span data-ttu-id="3280e-103">Skapa en Azure IoT Hub-enhet för etablerings enheter.</span><span class="sxs-lookup"><span data-stu-id="3280e-103">Create an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3280e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3280e-104">SYNTAX</span></span>

```
New-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3280e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3280e-105">DESCRIPTION</span></span>
<span data-ttu-id="3280e-106">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="3280e-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3280e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3280e-107">EXAMPLES</span></span>

### <span data-ttu-id="3280e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3280e-108">Example 1</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
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

<span data-ttu-id="3280e-109">Skapa en Azure IoT Hub-enhet med standard pris nivå S1 i området i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3280e-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="3280e-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3280e-110">Example 2</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

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
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="3280e-111">Skapa en Azure IoT Hub-enhet med en standard pris nivå S1 i området ' östable '.</span><span class="sxs-lookup"><span data-stu-id="3280e-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="3280e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3280e-112">PARAMETERS</span></span>

### <span data-ttu-id="3280e-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3280e-113">-AllocationPolicy</span></span>
<span data-ttu-id="3280e-114">Tjänst tilldelnings princip för IoT-etablering</span><span class="sxs-lookup"><span data-stu-id="3280e-114">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3280e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3280e-115">-DefaultProfile</span></span>
<span data-ttu-id="3280e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3280e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3280e-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="3280e-117">-Location</span></span>
<span data-ttu-id="3280e-118">Plats</span><span class="sxs-lookup"><span data-stu-id="3280e-118">Location</span></span>

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

### <span data-ttu-id="3280e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="3280e-119">-Name</span></span>
<span data-ttu-id="3280e-120">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="3280e-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3280e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3280e-121">-ResourceGroupName</span></span>
<span data-ttu-id="3280e-122">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="3280e-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3280e-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3280e-123">-SkuName</span></span>
<span data-ttu-id="3280e-124">N</span><span class="sxs-lookup"><span data-stu-id="3280e-124">Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3280e-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3280e-125">-Confirm</span></span>
<span data-ttu-id="3280e-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3280e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3280e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3280e-127">-WhatIf</span></span>
<span data-ttu-id="3280e-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3280e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3280e-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3280e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3280e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3280e-130">CommonParameters</span></span>
<span data-ttu-id="3280e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3280e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3280e-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3280e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3280e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3280e-133">INPUTS</span></span>

### <span data-ttu-id="3280e-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="3280e-134">None</span></span>

## <span data-ttu-id="3280e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3280e-135">OUTPUTS</span></span>

### <span data-ttu-id="3280e-136">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3280e-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="3280e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3280e-137">NOTES</span></span>

## <span data-ttu-id="3280e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3280e-138">RELATED LINKS</span></span>
