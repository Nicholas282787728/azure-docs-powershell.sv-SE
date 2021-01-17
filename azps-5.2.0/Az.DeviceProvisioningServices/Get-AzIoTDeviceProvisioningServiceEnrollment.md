---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390501"
---
# <span data-ttu-id="4ce2b-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="4ce2b-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="4ce2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ce2b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce2b-103">Skaffa en enhets registrerings post.</span><span class="sxs-lookup"><span data-stu-id="4ce2b-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="4ce2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ce2b-104">SYNTAX</span></span>

### <span data-ttu-id="4ce2b-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4ce2b-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ce2b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ce2b-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ce2b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ce2b-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ce2b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ce2b-108">DESCRIPTION</span></span>
<span data-ttu-id="4ce2b-109">Få information om enhets registrering eller registrering av list enheter i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="4ce2b-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4ce2b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ce2b-110">EXAMPLES</span></span>

### <span data-ttu-id="4ce2b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4ce2b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="4ce2b-112">Få information om enhets registrering i en Azure IoT Hub-enhet för etablering.</span><span class="sxs-lookup"><span data-stu-id="4ce2b-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="4ce2b-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4ce2b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="4ce2b-114">Visa enhets registreringar i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="4ce2b-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4ce2b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ce2b-115">PARAMETERS</span></span>

### <span data-ttu-id="4ce2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce2b-116">-DefaultProfile</span></span>
<span data-ttu-id="4ce2b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce2b-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="4ce2b-118">-DpsName</span></span>
<span data-ttu-id="4ce2b-119">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="4ce2b-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4ce2b-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4ce2b-120">-DpsObject</span></span>
<span data-ttu-id="4ce2b-121">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="4ce2b-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4ce2b-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="4ce2b-122">-RegistrationId</span></span>
<span data-ttu-id="4ce2b-123">Registrerings-ID för individuell registrering.</span><span class="sxs-lookup"><span data-stu-id="4ce2b-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="4ce2b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce2b-124">-ResourceGroupName</span></span>
<span data-ttu-id="4ce2b-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="4ce2b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4ce2b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce2b-126">-ResourceId</span></span>
<span data-ttu-id="4ce2b-127">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="4ce2b-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4ce2b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce2b-128">CommonParameters</span></span>
<span data-ttu-id="4ce2b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce2b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce2b-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce2b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce2b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ce2b-131">INPUTS</span></span>

### <span data-ttu-id="4ce2b-132">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4ce2b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4ce2b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4ce2b-133">System.String</span></span>

## <span data-ttu-id="4ce2b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ce2b-134">OUTPUTS</span></span>

### <span data-ttu-id="4ce2b-135">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="4ce2b-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="4ce2b-136">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollments []</span><span class="sxs-lookup"><span data-stu-id="4ce2b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="4ce2b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ce2b-137">NOTES</span></span>

## <span data-ttu-id="4ce2b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ce2b-138">RELATED LINKS</span></span>
