---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102886"
---
# <span data-ttu-id="1758c-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="1758c-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="1758c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1758c-102">SYNOPSIS</span></span>
<span data-ttu-id="1758c-103">Hämtar enhetens registrerings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="1758c-103">Gets the device registration state.</span></span>

## <span data-ttu-id="1758c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1758c-104">SYNTAX</span></span>

### <span data-ttu-id="1758c-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1758c-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1758c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1758c-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1758c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1758c-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1758c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1758c-108">DESCRIPTION</span></span>
<span data-ttu-id="1758c-109">Skaffa enhetens registrerings tillstånd eller registrerings statusen för enheter under enrollmentGroup i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="1758c-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="1758c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1758c-110">EXAMPLES</span></span>

### <span data-ttu-id="1758c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1758c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="1758c-112">Hämta information om enhetens registrerings tillstånd i en Azure IoT Hub-enhet för etablering.</span><span class="sxs-lookup"><span data-stu-id="1758c-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="1758c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1758c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="1758c-114">Lista alla registrerings statusen för enheter i denna enrollmentGroup.</span><span class="sxs-lookup"><span data-stu-id="1758c-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="1758c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1758c-115">PARAMETERS</span></span>

### <span data-ttu-id="1758c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1758c-116">-DefaultProfile</span></span>
<span data-ttu-id="1758c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1758c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1758c-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="1758c-118">-DpsName</span></span>
<span data-ttu-id="1758c-119">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="1758c-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1758c-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="1758c-120">-DpsObject</span></span>
<span data-ttu-id="1758c-121">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="1758c-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1758c-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="1758c-122">-EnrollmentId</span></span>
<span data-ttu-id="1758c-123">ID för registrerings gruppen.</span><span class="sxs-lookup"><span data-stu-id="1758c-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="1758c-124">-Fråga</span><span class="sxs-lookup"><span data-stu-id="1758c-124">-Query</span></span>
<span data-ttu-id="1758c-125">SQL-fråga.</span><span class="sxs-lookup"><span data-stu-id="1758c-125">Sql query.</span></span>

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

### <span data-ttu-id="1758c-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="1758c-126">-RegistrationId</span></span>
<span data-ttu-id="1758c-127">ID för enhets registrering.</span><span class="sxs-lookup"><span data-stu-id="1758c-127">ID of device registration.</span></span>

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

### <span data-ttu-id="1758c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1758c-128">-ResourceGroupName</span></span>
<span data-ttu-id="1758c-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="1758c-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1758c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1758c-130">-ResourceId</span></span>
<span data-ttu-id="1758c-131">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="1758c-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1758c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1758c-132">CommonParameters</span></span>
<span data-ttu-id="1758c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1758c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1758c-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1758c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1758c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1758c-135">INPUTS</span></span>

### <span data-ttu-id="1758c-136">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1758c-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1758c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1758c-137">System.String</span></span>

## <span data-ttu-id="1758c-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1758c-138">OUTPUTS</span></span>

### <span data-ttu-id="1758c-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="1758c-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="1758c-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates []</span><span class="sxs-lookup"><span data-stu-id="1758c-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="1758c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1758c-141">NOTES</span></span>

## <span data-ttu-id="1758c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1758c-142">RELATED LINKS</span></span>
