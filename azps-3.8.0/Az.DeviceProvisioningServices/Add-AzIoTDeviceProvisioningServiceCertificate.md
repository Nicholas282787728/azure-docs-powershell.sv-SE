---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090114"
---
# <span data-ttu-id="b5b56-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="b5b56-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="b5b56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5b56-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b56-103">Skapa/uppdatera ett certifikat för konfiguration av en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="b5b56-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="b5b56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5b56-104">SYNTAX</span></span>

### <span data-ttu-id="b5b56-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b5b56-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5b56-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b5b56-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5b56-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b5b56-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5b56-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5b56-108">DESCRIPTION</span></span>
<span data-ttu-id="b5b56-109">Uppladdar ett nytt certifikat eller ersätter det befintliga certifikatet med samma namn.</span><span class="sxs-lookup"><span data-stu-id="b5b56-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="b5b56-110">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i konfigurations tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="b5b56-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="b5b56-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5b56-111">EXAMPLES</span></span>

### <span data-ttu-id="b5b56-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b5b56-112">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

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

<span data-ttu-id="b5b56-113">Ladda upp en CER-fil för CA-certifikat till en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="b5b56-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="b5b56-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b5b56-114">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

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

<span data-ttu-id="b5b56-115">Uppdaterar ett CERTIFIKATUTFÄRDARCERTIFIKAT i en IoT Hub-enhets etablerings tjänst genom att överföra en ny CER-fil.</span><span class="sxs-lookup"><span data-stu-id="b5b56-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="b5b56-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5b56-116">PARAMETERS</span></span>

### <span data-ttu-id="b5b56-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b5b56-117">-CertificateName</span></span>
<span data-ttu-id="b5b56-118">Namnet på IoT-enhetens etablerings tjänst certifikat</span><span class="sxs-lookup"><span data-stu-id="b5b56-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="b5b56-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b56-119">-DefaultProfile</span></span>
<span data-ttu-id="b5b56-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b56-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5b56-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="b5b56-121">-Etag</span></span>
<span data-ttu-id="b5b56-122">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="b5b56-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="b5b56-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5b56-123">-InputObject</span></span>
<span data-ttu-id="b5b56-124">Objekt för webb tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="b5b56-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="b5b56-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5b56-125">-Name</span></span>
<span data-ttu-id="b5b56-126">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="b5b56-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b5b56-127">-Path</span><span class="sxs-lookup"><span data-stu-id="b5b56-127">-Path</span></span>
<span data-ttu-id="b5b56-128">Base-64-representation av X509-certifikat. cer-fil eller. PEM fil Sök väg</span><span class="sxs-lookup"><span data-stu-id="b5b56-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="b5b56-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b56-129">-ResourceGroupName</span></span>
<span data-ttu-id="b5b56-130">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="b5b56-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b5b56-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5b56-131">-ResourceId</span></span>
<span data-ttu-id="b5b56-132">ID för tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="b5b56-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="b5b56-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5b56-133">-Confirm</span></span>
<span data-ttu-id="b5b56-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5b56-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5b56-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5b56-135">-WhatIf</span></span>
<span data-ttu-id="b5b56-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5b56-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5b56-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5b56-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5b56-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b56-138">CommonParameters</span></span>
<span data-ttu-id="b5b56-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b56-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b56-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b56-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b56-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5b56-141">INPUTS</span></span>

### <span data-ttu-id="b5b56-142">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="b5b56-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="b5b56-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b5b56-143">System.String</span></span>

## <span data-ttu-id="b5b56-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5b56-144">OUTPUTS</span></span>

### <span data-ttu-id="b5b56-145">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="b5b56-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="b5b56-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5b56-146">NOTES</span></span>

## <span data-ttu-id="b5b56-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5b56-147">RELATED LINKS</span></span>
