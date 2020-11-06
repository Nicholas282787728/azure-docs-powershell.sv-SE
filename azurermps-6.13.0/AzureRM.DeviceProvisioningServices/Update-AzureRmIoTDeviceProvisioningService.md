---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: 80032ab2a677683ff876aca499f7e0ee682e6fd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580104"
---
# <span data-ttu-id="53f55-101">Update-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="53f55-101">Update-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="53f55-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53f55-102">SYNOPSIS</span></span>
<span data-ttu-id="53f55-103">Uppdatera etablerings tjänsten för en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="53f55-103">Update an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53f55-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53f55-104">SYNTAX</span></span>

### <span data-ttu-id="53f55-105">ResourceUpdateSet (standard)</span><span class="sxs-lookup"><span data-stu-id="53f55-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53f55-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="53f55-106">InputObjectUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53f55-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="53f55-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53f55-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="53f55-108">ResourceIdUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53f55-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="53f55-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53f55-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="53f55-110">ResourceCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53f55-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53f55-111">DESCRIPTION</span></span>
<span data-ttu-id="53f55-112">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="53f55-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="53f55-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53f55-113">EXAMPLES</span></span>

### <span data-ttu-id="53f55-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="53f55-114">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

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

<span data-ttu-id="53f55-115">Uppdatera allokeringsregeln till "lång laten" för en Azure IoT Hub-enhet "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="53f55-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="53f55-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="53f55-116">Example 2</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

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

<span data-ttu-id="53f55-117">Lägg till " @tags " i taggen för en Azure IoT Hub-enhet "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="53f55-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="53f55-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="53f55-118">Example 3</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzureRmIoTDps -Tag @tags -Reset

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

<span data-ttu-id="53f55-119">Ta bort taggen och Lägg till ny " @tags " till taggen för en Azure IoT Hub-enhet "myiotdps" med pipeline.</span><span class="sxs-lookup"><span data-stu-id="53f55-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="53f55-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53f55-120">PARAMETERS</span></span>

### <span data-ttu-id="53f55-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="53f55-121">-AllocationPolicy</span></span>
<span data-ttu-id="53f55-122">Tjänst tilldelnings princip för IoT-etablering</span><span class="sxs-lookup"><span data-stu-id="53f55-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="53f55-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f55-123">-DefaultProfile</span></span>
<span data-ttu-id="53f55-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53f55-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53f55-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53f55-125">-InputObject</span></span>
<span data-ttu-id="53f55-126">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="53f55-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="53f55-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="53f55-127">-Name</span></span>
<span data-ttu-id="53f55-128">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="53f55-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="53f55-129">-Återställ</span><span class="sxs-lookup"><span data-stu-id="53f55-129">-Reset</span></span>
<span data-ttu-id="53f55-130">Återställ IoT-enhetens etablerings service märken</span><span class="sxs-lookup"><span data-stu-id="53f55-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="53f55-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f55-131">-ResourceGroupName</span></span>
<span data-ttu-id="53f55-132">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="53f55-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="53f55-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53f55-133">-ResourceId</span></span>
<span data-ttu-id="53f55-134">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="53f55-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="53f55-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="53f55-135">-Tag</span></span>
<span data-ttu-id="53f55-136">IoT Device Revisioning service-insamling</span><span class="sxs-lookup"><span data-stu-id="53f55-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="53f55-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53f55-137">-Confirm</span></span>
<span data-ttu-id="53f55-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53f55-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53f55-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f55-139">-WhatIf</span></span>
<span data-ttu-id="53f55-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53f55-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53f55-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53f55-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53f55-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f55-142">CommonParameters</span></span>
<span data-ttu-id="53f55-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f55-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f55-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53f55-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f55-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53f55-145">INPUTS</span></span>

### <span data-ttu-id="53f55-146">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="53f55-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="53f55-147">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="53f55-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="53f55-148">System. String</span><span class="sxs-lookup"><span data-stu-id="53f55-148">System.String</span></span>

## <span data-ttu-id="53f55-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53f55-149">OUTPUTS</span></span>

### <span data-ttu-id="53f55-150">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="53f55-150">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="53f55-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53f55-151">NOTES</span></span>

## <span data-ttu-id="53f55-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53f55-152">RELATED LINKS</span></span>
