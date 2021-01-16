---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7000d7cc6922cec022efad9faca2e61e539af0e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398440"
---
# <span data-ttu-id="c611c-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="c611c-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="c611c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c611c-102">SYNOPSIS</span></span>
<span data-ttu-id="c611c-103">Skapa en enhets registrerings grupp.</span><span class="sxs-lookup"><span data-stu-id="c611c-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="c611c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c611c-104">SYNTAX</span></span>

### <span data-ttu-id="c611c-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c611c-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c611c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c611c-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c611c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c611c-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c611c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c611c-108">DESCRIPTION</span></span>
<span data-ttu-id="c611c-109">Skapa en registrerings grupp i en Azure IoT Hub-enhets etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="c611c-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c611c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c611c-110">EXAMPLES</span></span>

### <span data-ttu-id="c611c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c611c-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="c611c-112">Skapa en registrering med attesterings typen SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="c611c-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="c611c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c611c-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="c611c-114">Skapa en registrering med attesterings typen X509</span><span class="sxs-lookup"><span data-stu-id="c611c-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="c611c-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c611c-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="c611c-116">Skapa en registrering med attesterings typen SymmetricKey och initialt skick.</span><span class="sxs-lookup"><span data-stu-id="c611c-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="c611c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c611c-117">PARAMETERS</span></span>

### <span data-ttu-id="c611c-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="c611c-118">-AllocationPolicy</span></span>
<span data-ttu-id="c611c-119">Typ av tilldelning för enheten som tilldelats navet.</span><span class="sxs-lookup"><span data-stu-id="c611c-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="c611c-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c611c-120">-ApiVersion</span></span>
<span data-ttu-id="c611c-121">API-versionen av etablerings tjänsten i begäran om anpassad tilldelning.</span><span class="sxs-lookup"><span data-stu-id="c611c-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="c611c-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="c611c-122">-AttestationType</span></span>
<span data-ttu-id="c611c-123">Mekanismen för attestering.</span><span class="sxs-lookup"><span data-stu-id="c611c-123">Attestation Mechanism.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAttestationMechanismType
Parameter Sets: (All)
Aliases:
Accepted values: None, Tpm, X509, SymmetricKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c611c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c611c-124">-DefaultProfile</span></span>
<span data-ttu-id="c611c-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c611c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c611c-126">-Önskat</span><span class="sxs-lookup"><span data-stu-id="c611c-126">-Desired</span></span>
<span data-ttu-id="c611c-127">Ursprungliga önskade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c611c-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="c611c-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="c611c-128">-DpsName</span></span>
<span data-ttu-id="c611c-129">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="c611c-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c611c-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c611c-130">-DpsObject</span></span>
<span data-ttu-id="c611c-131">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="c611c-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c611c-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="c611c-132">-EdgeEnabled</span></span>
<span data-ttu-id="c611c-133">Flagga som anger hur Edge ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="c611c-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="c611c-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="c611c-134">-IotHub</span></span>
<span data-ttu-id="c611c-135">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="c611c-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="c611c-136">Använd blankstegsavgränsad lista för flera IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="c611c-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="c611c-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="c611c-137">-IotHubHostName</span></span>
<span data-ttu-id="c611c-138">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="c611c-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="c611c-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="c611c-139">-Name</span></span>
<span data-ttu-id="c611c-140">Namn på registrerings gruppen.</span><span class="sxs-lookup"><span data-stu-id="c611c-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="c611c-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="c611c-141">-PrimaryCAName</span></span>
<span data-ttu-id="c611c-142">Namnet på det primära rot certifikat utfärdarens certifikat.</span><span class="sxs-lookup"><span data-stu-id="c611c-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="c611c-143">Om attestering med ett rotcertifikatutfärdarcertifikat är önskat måste ett namn på rot certifikat utfärdare anges.</span><span class="sxs-lookup"><span data-stu-id="c611c-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="c611c-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="c611c-144">-PrimaryCertificate</span></span>
<span data-ttu-id="c611c-145">Sökvägen till filen som innehåller det primära certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c611c-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="c611c-146">Base-64-representation av X509 Certificate. cer-fil eller PEM-fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="c611c-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="c611c-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c611c-147">-PrimaryKey</span></span>
<span data-ttu-id="c611c-148">Den primära symmetriska delade åtkomst nycklar som lagras i base64-format.</span><span class="sxs-lookup"><span data-stu-id="c611c-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="c611c-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="c611c-149">-ProvisioningStatus</span></span>
<span data-ttu-id="c611c-150">Aktivera eller inaktivera registrerings posten.</span><span class="sxs-lookup"><span data-stu-id="c611c-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="c611c-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="c611c-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="c611c-152">Enhets data som ska hanteras vid ometablering till olika IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="c611c-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="c611c-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c611c-153">-ResourceGroupName</span></span>
<span data-ttu-id="c611c-154">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c611c-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c611c-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c611c-155">-ResourceId</span></span>
<span data-ttu-id="c611c-156">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="c611c-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c611c-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="c611c-157">-RootCertificate</span></span>
<span data-ttu-id="c611c-158">Gör det möjligt att skapa X509attestation med rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="c611c-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="c611c-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="c611c-159">-SecondaryCAName</span></span>
<span data-ttu-id="c611c-160">Namnet på den sekundära rot certifikat utfärdarens certifikat.</span><span class="sxs-lookup"><span data-stu-id="c611c-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="c611c-161">Om attestering med ett rotcertifikatutfärdarcertifikat är önskat måste ett namn på rot certifikat utfärdare anges.</span><span class="sxs-lookup"><span data-stu-id="c611c-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="c611c-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="c611c-162">-SecondaryCertificate</span></span>
<span data-ttu-id="c611c-163">Sökvägen till filen som innehåller det sekundära certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c611c-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="c611c-164">Base-64-representation av X509 Certificate. cer-fil eller PEM-fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="c611c-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="c611c-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="c611c-165">-SecondaryKey</span></span>
<span data-ttu-id="c611c-166">Den sekundära symmetriska delade åtkomst nycklar som lagras i base64-format.</span><span class="sxs-lookup"><span data-stu-id="c611c-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="c611c-167">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c611c-167">-Tag</span></span>
<span data-ttu-id="c611c-168">Inledande dubbla taggar.</span><span class="sxs-lookup"><span data-stu-id="c611c-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="c611c-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="c611c-169">-WebhookUrl</span></span>
<span data-ttu-id="c611c-170">Webhook-URL som används för anpassade tilldelnings begär Anden.</span><span class="sxs-lookup"><span data-stu-id="c611c-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="c611c-171">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c611c-171">-Confirm</span></span>
<span data-ttu-id="c611c-172">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c611c-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c611c-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c611c-173">-WhatIf</span></span>
<span data-ttu-id="c611c-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c611c-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c611c-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c611c-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c611c-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c611c-176">CommonParameters</span></span>
<span data-ttu-id="c611c-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c611c-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c611c-178">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c611c-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c611c-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c611c-179">INPUTS</span></span>

### <span data-ttu-id="c611c-180">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c611c-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c611c-181">System. String</span><span class="sxs-lookup"><span data-stu-id="c611c-181">System.String</span></span>

## <span data-ttu-id="c611c-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c611c-182">OUTPUTS</span></span>

### <span data-ttu-id="c611c-183">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="c611c-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="c611c-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c611c-184">NOTES</span></span>

## <span data-ttu-id="c611c-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c611c-185">RELATED LINKS</span></span>
