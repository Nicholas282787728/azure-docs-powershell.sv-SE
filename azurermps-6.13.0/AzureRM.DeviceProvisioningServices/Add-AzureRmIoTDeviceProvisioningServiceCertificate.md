---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 098689074debe4b9cf5be4d682023186b123d504
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757891"
---
# <span data-ttu-id="000d5-101">Add-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="000d5-101">Add-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="000d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="000d5-102">SYNOPSIS</span></span>
<span data-ttu-id="000d5-103">Skapa/uppdatera ett certifikat för konfiguration av en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="000d5-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="000d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="000d5-104">SYNTAX</span></span>

### <span data-ttu-id="000d5-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="000d5-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="000d5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="000d5-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="000d5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="000d5-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="000d5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="000d5-108">DESCRIPTION</span></span>
<span data-ttu-id="000d5-109">Uppladdar ett nytt certifikat eller ersätter det befintliga certifikatet med samma namn.</span><span class="sxs-lookup"><span data-stu-id="000d5-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="000d5-110">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i konfigurations tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="000d5-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="000d5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="000d5-111">EXAMPLES</span></span>

### <span data-ttu-id="000d5-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="000d5-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="000d5-113">Ladda upp en CER-fil för CA-certifikat till en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="000d5-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="000d5-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="000d5-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="000d5-115">Uppdaterar ett CERTIFIKATUTFÄRDARCERTIFIKAT i en IoT Hub-enhets etablerings tjänst genom att överföra en ny CER-fil.</span><span class="sxs-lookup"><span data-stu-id="000d5-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="000d5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="000d5-116">PARAMETERS</span></span>

### <span data-ttu-id="000d5-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="000d5-117">-CertificateName</span></span>
<span data-ttu-id="000d5-118">Namnet på IoT-enhetens etablerings tjänst certifikat</span><span class="sxs-lookup"><span data-stu-id="000d5-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="000d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="000d5-119">-DefaultProfile</span></span>
<span data-ttu-id="000d5-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="000d5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="000d5-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="000d5-121">-Etag</span></span>
<span data-ttu-id="000d5-122">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="000d5-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="000d5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="000d5-123">-InputObject</span></span>
<span data-ttu-id="000d5-124">Objekt för webb tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="000d5-124">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="000d5-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="000d5-125">-Name</span></span>
<span data-ttu-id="000d5-126">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="000d5-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="000d5-127">-Path</span><span class="sxs-lookup"><span data-stu-id="000d5-127">-Path</span></span>
<span data-ttu-id="000d5-128">Base-64-representation av X509-certifikat. cer-fil eller. PEM fil Sök väg</span><span class="sxs-lookup"><span data-stu-id="000d5-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000d5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="000d5-129">-ResourceGroupName</span></span>
<span data-ttu-id="000d5-130">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="000d5-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="000d5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="000d5-131">-ResourceId</span></span>
<span data-ttu-id="000d5-132">ID för tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="000d5-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="000d5-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="000d5-133">-Confirm</span></span>
<span data-ttu-id="000d5-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="000d5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="000d5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="000d5-135">-WhatIf</span></span>
<span data-ttu-id="000d5-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="000d5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="000d5-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="000d5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="000d5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="000d5-138">CommonParameters</span></span>
<span data-ttu-id="000d5-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="000d5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="000d5-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="000d5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="000d5-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="000d5-141">INPUTS</span></span>

### <span data-ttu-id="000d5-142">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="000d5-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="000d5-143">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="000d5-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="000d5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="000d5-144">System.String</span></span>

## <span data-ttu-id="000d5-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="000d5-145">OUTPUTS</span></span>

### <span data-ttu-id="000d5-146">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="000d5-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="000d5-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="000d5-147">NOTES</span></span>

## <span data-ttu-id="000d5-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="000d5-148">RELATED LINKS</span></span>
