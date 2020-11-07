---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f978e6c0a496273535551663a442989b2ab1648e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754157"
---
# <span data-ttu-id="099a7-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="099a7-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="099a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="099a7-102">SYNOPSIS</span></span>
<span data-ttu-id="099a7-103">Lista alla eller Visa information om delade åtkomst principer i tjänste etablerings tjänsten för Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="099a7-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="099a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="099a7-104">SYNTAX</span></span>

### <span data-ttu-id="099a7-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="099a7-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="099a7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="099a7-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="099a7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="099a7-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="099a7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="099a7-108">DESCRIPTION</span></span>
<span data-ttu-id="099a7-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="099a7-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="099a7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="099a7-110">EXAMPLES</span></span>

### <span data-ttu-id="099a7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="099a7-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="099a7-112">Visa alla delade åtkomst principer i "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="099a7-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="099a7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="099a7-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="099a7-114">Visa information om principen för delad åtkomst "policy" i en tjänste etablerings tjänst för Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="099a7-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="099a7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="099a7-115">PARAMETERS</span></span>

### <span data-ttu-id="099a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="099a7-116">-DefaultProfile</span></span>
<span data-ttu-id="099a7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="099a7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="099a7-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="099a7-118">-DpsObject</span></span>
<span data-ttu-id="099a7-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="099a7-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="099a7-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="099a7-120">-KeyName</span></span>
<span data-ttu-id="099a7-121">IoT enhetens konfigurations princip namn för åtkomst till tjänst</span><span class="sxs-lookup"><span data-stu-id="099a7-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="099a7-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="099a7-122">-Name</span></span>
<span data-ttu-id="099a7-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="099a7-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="099a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="099a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="099a7-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="099a7-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="099a7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="099a7-126">-ResourceId</span></span>
<span data-ttu-id="099a7-127">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="099a7-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="099a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="099a7-128">CommonParameters</span></span>
<span data-ttu-id="099a7-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="099a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="099a7-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="099a7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="099a7-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="099a7-131">INPUTS</span></span>

### <span data-ttu-id="099a7-132">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="099a7-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="099a7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="099a7-133">System.String</span></span>

## <span data-ttu-id="099a7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="099a7-134">OUTPUTS</span></span>

### <span data-ttu-id="099a7-135">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="099a7-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="099a7-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="099a7-136">NOTES</span></span>

## <span data-ttu-id="099a7-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="099a7-137">RELATED LINKS</span></span>
