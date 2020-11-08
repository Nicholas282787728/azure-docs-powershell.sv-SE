---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8a81df2081420f8d218e094ff43f22e8dd9cc5c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263218"
---
# <span data-ttu-id="bcd84-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="bcd84-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="bcd84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bcd84-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd84-103">Uppdatera en enhets registrerings post.</span><span class="sxs-lookup"><span data-stu-id="bcd84-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="bcd84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bcd84-104">SYNTAX</span></span>

### <span data-ttu-id="bcd84-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bcd84-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcd84-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bcd84-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcd84-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bcd84-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcd84-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bcd84-108">DESCRIPTION</span></span>
<span data-ttu-id="bcd84-109">Uppdatera en enhets registrering i en Azure IoT Hub-enhet för etablering.</span><span class="sxs-lookup"><span data-stu-id="bcd84-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="bcd84-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bcd84-110">EXAMPLES</span></span>

### <span data-ttu-id="bcd84-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bcd84-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="bcd84-112">Uppdatera tilldelnings principer och hubbar för en registrerings post.</span><span class="sxs-lookup"><span data-stu-id="bcd84-112">Update allocation policy and hubs for an enrollment record.</span></span>

## <span data-ttu-id="bcd84-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bcd84-113">PARAMETERS</span></span>

### <span data-ttu-id="bcd84-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="bcd84-114">-AllocationPolicy</span></span>
<span data-ttu-id="bcd84-115">Typ av tilldelning för enheten som tilldelats navet.</span><span class="sxs-lookup"><span data-stu-id="bcd84-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="bcd84-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bcd84-116">-ApiVersion</span></span>
<span data-ttu-id="bcd84-117">API-versionen av etablerings tjänsten i begäran om anpassad tilldelning.</span><span class="sxs-lookup"><span data-stu-id="bcd84-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="bcd84-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd84-118">-DefaultProfile</span></span>
<span data-ttu-id="bcd84-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bcd84-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcd84-120">-Önskat</span><span class="sxs-lookup"><span data-stu-id="bcd84-120">-Desired</span></span>
<span data-ttu-id="bcd84-121">Ursprungliga önskade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="bcd84-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="bcd84-122">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="bcd84-122">-DeviceId</span></span>
<span data-ttu-id="bcd84-123">IoT Hub-enhetens ID.</span><span class="sxs-lookup"><span data-stu-id="bcd84-123">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="bcd84-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="bcd84-124">-DpsName</span></span>
<span data-ttu-id="bcd84-125">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="bcd84-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="bcd84-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="bcd84-126">-DpsObject</span></span>
<span data-ttu-id="bcd84-127">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="bcd84-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="bcd84-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="bcd84-128">-EdgeEnabled</span></span>
<span data-ttu-id="bcd84-129">Flagga som anger hur Edge ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="bcd84-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="bcd84-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="bcd84-130">-IotHub</span></span>
<span data-ttu-id="bcd84-131">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="bcd84-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="bcd84-132">Använd blankstegsavgränsad lista för flera IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="bcd84-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="bcd84-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="bcd84-133">-IotHubHostName</span></span>
<span data-ttu-id="bcd84-134">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="bcd84-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="bcd84-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="bcd84-135">-ProvisioningStatus</span></span>
<span data-ttu-id="bcd84-136">Aktivera eller inaktivera registrerings posten.</span><span class="sxs-lookup"><span data-stu-id="bcd84-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="bcd84-137">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="bcd84-137">-RegistrationId</span></span>
<span data-ttu-id="bcd84-138">Registrerings-ID för individuell registrering.</span><span class="sxs-lookup"><span data-stu-id="bcd84-138">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="bcd84-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="bcd84-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="bcd84-140">Enhets data som ska hanteras vid ometablering till olika IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="bcd84-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="bcd84-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcd84-141">-ResourceGroupName</span></span>
<span data-ttu-id="bcd84-142">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="bcd84-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bcd84-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcd84-143">-ResourceId</span></span>
<span data-ttu-id="bcd84-144">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="bcd84-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="bcd84-145">-Tagg</span><span class="sxs-lookup"><span data-stu-id="bcd84-145">-Tag</span></span>
<span data-ttu-id="bcd84-146">Inledande dubbla taggar.</span><span class="sxs-lookup"><span data-stu-id="bcd84-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="bcd84-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="bcd84-147">-WebhookUrl</span></span>
<span data-ttu-id="bcd84-148">Webhook-URL som används för anpassade tilldelnings begär Anden.</span><span class="sxs-lookup"><span data-stu-id="bcd84-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="bcd84-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bcd84-149">-Confirm</span></span>
<span data-ttu-id="bcd84-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bcd84-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcd84-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcd84-151">-WhatIf</span></span>
<span data-ttu-id="bcd84-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bcd84-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcd84-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bcd84-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcd84-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd84-154">CommonParameters</span></span>
<span data-ttu-id="bcd84-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcd84-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd84-156">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcd84-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd84-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bcd84-157">INPUTS</span></span>

### <span data-ttu-id="bcd84-158">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="bcd84-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="bcd84-159">System. String</span><span class="sxs-lookup"><span data-stu-id="bcd84-159">System.String</span></span>

## <span data-ttu-id="bcd84-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bcd84-160">OUTPUTS</span></span>

### <span data-ttu-id="bcd84-161">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="bcd84-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="bcd84-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bcd84-162">NOTES</span></span>

## <span data-ttu-id="bcd84-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bcd84-163">RELATED LINKS</span></span>
