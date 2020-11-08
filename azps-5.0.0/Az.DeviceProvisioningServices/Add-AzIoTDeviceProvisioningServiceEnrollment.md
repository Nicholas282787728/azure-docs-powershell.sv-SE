---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: e02d9c1ca9a5d45f081f168c3d8736d502f52094
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263260"
---
# <span data-ttu-id="82b2a-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="82b2a-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="82b2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="82b2a-103">Skapa en enhets registrerings post.</span><span class="sxs-lookup"><span data-stu-id="82b2a-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="82b2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82b2a-104">SYNTAX</span></span>

### <span data-ttu-id="82b2a-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="82b2a-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82b2a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="82b2a-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82b2a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="82b2a-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 -AttestationType <PSAttestationMechanismType> [-DeviceId <String>] [-EndorsementKey <String>]
 [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82b2a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82b2a-108">DESCRIPTION</span></span>
<span data-ttu-id="82b2a-109">Skapa en enhets registrering i en Azure IoT Hub-enhet för etablering.</span><span class="sxs-lookup"><span data-stu-id="82b2a-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="82b2a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82b2a-110">EXAMPLES</span></span>

### <span data-ttu-id="82b2a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82b2a-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="82b2a-112">Skapa en registrering med attesterings typen SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="82b2a-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="82b2a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="82b2a-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="82b2a-114">Skapa en registrering med TPM-attestering.</span><span class="sxs-lookup"><span data-stu-id="82b2a-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="82b2a-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="82b2a-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="82b2a-116">Skapa en registrering med attesterings typen X509</span><span class="sxs-lookup"><span data-stu-id="82b2a-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="82b2a-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="82b2a-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="82b2a-118">Skapa en registrering med attesterings typen SymmetricKey och initialt skick.</span><span class="sxs-lookup"><span data-stu-id="82b2a-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="82b2a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82b2a-119">PARAMETERS</span></span>

### <span data-ttu-id="82b2a-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="82b2a-120">-AllocationPolicy</span></span>
<span data-ttu-id="82b2a-121">Typ av tilldelning för enheten som tilldelats navet.</span><span class="sxs-lookup"><span data-stu-id="82b2a-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="82b2a-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="82b2a-122">-ApiVersion</span></span>
<span data-ttu-id="82b2a-123">API-versionen av etablerings tjänsten i begäran om anpassad tilldelning.</span><span class="sxs-lookup"><span data-stu-id="82b2a-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="82b2a-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="82b2a-124">-AttestationType</span></span>
<span data-ttu-id="82b2a-125">Mekanismen för attestering.</span><span class="sxs-lookup"><span data-stu-id="82b2a-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="82b2a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b2a-126">-DefaultProfile</span></span>
<span data-ttu-id="82b2a-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82b2a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b2a-128">-Önskat</span><span class="sxs-lookup"><span data-stu-id="82b2a-128">-Desired</span></span>
<span data-ttu-id="82b2a-129">Ursprungliga önskade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="82b2a-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="82b2a-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="82b2a-130">-DeviceId</span></span>
<span data-ttu-id="82b2a-131">IoT Hub-enhetens ID.</span><span class="sxs-lookup"><span data-stu-id="82b2a-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="82b2a-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="82b2a-132">-DpsName</span></span>
<span data-ttu-id="82b2a-133">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="82b2a-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="82b2a-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="82b2a-134">-DpsObject</span></span>
<span data-ttu-id="82b2a-135">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="82b2a-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="82b2a-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="82b2a-136">-EdgeEnabled</span></span>
<span data-ttu-id="82b2a-137">Flagga som anger hur Edge ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="82b2a-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="82b2a-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="82b2a-138">-EndorsementKey</span></span>
<span data-ttu-id="82b2a-139">TPM-påskrift för en TPM-enhet.</span><span class="sxs-lookup"><span data-stu-id="82b2a-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="82b2a-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="82b2a-140">-IotHub</span></span>
<span data-ttu-id="82b2a-141">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="82b2a-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="82b2a-142">Använd blankstegsavgränsad lista för flera IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="82b2a-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="82b2a-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="82b2a-143">-IotHubHostName</span></span>
<span data-ttu-id="82b2a-144">Värd namnet på mål-IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="82b2a-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="82b2a-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="82b2a-145">-PrimaryCAName</span></span>
<span data-ttu-id="82b2a-146">Namnet på det primära rot certifikat utfärdarens certifikat.</span><span class="sxs-lookup"><span data-stu-id="82b2a-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="82b2a-147">Om attestering med ett rotcertifikatutfärdarcertifikat är önskat måste ett namn på rot certifikat utfärdare anges.</span><span class="sxs-lookup"><span data-stu-id="82b2a-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="82b2a-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="82b2a-148">-PrimaryCertificate</span></span>
<span data-ttu-id="82b2a-149">Sökvägen till filen som innehåller det primära certifikatet.</span><span class="sxs-lookup"><span data-stu-id="82b2a-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="82b2a-150">Base-64-representation av X509 Certificate. cer-fil eller PEM-fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="82b2a-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="82b2a-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="82b2a-151">-PrimaryKey</span></span>
<span data-ttu-id="82b2a-152">Den primära symmetriska delade åtkomst nycklar som lagras i base64-format.</span><span class="sxs-lookup"><span data-stu-id="82b2a-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="82b2a-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="82b2a-153">-ProvisioningStatus</span></span>
<span data-ttu-id="82b2a-154">Aktivera eller inaktivera registrerings posten.</span><span class="sxs-lookup"><span data-stu-id="82b2a-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="82b2a-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="82b2a-155">-RegistrationId</span></span>
<span data-ttu-id="82b2a-156">Registrerings-ID för individuell registrering.</span><span class="sxs-lookup"><span data-stu-id="82b2a-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="82b2a-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="82b2a-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="82b2a-158">Enhets data som ska hanteras vid ometablering till olika IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="82b2a-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="82b2a-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b2a-159">-ResourceGroupName</span></span>
<span data-ttu-id="82b2a-160">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="82b2a-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="82b2a-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82b2a-161">-ResourceId</span></span>
<span data-ttu-id="82b2a-162">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="82b2a-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="82b2a-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="82b2a-163">-RootCertificate</span></span>
<span data-ttu-id="82b2a-164">Gör det möjligt att skapa X509attestation med rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="82b2a-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="82b2a-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="82b2a-165">-SecondaryCAName</span></span>
<span data-ttu-id="82b2a-166">Namnet på den sekundära rot certifikat utfärdarens certifikat.</span><span class="sxs-lookup"><span data-stu-id="82b2a-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="82b2a-167">Om attestering med ett rotcertifikatutfärdarcertifikat är önskat måste ett namn på rot certifikat utfärdare anges.</span><span class="sxs-lookup"><span data-stu-id="82b2a-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="82b2a-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="82b2a-168">-SecondaryCertificate</span></span>
<span data-ttu-id="82b2a-169">Sökvägen till filen som innehåller det sekundära certifikatet.</span><span class="sxs-lookup"><span data-stu-id="82b2a-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="82b2a-170">Base-64-representation av X509 Certificate. cer-fil eller PEM-fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="82b2a-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="82b2a-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="82b2a-171">-SecondaryKey</span></span>
<span data-ttu-id="82b2a-172">Den sekundära symmetriska delade åtkomst nycklar som lagras i base64-format.</span><span class="sxs-lookup"><span data-stu-id="82b2a-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="82b2a-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="82b2a-173">-StorageRootKey</span></span>
<span data-ttu-id="82b2a-174">TPM-lagringsenheten för en TPM-enhet.</span><span class="sxs-lookup"><span data-stu-id="82b2a-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="82b2a-175">-Tagg</span><span class="sxs-lookup"><span data-stu-id="82b2a-175">-Tag</span></span>
<span data-ttu-id="82b2a-176">Inledande dubbla taggar.</span><span class="sxs-lookup"><span data-stu-id="82b2a-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="82b2a-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="82b2a-177">-WebhookUrl</span></span>
<span data-ttu-id="82b2a-178">Webhook-URL som används för anpassade tilldelnings begär Anden.</span><span class="sxs-lookup"><span data-stu-id="82b2a-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="82b2a-179">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82b2a-179">-Confirm</span></span>
<span data-ttu-id="82b2a-180">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82b2a-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82b2a-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82b2a-181">-WhatIf</span></span>
<span data-ttu-id="82b2a-182">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82b2a-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82b2a-183">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82b2a-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82b2a-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b2a-184">CommonParameters</span></span>
<span data-ttu-id="82b2a-185">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82b2a-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b2a-186">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82b2a-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b2a-187">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82b2a-187">INPUTS</span></span>

### <span data-ttu-id="82b2a-188">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="82b2a-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="82b2a-189">System. String</span><span class="sxs-lookup"><span data-stu-id="82b2a-189">System.String</span></span>

## <span data-ttu-id="82b2a-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82b2a-190">OUTPUTS</span></span>

### <span data-ttu-id="82b2a-191">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="82b2a-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="82b2a-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82b2a-192">NOTES</span></span>

## <span data-ttu-id="82b2a-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82b2a-193">RELATED LINKS</span></span>
