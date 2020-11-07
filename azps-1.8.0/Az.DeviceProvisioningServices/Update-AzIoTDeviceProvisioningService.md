---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 7d41a75473d26b113e5d4e4163775269b8b9f60d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754136"
---
# <span data-ttu-id="8ed64-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="8ed64-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="8ed64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ed64-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed64-103">Uppdatera etablerings tjänsten för en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="8ed64-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="8ed64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ed64-104">SYNTAX</span></span>

### <span data-ttu-id="8ed64-105">ResourceUpdateSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8ed64-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed64-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="8ed64-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed64-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="8ed64-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ed64-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="8ed64-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed64-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="8ed64-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed64-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="8ed64-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ed64-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ed64-111">DESCRIPTION</span></span>
<span data-ttu-id="8ed64-112">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="8ed64-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="8ed64-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ed64-113">EXAMPLES</span></span>

### <span data-ttu-id="8ed64-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8ed64-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="8ed64-115">Uppdatera allokeringsregeln till "lång laten" för en Azure IoT Hub-enhet "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="8ed64-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="8ed64-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8ed64-116">Example 2</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="8ed64-117">Lägg till " @tags " i taggen för en Azure IoT Hub-enhet "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="8ed64-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="8ed64-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8ed64-118">Example 3</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag @tags -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="8ed64-119">Ta bort taggen och Lägg till ny " @tags " till taggen för en Azure IoT Hub-enhet "myiotdps" med pipeline.</span><span class="sxs-lookup"><span data-stu-id="8ed64-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="8ed64-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ed64-120">PARAMETERS</span></span>

### <span data-ttu-id="8ed64-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="8ed64-121">-AllocationPolicy</span></span>
<span data-ttu-id="8ed64-122">Tjänst tilldelnings princip för IoT-etablering</span><span class="sxs-lookup"><span data-stu-id="8ed64-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ed64-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed64-123">-DefaultProfile</span></span>
<span data-ttu-id="8ed64-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ed64-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ed64-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ed64-125">-InputObject</span></span>
<span data-ttu-id="8ed64-126">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="8ed64-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed64-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="8ed64-127">-Name</span></span>
<span data-ttu-id="8ed64-128">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="8ed64-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ed64-129">-Återställ</span><span class="sxs-lookup"><span data-stu-id="8ed64-129">-Reset</span></span>
<span data-ttu-id="8ed64-130">Återställ IoT-enhetens etablerings service märken</span><span class="sxs-lookup"><span data-stu-id="8ed64-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ed64-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ed64-131">-ResourceGroupName</span></span>
<span data-ttu-id="8ed64-132">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="8ed64-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ed64-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ed64-133">-ResourceId</span></span>
<span data-ttu-id="8ed64-134">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="8ed64-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ed64-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8ed64-135">-Tag</span></span>
<span data-ttu-id="8ed64-136">IoT Device Revisioning service-insamling</span><span class="sxs-lookup"><span data-stu-id="8ed64-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ed64-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8ed64-137">-Confirm</span></span>
<span data-ttu-id="8ed64-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8ed64-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ed64-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ed64-139">-WhatIf</span></span>
<span data-ttu-id="8ed64-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8ed64-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ed64-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8ed64-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ed64-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed64-142">CommonParameters</span></span>
<span data-ttu-id="8ed64-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ed64-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed64-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ed64-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed64-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ed64-145">INPUTS</span></span>

### <span data-ttu-id="8ed64-146">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8ed64-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="8ed64-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8ed64-147">System.String</span></span>

## <span data-ttu-id="8ed64-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ed64-148">OUTPUTS</span></span>

### <span data-ttu-id="8ed64-149">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8ed64-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="8ed64-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ed64-150">NOTES</span></span>

## <span data-ttu-id="8ed64-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ed64-151">RELATED LINKS</span></span>
