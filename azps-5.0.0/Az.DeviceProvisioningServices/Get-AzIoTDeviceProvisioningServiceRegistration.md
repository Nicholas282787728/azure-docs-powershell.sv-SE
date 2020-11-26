---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263240"
---
# <span data-ttu-id="82c85-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="82c85-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="82c85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82c85-102">SYNOPSIS</span></span>
<span data-ttu-id="82c85-103">Hämtar enhetens registrerings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="82c85-103">Gets the device registration state.</span></span>

## <span data-ttu-id="82c85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82c85-104">SYNTAX</span></span>

### <span data-ttu-id="82c85-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="82c85-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82c85-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="82c85-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82c85-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="82c85-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c85-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82c85-108">DESCRIPTION</span></span>
<span data-ttu-id="82c85-109">Skaffa enhetens registrerings tillstånd eller registrerings statusen för enheter under enrollmentGroup i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="82c85-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="82c85-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82c85-110">EXAMPLES</span></span>

### <span data-ttu-id="82c85-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82c85-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="82c85-112">Hämta information om enhetens registrerings tillstånd i en Azure IoT Hub-enhet för etablering.</span><span class="sxs-lookup"><span data-stu-id="82c85-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="82c85-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="82c85-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="82c85-114">Lista alla registrerings statusen för enheter i denna enrollmentGroup.</span><span class="sxs-lookup"><span data-stu-id="82c85-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="82c85-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82c85-115">PARAMETERS</span></span>

### <span data-ttu-id="82c85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c85-116">-DefaultProfile</span></span>
<span data-ttu-id="82c85-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82c85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82c85-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="82c85-118">-DpsName</span></span>
<span data-ttu-id="82c85-119">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="82c85-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="82c85-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="82c85-120">-DpsObject</span></span>
<span data-ttu-id="82c85-121">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="82c85-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="82c85-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="82c85-122">-EnrollmentId</span></span>
<span data-ttu-id="82c85-123">ID för registrerings gruppen.</span><span class="sxs-lookup"><span data-stu-id="82c85-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="82c85-124">-Fråga</span><span class="sxs-lookup"><span data-stu-id="82c85-124">-Query</span></span>
<span data-ttu-id="82c85-125">SQL-fråga.</span><span class="sxs-lookup"><span data-stu-id="82c85-125">Sql query.</span></span>

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

### <span data-ttu-id="82c85-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="82c85-126">-RegistrationId</span></span>
<span data-ttu-id="82c85-127">ID för enhets registrering.</span><span class="sxs-lookup"><span data-stu-id="82c85-127">ID of device registration.</span></span>

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

### <span data-ttu-id="82c85-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c85-128">-ResourceGroupName</span></span>
<span data-ttu-id="82c85-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="82c85-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="82c85-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82c85-130">-ResourceId</span></span>
<span data-ttu-id="82c85-131">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="82c85-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="82c85-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c85-132">CommonParameters</span></span>
<span data-ttu-id="82c85-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c85-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c85-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c85-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c85-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82c85-135">INPUTS</span></span>

### <span data-ttu-id="82c85-136">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="82c85-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="82c85-137">System. String</span><span class="sxs-lookup"><span data-stu-id="82c85-137">System.String</span></span>

## <span data-ttu-id="82c85-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82c85-138">OUTPUTS</span></span>

### <span data-ttu-id="82c85-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="82c85-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="82c85-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates []</span><span class="sxs-lookup"><span data-stu-id="82c85-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="82c85-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82c85-141">NOTES</span></span>

## <span data-ttu-id="82c85-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82c85-142">RELATED LINKS</span></span>