---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 482acd4f82320bbc14c5bf95c113304a8720019b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398408"
---
# <span data-ttu-id="9c72f-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="9c72f-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="9c72f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c72f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c72f-103">Skapa en Azure IoT Hub-enhet för etablerings enheter.</span><span class="sxs-lookup"><span data-stu-id="9c72f-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9c72f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c72f-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c72f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c72f-105">DESCRIPTION</span></span>
<span data-ttu-id="9c72f-106">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="9c72f-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="9c72f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c72f-107">EXAMPLES</span></span>

### <span data-ttu-id="9c72f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9c72f-108">Example 1</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {[key1, value1]}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="9c72f-109">Skapa en Azure IoT Hub-enhet med en standard pris nivå S1 och-taggar, i området i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9c72f-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="9c72f-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9c72f-110">Example 2</span></span>
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

<span data-ttu-id="9c72f-111">Skapa en Azure IoT Hub-enhet med en standard pris nivå S1 i området ' östable '.</span><span class="sxs-lookup"><span data-stu-id="9c72f-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="9c72f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c72f-112">PARAMETERS</span></span>

### <span data-ttu-id="9c72f-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="9c72f-113">-AllocationPolicy</span></span>
<span data-ttu-id="9c72f-114">Tjänst tilldelnings princip för IoT-etablering</span><span class="sxs-lookup"><span data-stu-id="9c72f-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="9c72f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c72f-115">-DefaultProfile</span></span>
<span data-ttu-id="9c72f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c72f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c72f-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="9c72f-117">-Location</span></span>
<span data-ttu-id="9c72f-118">Plats</span><span class="sxs-lookup"><span data-stu-id="9c72f-118">Location</span></span>

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

### <span data-ttu-id="9c72f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c72f-119">-Name</span></span>
<span data-ttu-id="9c72f-120">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="9c72f-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9c72f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c72f-121">-ResourceGroupName</span></span>
<span data-ttu-id="9c72f-122">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="9c72f-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9c72f-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9c72f-123">-SkuName</span></span>
<span data-ttu-id="9c72f-124">N</span><span class="sxs-lookup"><span data-stu-id="9c72f-124">Sku</span></span>

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

### <span data-ttu-id="9c72f-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9c72f-125">-Tag</span></span>
<span data-ttu-id="9c72f-126">IoT enheter för etablerings tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="9c72f-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="9c72f-127">Egenskaps uppsättning i nyckel värde par i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9c72f-127">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c72f-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9c72f-128">-Confirm</span></span>
<span data-ttu-id="9c72f-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9c72f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c72f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c72f-130">-WhatIf</span></span>
<span data-ttu-id="9c72f-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9c72f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c72f-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9c72f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c72f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c72f-133">CommonParameters</span></span>
<span data-ttu-id="9c72f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c72f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c72f-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c72f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c72f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c72f-136">INPUTS</span></span>

### <span data-ttu-id="9c72f-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="9c72f-137">None</span></span>

## <span data-ttu-id="9c72f-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c72f-138">OUTPUTS</span></span>

### <span data-ttu-id="9c72f-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9c72f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="9c72f-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c72f-140">NOTES</span></span>

## <span data-ttu-id="9c72f-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c72f-141">RELATED LINKS</span></span>
