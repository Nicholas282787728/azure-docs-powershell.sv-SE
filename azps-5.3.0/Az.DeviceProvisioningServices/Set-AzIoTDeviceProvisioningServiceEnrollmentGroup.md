---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522646"
---
# <span data-ttu-id="05304-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="05304-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="05304-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05304-102">SYNOPSIS</span></span>
<span data-ttu-id="05304-103">Uppdatera en enhets registrerings grupp.</span><span class="sxs-lookup"><span data-stu-id="05304-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="05304-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05304-104">SYNTAX</span></span>

### <span data-ttu-id="05304-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="05304-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05304-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="05304-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05304-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="05304-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05304-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05304-108">DESCRIPTION</span></span>
<span data-ttu-id="05304-109">Uppdatera en registrerings grupp i en Azure IoT Hub-enhets etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="05304-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="05304-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05304-110">EXAMPLES</span></span>

### <span data-ttu-id="05304-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="05304-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="05304-112">Uppdatera tilldelnings principer och nav för en registrerings grupp.</span><span class="sxs-lookup"><span data-stu-id="05304-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="05304-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="05304-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="05304-114">Uppdatera en registrerings grupps initiala status.</span><span class="sxs-lookup"><span data-stu-id="05304-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="05304-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05304-115">PARAMETERS</span></span>

### <span data-ttu-id="05304-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="05304-116">-AllocationPolicy</span></span>
<span data-ttu-id="05304-117">Typ av tilldelning för enheten som tilldelats navet.</span><span class="sxs-lookup"><span data-stu-id="05304-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="05304-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="05304-118">-ApiVersion</span></span>
<span data-ttu-id="05304-119">API-versionen av etablerings tjänsten i begäran om anpassad tilldelning.</span><span class="sxs-lookup"><span data-stu-id="05304-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="05304-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05304-120">-DefaultProfile</span></span>
<span data-ttu-id="05304-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05304-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05304-122">-Önskat</span><span class="sxs-lookup"><span data-stu-id="05304-122">-Desired</span></span>
<span data-ttu-id="05304-123">Ursprungliga önskade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="05304-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="05304-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="05304-124">-DpsName</span></span>
<span data-ttu-id="05304-125">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="05304-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="05304-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="05304-126">-DpsObject</span></span>
<span data-ttu-id="05304-127">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="05304-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="05304-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="05304-128">-EdgeEnabled</span></span>
<span data-ttu-id="05304-129">Flagga som anger hur Edge ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="05304-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="05304-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="05304-130">-IotHub</span></span>
<span data-ttu-id="05304-131">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="05304-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="05304-132">Använd blankstegsavgränsad lista för flera IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="05304-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="05304-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="05304-133">-IotHubHostName</span></span>
<span data-ttu-id="05304-134">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="05304-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="05304-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="05304-135">-Name</span></span>
<span data-ttu-id="05304-136">Namn på registrerings gruppen.</span><span class="sxs-lookup"><span data-stu-id="05304-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="05304-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="05304-137">-ProvisioningStatus</span></span>
<span data-ttu-id="05304-138">Aktivera eller inaktivera registrerings posten.</span><span class="sxs-lookup"><span data-stu-id="05304-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="05304-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="05304-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="05304-140">Enhets data som ska hanteras vid ometablering till olika IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="05304-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="05304-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05304-141">-ResourceGroupName</span></span>
<span data-ttu-id="05304-142">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="05304-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="05304-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05304-143">-ResourceId</span></span>
<span data-ttu-id="05304-144">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="05304-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="05304-145">-Tagg</span><span class="sxs-lookup"><span data-stu-id="05304-145">-Tag</span></span>
<span data-ttu-id="05304-146">Inledande dubbla taggar.</span><span class="sxs-lookup"><span data-stu-id="05304-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="05304-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="05304-147">-WebhookUrl</span></span>
<span data-ttu-id="05304-148">Webhook-URL som används för anpassade tilldelnings begär Anden.</span><span class="sxs-lookup"><span data-stu-id="05304-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="05304-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05304-149">-Confirm</span></span>
<span data-ttu-id="05304-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05304-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05304-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05304-151">-WhatIf</span></span>
<span data-ttu-id="05304-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05304-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05304-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05304-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05304-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05304-154">CommonParameters</span></span>
<span data-ttu-id="05304-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05304-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05304-156">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05304-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05304-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05304-157">INPUTS</span></span>

### <span data-ttu-id="05304-158">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="05304-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="05304-159">System. String</span><span class="sxs-lookup"><span data-stu-id="05304-159">System.String</span></span>

## <span data-ttu-id="05304-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05304-160">OUTPUTS</span></span>

### <span data-ttu-id="05304-161">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="05304-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="05304-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05304-162">NOTES</span></span>

## <span data-ttu-id="05304-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05304-163">RELATED LINKS</span></span>
