---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 47c5c5119e41f3feeaccda66871d902e631c9ac2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396627"
---
# <span data-ttu-id="7fb01-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="7fb01-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="7fb01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fb01-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb01-103">Uppdatera en enhets registrerings post.</span><span class="sxs-lookup"><span data-stu-id="7fb01-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="7fb01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fb01-104">SYNTAX</span></span>

### <span data-ttu-id="7fb01-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7fb01-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fb01-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7fb01-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fb01-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7fb01-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb01-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fb01-108">DESCRIPTION</span></span>
<span data-ttu-id="7fb01-109">Uppdatera en enhets registrering i en Azure IoT Hub-enhet för etablering.</span><span class="sxs-lookup"><span data-stu-id="7fb01-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="7fb01-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fb01-110">EXAMPLES</span></span>

### <span data-ttu-id="7fb01-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7fb01-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="7fb01-112">Uppdatera tilldelnings principer och hubbar för en registrerings post.</span><span class="sxs-lookup"><span data-stu-id="7fb01-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="7fb01-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7fb01-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="7fb01-114">Uppdatera registreringens initialer.</span><span class="sxs-lookup"><span data-stu-id="7fb01-114">Update an enrollment's initial twin state.</span></span>

## <span data-ttu-id="7fb01-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fb01-115">PARAMETERS</span></span>

### <span data-ttu-id="7fb01-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="7fb01-116">-AllocationPolicy</span></span>
<span data-ttu-id="7fb01-117">Typ av tilldelning för enheten som tilldelats navet.</span><span class="sxs-lookup"><span data-stu-id="7fb01-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="7fb01-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7fb01-118">-ApiVersion</span></span>
<span data-ttu-id="7fb01-119">API-versionen av etablerings tjänsten i begäran om anpassad tilldelning.</span><span class="sxs-lookup"><span data-stu-id="7fb01-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="7fb01-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb01-120">-DefaultProfile</span></span>
<span data-ttu-id="7fb01-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb01-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb01-122">-Önskat</span><span class="sxs-lookup"><span data-stu-id="7fb01-122">-Desired</span></span>
<span data-ttu-id="7fb01-123">Ursprungliga önskade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7fb01-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="7fb01-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7fb01-124">-DeviceId</span></span>
<span data-ttu-id="7fb01-125">IoT Hub-enhetens ID.</span><span class="sxs-lookup"><span data-stu-id="7fb01-125">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="7fb01-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="7fb01-126">-DpsName</span></span>
<span data-ttu-id="7fb01-127">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="7fb01-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7fb01-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="7fb01-128">-DpsObject</span></span>
<span data-ttu-id="7fb01-129">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="7fb01-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7fb01-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7fb01-130">-EdgeEnabled</span></span>
<span data-ttu-id="7fb01-131">Flagga som anger hur Edge ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="7fb01-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="7fb01-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="7fb01-132">-IotHub</span></span>
<span data-ttu-id="7fb01-133">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="7fb01-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="7fb01-134">Använd blankstegsavgränsad lista för flera IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="7fb01-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="7fb01-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="7fb01-135">-IotHubHostName</span></span>
<span data-ttu-id="7fb01-136">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="7fb01-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="7fb01-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="7fb01-137">-ProvisioningStatus</span></span>
<span data-ttu-id="7fb01-138">Aktivera eller inaktivera registrerings posten.</span><span class="sxs-lookup"><span data-stu-id="7fb01-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="7fb01-139">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="7fb01-139">-RegistrationId</span></span>
<span data-ttu-id="7fb01-140">Registrerings-ID för individuell registrering.</span><span class="sxs-lookup"><span data-stu-id="7fb01-140">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="7fb01-141">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="7fb01-141">-ReprovisionPolicy</span></span>
<span data-ttu-id="7fb01-142">Enhets data som ska hanteras vid ometablering till olika IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="7fb01-142">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="7fb01-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb01-143">-ResourceGroupName</span></span>
<span data-ttu-id="7fb01-144">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="7fb01-144">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7fb01-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fb01-145">-ResourceId</span></span>
<span data-ttu-id="7fb01-146">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="7fb01-146">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7fb01-147">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7fb01-147">-Tag</span></span>
<span data-ttu-id="7fb01-148">Inledande dubbla taggar.</span><span class="sxs-lookup"><span data-stu-id="7fb01-148">Initial twin tags.</span></span>

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

### <span data-ttu-id="7fb01-149">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="7fb01-149">-WebhookUrl</span></span>
<span data-ttu-id="7fb01-150">Webhook-URL som används för anpassade tilldelnings begär Anden.</span><span class="sxs-lookup"><span data-stu-id="7fb01-150">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="7fb01-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7fb01-151">-Confirm</span></span>
<span data-ttu-id="7fb01-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7fb01-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb01-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb01-153">-WhatIf</span></span>
<span data-ttu-id="7fb01-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7fb01-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb01-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7fb01-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb01-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb01-156">CommonParameters</span></span>
<span data-ttu-id="7fb01-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb01-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb01-158">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb01-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb01-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fb01-159">INPUTS</span></span>

### <span data-ttu-id="7fb01-160">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="7fb01-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="7fb01-161">System. String</span><span class="sxs-lookup"><span data-stu-id="7fb01-161">System.String</span></span>

## <span data-ttu-id="7fb01-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fb01-162">OUTPUTS</span></span>

### <span data-ttu-id="7fb01-163">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="7fb01-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="7fb01-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fb01-164">NOTES</span></span>

## <span data-ttu-id="7fb01-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fb01-165">RELATED LINKS</span></span>
