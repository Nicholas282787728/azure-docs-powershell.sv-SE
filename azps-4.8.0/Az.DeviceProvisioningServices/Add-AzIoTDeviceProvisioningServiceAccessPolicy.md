---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101537"
---
# <span data-ttu-id="58656-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="58656-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="58656-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58656-102">SYNOPSIS</span></span>
<span data-ttu-id="58656-103">Lägga till en ny delad åtkomst princip i etablerings tjänsten för en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="58656-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="58656-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58656-104">SYNTAX</span></span>

### <span data-ttu-id="58656-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="58656-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58656-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="58656-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58656-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="58656-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58656-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58656-108">DESCRIPTION</span></span>
<span data-ttu-id="58656-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="58656-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="58656-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58656-110">EXAMPLES</span></span>

### <span data-ttu-id="58656-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="58656-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="58656-112">Lägga till en ny delad åtkomst policy i en konfigurations tjänst för Azure IoT Hub med EnrollmentWrite-och ServiceConfig-rättigheter.</span><span class="sxs-lookup"><span data-stu-id="58656-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="58656-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="58656-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="58656-114">Lägga till en ny delad åtkomst princip i tjänste etablerings tjänsten för Azure IoT Hub med EnrollmentRead rättighet.</span><span class="sxs-lookup"><span data-stu-id="58656-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="58656-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58656-115">PARAMETERS</span></span>

### <span data-ttu-id="58656-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58656-116">-DefaultProfile</span></span>
<span data-ttu-id="58656-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58656-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58656-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="58656-118">-DpsObject</span></span>
<span data-ttu-id="58656-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="58656-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="58656-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="58656-120">-KeyName</span></span>
<span data-ttu-id="58656-121">IoT enhetens konfigurations princip namn för åtkomst till tjänst</span><span class="sxs-lookup"><span data-stu-id="58656-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="58656-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="58656-122">-Name</span></span>
<span data-ttu-id="58656-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="58656-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="58656-124">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="58656-124">-Permissions</span></span>
<span data-ttu-id="58656-125">Tjänst åtkomst principer för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="58656-125">IoT Device Provisioning Service access policy permissions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ServiceConfig, EnrollmentRead, EnrollmentWrite, DeviceConnect, RegistrationStatusRead, RegistrationStatusWrite

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58656-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58656-126">-ResourceGroupName</span></span>
<span data-ttu-id="58656-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="58656-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="58656-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58656-128">-ResourceId</span></span>
<span data-ttu-id="58656-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="58656-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="58656-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="58656-130">-Confirm</span></span>
<span data-ttu-id="58656-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="58656-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58656-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58656-132">-WhatIf</span></span>
<span data-ttu-id="58656-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="58656-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58656-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="58656-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58656-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58656-135">CommonParameters</span></span>
<span data-ttu-id="58656-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58656-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58656-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58656-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58656-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58656-138">INPUTS</span></span>

### <span data-ttu-id="58656-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="58656-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="58656-140">System. String</span><span class="sxs-lookup"><span data-stu-id="58656-140">System.String</span></span>

## <span data-ttu-id="58656-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58656-141">OUTPUTS</span></span>

### <span data-ttu-id="58656-142">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="58656-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="58656-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58656-143">NOTES</span></span>

## <span data-ttu-id="58656-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58656-144">RELATED LINKS</span></span>
