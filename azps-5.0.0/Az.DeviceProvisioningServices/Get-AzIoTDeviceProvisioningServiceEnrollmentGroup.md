---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263241"
---
# <span data-ttu-id="a14c1-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="a14c1-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="a14c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a14c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a14c1-103">Skaffa en enhets registrerings grupp.</span><span class="sxs-lookup"><span data-stu-id="a14c1-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="a14c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a14c1-104">SYNTAX</span></span>

### <span data-ttu-id="a14c1-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a14c1-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a14c1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a14c1-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a14c1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a14c1-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a14c1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a14c1-108">DESCRIPTION</span></span>
<span data-ttu-id="a14c1-109">Få information om en registrerings grupp eller lista alla registrerings grupper i en Azure IoT Hub-enhets etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="a14c1-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="a14c1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a14c1-110">EXAMPLES</span></span>

### <span data-ttu-id="a14c1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a14c1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="a14c1-112">Skaffa en enhets registrerings grupp i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="a14c1-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="a14c1-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a14c1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="a14c1-114">Lista alla enheter för registrerings grupper i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="a14c1-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="a14c1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a14c1-115">PARAMETERS</span></span>

### <span data-ttu-id="a14c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14c1-116">-DefaultProfile</span></span>
<span data-ttu-id="a14c1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a14c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a14c1-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="a14c1-118">-DpsName</span></span>
<span data-ttu-id="a14c1-119">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="a14c1-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a14c1-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a14c1-120">-DpsObject</span></span>
<span data-ttu-id="a14c1-121">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="a14c1-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a14c1-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="a14c1-122">-Name</span></span>
<span data-ttu-id="a14c1-123">Namn på registrerings gruppen.</span><span class="sxs-lookup"><span data-stu-id="a14c1-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="a14c1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a14c1-124">-ResourceGroupName</span></span>
<span data-ttu-id="a14c1-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="a14c1-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a14c1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a14c1-126">-ResourceId</span></span>
<span data-ttu-id="a14c1-127">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="a14c1-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a14c1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14c1-128">CommonParameters</span></span>
<span data-ttu-id="a14c1-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a14c1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14c1-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a14c1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14c1-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a14c1-131">INPUTS</span></span>

### <span data-ttu-id="a14c1-132">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a14c1-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="a14c1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a14c1-133">System.String</span></span>

## <span data-ttu-id="a14c1-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a14c1-134">OUTPUTS</span></span>

### <span data-ttu-id="a14c1-135">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="a14c1-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="a14c1-136">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroups []</span><span class="sxs-lookup"><span data-stu-id="a14c1-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="a14c1-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a14c1-137">NOTES</span></span>

## <span data-ttu-id="a14c1-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a14c1-138">RELATED LINKS</span></span>
