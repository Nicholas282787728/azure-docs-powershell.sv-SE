---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 3102cafabecb5df8daea15a40eb179405c6c0ea8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089644"
---
# <span data-ttu-id="0890c-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="0890c-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="0890c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0890c-102">SYNOPSIS</span></span>
<span data-ttu-id="0890c-103">Skapa en Azure IoT Hub-enhet för etablerings enheter.</span><span class="sxs-lookup"><span data-stu-id="0890c-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0890c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0890c-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0890c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0890c-105">DESCRIPTION</span></span>
<span data-ttu-id="0890c-106">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0890c-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0890c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0890c-107">EXAMPLES</span></span>

### <span data-ttu-id="0890c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0890c-108">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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

<span data-ttu-id="0890c-109">Skapa en Azure IoT Hub-enhet med standard pris nivå S1 i området i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0890c-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="0890c-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0890c-110">Example 2</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

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

<span data-ttu-id="0890c-111">Skapa en Azure IoT Hub-enhet med en standard pris nivå S1 i området ' östable '.</span><span class="sxs-lookup"><span data-stu-id="0890c-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="0890c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0890c-112">PARAMETERS</span></span>

### <span data-ttu-id="0890c-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0890c-113">-AllocationPolicy</span></span>
<span data-ttu-id="0890c-114">Tjänst tilldelnings princip för IoT-etablering</span><span class="sxs-lookup"><span data-stu-id="0890c-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="0890c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0890c-115">-DefaultProfile</span></span>
<span data-ttu-id="0890c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0890c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0890c-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="0890c-117">-Location</span></span>
<span data-ttu-id="0890c-118">Plats</span><span class="sxs-lookup"><span data-stu-id="0890c-118">Location</span></span>

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

### <span data-ttu-id="0890c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0890c-119">-Name</span></span>
<span data-ttu-id="0890c-120">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="0890c-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0890c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0890c-121">-ResourceGroupName</span></span>
<span data-ttu-id="0890c-122">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="0890c-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0890c-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0890c-123">-SkuName</span></span>
<span data-ttu-id="0890c-124">N</span><span class="sxs-lookup"><span data-stu-id="0890c-124">Sku</span></span>

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

### <span data-ttu-id="0890c-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0890c-125">-Confirm</span></span>
<span data-ttu-id="0890c-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0890c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0890c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0890c-127">-WhatIf</span></span>
<span data-ttu-id="0890c-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0890c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0890c-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0890c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0890c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0890c-130">CommonParameters</span></span>
<span data-ttu-id="0890c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0890c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0890c-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0890c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0890c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0890c-133">INPUTS</span></span>

### <span data-ttu-id="0890c-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="0890c-134">None</span></span>

## <span data-ttu-id="0890c-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0890c-135">OUTPUTS</span></span>

### <span data-ttu-id="0890c-136">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0890c-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="0890c-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0890c-137">NOTES</span></span>

## <span data-ttu-id="0890c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0890c-138">RELATED LINKS</span></span>
