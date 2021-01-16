---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: aa51001163e4559dd0d3ef7edfb48abd3448c0b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398443"
---
# <span data-ttu-id="03677-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="03677-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="03677-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03677-102">SYNOPSIS</span></span>
<span data-ttu-id="03677-103">Visar en lista över alla certifikat eller ett visst certifikat som ingår i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="03677-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="03677-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03677-104">SYNTAX</span></span>

### <span data-ttu-id="03677-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="03677-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03677-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="03677-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03677-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="03677-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03677-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03677-108">DESCRIPTION</span></span>
<span data-ttu-id="03677-109">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i konfigurations tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="03677-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="03677-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03677-110">EXAMPLES</span></span>

### <span data-ttu-id="03677-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="03677-111">Example 1</span></span>
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

<span data-ttu-id="03677-112">Visa information om "certifikatet" i en konfigurations tjänst för en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="03677-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="03677-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="03677-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="03677-114">Lista alla certifikat i "myiotdps" med pipeline.</span><span class="sxs-lookup"><span data-stu-id="03677-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="03677-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03677-115">PARAMETERS</span></span>

### <span data-ttu-id="03677-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="03677-116">-CertificateName</span></span>
<span data-ttu-id="03677-117">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="03677-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="03677-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03677-118">-DefaultProfile</span></span>
<span data-ttu-id="03677-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03677-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03677-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="03677-120">-DpsObject</span></span>
<span data-ttu-id="03677-121">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="03677-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="03677-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="03677-122">-Name</span></span>
<span data-ttu-id="03677-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="03677-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="03677-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03677-124">-ResourceGroupName</span></span>
<span data-ttu-id="03677-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="03677-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="03677-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03677-126">-ResourceId</span></span>
<span data-ttu-id="03677-127">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="03677-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="03677-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03677-128">CommonParameters</span></span>
<span data-ttu-id="03677-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03677-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03677-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03677-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03677-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03677-131">INPUTS</span></span>

### <span data-ttu-id="03677-132">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="03677-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="03677-133">System. String</span><span class="sxs-lookup"><span data-stu-id="03677-133">System.String</span></span>

## <span data-ttu-id="03677-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03677-134">OUTPUTS</span></span>

### <span data-ttu-id="03677-135">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="03677-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="03677-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03677-136">NOTES</span></span>

## <span data-ttu-id="03677-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03677-137">RELATED LINKS</span></span>
