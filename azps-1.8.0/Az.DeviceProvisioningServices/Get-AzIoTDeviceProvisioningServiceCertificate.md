---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: ab7d28c80f87eaf0220ead80e2c7fd76d3d2483b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754156"
---
# <span data-ttu-id="2647c-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="2647c-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="2647c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2647c-102">SYNOPSIS</span></span>
<span data-ttu-id="2647c-103">Visar en lista över alla certifikat eller ett visst certifikat som ingår i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="2647c-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2647c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2647c-104">SYNTAX</span></span>

### <span data-ttu-id="2647c-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2647c-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2647c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2647c-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2647c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2647c-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2647c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2647c-108">DESCRIPTION</span></span>
<span data-ttu-id="2647c-109">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i konfigurations tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="2647c-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="2647c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2647c-110">EXAMPLES</span></span>

### <span data-ttu-id="2647c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2647c-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

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

<span data-ttu-id="2647c-112">Visa information om "certifikatet" i en konfigurations tjänst för en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="2647c-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="2647c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2647c-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="2647c-114">Lista alla certifikat i "myiotdps" med pipeline.</span><span class="sxs-lookup"><span data-stu-id="2647c-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="2647c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2647c-115">PARAMETERS</span></span>

### <span data-ttu-id="2647c-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2647c-116">-CertificateName</span></span>
<span data-ttu-id="2647c-117">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="2647c-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="2647c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2647c-118">-DefaultProfile</span></span>
<span data-ttu-id="2647c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2647c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2647c-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2647c-120">-DpsObject</span></span>
<span data-ttu-id="2647c-121">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="2647c-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2647c-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="2647c-122">-Name</span></span>
<span data-ttu-id="2647c-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="2647c-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2647c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2647c-124">-ResourceGroupName</span></span>
<span data-ttu-id="2647c-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="2647c-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2647c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2647c-126">-ResourceId</span></span>
<span data-ttu-id="2647c-127">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="2647c-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2647c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2647c-128">CommonParameters</span></span>
<span data-ttu-id="2647c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2647c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2647c-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2647c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2647c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2647c-131">INPUTS</span></span>

### <span data-ttu-id="2647c-132">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2647c-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2647c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2647c-133">System.String</span></span>

## <span data-ttu-id="2647c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2647c-134">OUTPUTS</span></span>

### <span data-ttu-id="2647c-135">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="2647c-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="2647c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2647c-136">NOTES</span></span>

## <span data-ttu-id="2647c-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2647c-137">RELATED LINKS</span></span>
