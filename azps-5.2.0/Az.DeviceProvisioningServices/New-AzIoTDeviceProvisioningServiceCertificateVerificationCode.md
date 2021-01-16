---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390486"
---
# <span data-ttu-id="54c66-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="54c66-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="54c66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54c66-102">SYNOPSIS</span></span>
<span data-ttu-id="54c66-103">Skapa en verifierings kod för ett certifikat för etablerings tjänsten för Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="54c66-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="54c66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54c66-104">SYNTAX</span></span>

### <span data-ttu-id="54c66-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="54c66-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54c66-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="54c66-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54c66-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="54c66-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c66-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54c66-108">DESCRIPTION</span></span>
<span data-ttu-id="54c66-109">Den här verifierings koden används för att slutföra beviset för en besittning för ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="54c66-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="54c66-110">Använd den här verifierings koden som CN för ett nytt certifikat som är signerat med rot certifikatets privata nycklar.</span><span class="sxs-lookup"><span data-stu-id="54c66-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="54c66-111">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i konfigurations tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="54c66-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="54c66-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54c66-112">EXAMPLES</span></span>

### <span data-ttu-id="54c66-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54c66-113">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="54c66-114">Skapa en verifierings kod för "certifikatet".</span><span class="sxs-lookup"><span data-stu-id="54c66-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="54c66-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="54c66-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzIoTDpsCVC

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="54c66-116">Skapa en verifierings kod för "certifikatet" med pipeline.</span><span class="sxs-lookup"><span data-stu-id="54c66-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="54c66-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54c66-117">PARAMETERS</span></span>

### <span data-ttu-id="54c66-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="54c66-118">-CertificateName</span></span>
<span data-ttu-id="54c66-119">Namnet på IoT-enhetens etablerings tjänst certifikat</span><span class="sxs-lookup"><span data-stu-id="54c66-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="54c66-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c66-120">-DefaultProfile</span></span>
<span data-ttu-id="54c66-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54c66-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c66-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="54c66-122">-Etag</span></span>
<span data-ttu-id="54c66-123">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="54c66-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="54c66-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54c66-124">-InputObject</span></span>
<span data-ttu-id="54c66-125">Objekt för webb tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="54c66-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="54c66-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="54c66-126">-Name</span></span>
<span data-ttu-id="54c66-127">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="54c66-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="54c66-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c66-128">-ResourceGroupName</span></span>
<span data-ttu-id="54c66-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="54c66-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="54c66-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54c66-130">-ResourceId</span></span>
<span data-ttu-id="54c66-131">ID för tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="54c66-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="54c66-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54c66-132">-Confirm</span></span>
<span data-ttu-id="54c66-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54c66-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c66-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c66-134">-WhatIf</span></span>
<span data-ttu-id="54c66-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54c66-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c66-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54c66-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c66-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c66-137">CommonParameters</span></span>
<span data-ttu-id="54c66-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c66-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c66-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54c66-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c66-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54c66-140">INPUTS</span></span>

### <span data-ttu-id="54c66-141">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="54c66-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="54c66-142">System. String</span><span class="sxs-lookup"><span data-stu-id="54c66-142">System.String</span></span>

## <span data-ttu-id="54c66-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54c66-143">OUTPUTS</span></span>

### <span data-ttu-id="54c66-144">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="54c66-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="54c66-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54c66-145">NOTES</span></span>

## <span data-ttu-id="54c66-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54c66-146">RELATED LINKS</span></span>
