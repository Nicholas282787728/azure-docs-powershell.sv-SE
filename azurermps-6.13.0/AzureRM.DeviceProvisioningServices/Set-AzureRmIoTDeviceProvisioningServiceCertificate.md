---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Set-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Set-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 5132d4c05b49ac4ff41933aa5c157697445cdbe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576281"
---
# <span data-ttu-id="a8cd3-101">Set-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="a8cd3-101">Set-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="a8cd3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="a8cd3-103">Verifiera ett certifikat för etablerings tjänsten för Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="a8cd3-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8cd3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8cd3-104">SYNTAX</span></span>

### <span data-ttu-id="a8cd3-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a8cd3-105">ResourceSet (Default)</span></span>
```
Set-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8cd3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a8cd3-106">InputObjectSet</span></span>
```
Set-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8cd3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a8cd3-107">ResourceIdSet</span></span>
```
Set-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8cd3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8cd3-108">DESCRIPTION</span></span>
<span data-ttu-id="a8cd3-109">Verifiera ett certifikat genom att överföra ett verifierings certifikat som innehåller den verifierings kod som erhålls genom att ringa upp-verifierings kod.</span><span class="sxs-lookup"><span data-stu-id="a8cd3-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="a8cd3-110">Det här är det sista steget i det beskrivna processen.</span><span class="sxs-lookup"><span data-stu-id="a8cd3-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="a8cd3-111">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i konfigurations tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="a8cd3-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="a8cd3-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8cd3-112">EXAMPLES</span></span>

### <span data-ttu-id="a8cd3-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a8cd3-113">Example 1</span></span>
```
PS C:\> Set-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="a8cd3-114">Verifiera ägarskap för den privata knappen "min certifiering".</span><span class="sxs-lookup"><span data-stu-id="a8cd3-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="a8cd3-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a8cd3-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzureRmIoTDpsCertificate -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="a8cd3-116">Verifiera ägarskap för den privata knappen "min certifiering" genom att använda pipeline.</span><span class="sxs-lookup"><span data-stu-id="a8cd3-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="a8cd3-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8cd3-117">PARAMETERS</span></span>

### <span data-ttu-id="a8cd3-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a8cd3-118">-CertificateName</span></span>
<span data-ttu-id="a8cd3-119">Namnet på IoT-enhetens etablerings tjänst certifikat</span><span class="sxs-lookup"><span data-stu-id="a8cd3-119">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cd3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8cd3-120">-DefaultProfile</span></span>
<span data-ttu-id="a8cd3-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8cd3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8cd3-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="a8cd3-122">-Etag</span></span>
<span data-ttu-id="a8cd3-123">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="a8cd3-123">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cd3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8cd3-124">-InputObject</span></span>
<span data-ttu-id="a8cd3-125">Objekt för webb tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="a8cd3-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="a8cd3-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8cd3-126">-Name</span></span>
<span data-ttu-id="a8cd3-127">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="a8cd3-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a8cd3-128">-Path</span><span class="sxs-lookup"><span data-stu-id="a8cd3-128">-Path</span></span>
<span data-ttu-id="a8cd3-129">Base-64-representation av X509-certifikat. cer-fil eller. PEM fil Sök väg</span><span class="sxs-lookup"><span data-stu-id="a8cd3-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="a8cd3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8cd3-130">-ResourceGroupName</span></span>
<span data-ttu-id="a8cd3-131">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="a8cd3-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a8cd3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8cd3-132">-ResourceId</span></span>
<span data-ttu-id="a8cd3-133">ID för tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="a8cd3-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="a8cd3-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8cd3-134">-Confirm</span></span>
<span data-ttu-id="a8cd3-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8cd3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8cd3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8cd3-136">-WhatIf</span></span>
<span data-ttu-id="a8cd3-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8cd3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8cd3-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8cd3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8cd3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8cd3-139">CommonParameters</span></span>
<span data-ttu-id="a8cd3-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8cd3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8cd3-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8cd3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8cd3-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8cd3-142">INPUTS</span></span>

### <span data-ttu-id="a8cd3-143">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="a8cd3-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="a8cd3-144">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a8cd3-144">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a8cd3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a8cd3-145">System.String</span></span>

## <span data-ttu-id="a8cd3-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8cd3-146">OUTPUTS</span></span>

### <span data-ttu-id="a8cd3-147">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="a8cd3-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="a8cd3-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8cd3-148">NOTES</span></span>

## <span data-ttu-id="a8cd3-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8cd3-149">RELATED LINKS</span></span>
