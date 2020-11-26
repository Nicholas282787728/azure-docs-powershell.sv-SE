---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: e7b0a5296147408633316ed27f0cba87a65d3a2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263216"
---
# <span data-ttu-id="0f2d5-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="0f2d5-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="0f2d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="0f2d5-103">Uppdatera en enhets registrerings grupp.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="0f2d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f2d5-104">SYNTAX</span></span>

### <span data-ttu-id="0f2d5-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0f2d5-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f2d5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0f2d5-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f2d5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0f2d5-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f2d5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f2d5-108">DESCRIPTION</span></span>
<span data-ttu-id="0f2d5-109">Uppdatera en registrerings grupp i en Azure IoT Hub-enhets etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="0f2d5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f2d5-110">EXAMPLES</span></span>

### <span data-ttu-id="0f2d5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0f2d5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="0f2d5-112">Uppdatera tilldelnings principer och nav för en registrerings grupp.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-112">Update allocation policy and hubs for an enrollment group.</span></span>

## <span data-ttu-id="0f2d5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f2d5-113">PARAMETERS</span></span>

### <span data-ttu-id="0f2d5-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0f2d5-114">-AllocationPolicy</span></span>
<span data-ttu-id="0f2d5-115">Typ av tilldelning för enheten som tilldelats navet.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-115">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d5-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0f2d5-116">-ApiVersion</span></span>
<span data-ttu-id="0f2d5-117">API-versionen av etablerings tjänsten i begäran om anpassad tilldelning.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="0f2d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f2d5-118">-DefaultProfile</span></span>
<span data-ttu-id="0f2d5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f2d5-120">-Önskat</span><span class="sxs-lookup"><span data-stu-id="0f2d5-120">-Desired</span></span>
<span data-ttu-id="0f2d5-121">Ursprungliga önskade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="0f2d5-122">-DpsName</span><span class="sxs-lookup"><span data-stu-id="0f2d5-122">-DpsName</span></span>
<span data-ttu-id="0f2d5-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="0f2d5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0f2d5-124">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="0f2d5-124">-DpsObject</span></span>
<span data-ttu-id="0f2d5-125">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="0f2d5-125">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0f2d5-126">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="0f2d5-126">-EdgeEnabled</span></span>
<span data-ttu-id="0f2d5-127">Flagga som anger hur Edge ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-127">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d5-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="0f2d5-128">-IotHub</span></span>
<span data-ttu-id="0f2d5-129">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-129">Host name of target IoT Hub.</span></span>
<span data-ttu-id="0f2d5-130">Använd blankstegsavgränsad lista för flera IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-130">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d5-131">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="0f2d5-131">-IotHubHostName</span></span>
<span data-ttu-id="0f2d5-132">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-132">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="0f2d5-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f2d5-133">-Name</span></span>
<span data-ttu-id="0f2d5-134">Namn på registrerings gruppen.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-134">Name of the enrollment group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d5-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="0f2d5-135">-ProvisioningStatus</span></span>
<span data-ttu-id="0f2d5-136">Aktivera eller inaktivera registrerings posten.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-136">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d5-137">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="0f2d5-137">-ReprovisionPolicy</span></span>
<span data-ttu-id="0f2d5-138">Enhets data som ska hanteras vid ometablering till olika IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-138">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2d5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f2d5-139">-ResourceGroupName</span></span>
<span data-ttu-id="0f2d5-140">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="0f2d5-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0f2d5-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f2d5-141">-ResourceId</span></span>
<span data-ttu-id="0f2d5-142">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="0f2d5-142">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0f2d5-143">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0f2d5-143">-Tag</span></span>
<span data-ttu-id="0f2d5-144">Inledande dubbla taggar.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-144">Initial twin tags.</span></span>

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

### <span data-ttu-id="0f2d5-145">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="0f2d5-145">-WebhookUrl</span></span>
<span data-ttu-id="0f2d5-146">Webhook-URL som används för anpassade tilldelnings begär Anden.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-146">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="0f2d5-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f2d5-147">-Confirm</span></span>
<span data-ttu-id="0f2d5-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f2d5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f2d5-149">-WhatIf</span></span>
<span data-ttu-id="0f2d5-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f2d5-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f2d5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f2d5-152">CommonParameters</span></span>
<span data-ttu-id="0f2d5-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f2d5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f2d5-154">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f2d5-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f2d5-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f2d5-155">INPUTS</span></span>

### <span data-ttu-id="0f2d5-156">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0f2d5-156">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0f2d5-157">System. String</span><span class="sxs-lookup"><span data-stu-id="0f2d5-157">System.String</span></span>

## <span data-ttu-id="0f2d5-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f2d5-158">OUTPUTS</span></span>

### <span data-ttu-id="0f2d5-159">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="0f2d5-159">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="0f2d5-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f2d5-160">NOTES</span></span>

## <span data-ttu-id="0f2d5-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f2d5-161">RELATED LINKS</span></span>