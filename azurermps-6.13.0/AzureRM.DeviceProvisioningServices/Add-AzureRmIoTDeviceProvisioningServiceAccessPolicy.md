---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 23d9e40fe6d25fbd2a6bb3e23959d1a4bf087af2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582692"
---
# <span data-ttu-id="43776-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43776-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="43776-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43776-102">SYNOPSIS</span></span>
<span data-ttu-id="43776-103">Lägga till en ny delad åtkomst princip i etablerings tjänsten för en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="43776-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43776-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43776-104">SYNTAX</span></span>

### <span data-ttu-id="43776-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="43776-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43776-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="43776-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43776-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="43776-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43776-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43776-108">DESCRIPTION</span></span>
<span data-ttu-id="43776-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="43776-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="43776-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43776-110">EXAMPLES</span></span>

### <span data-ttu-id="43776-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="43776-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="43776-112">Lägga till en ny delad åtkomst policy i en konfigurations tjänst för Azure IoT Hub med EnrollmentWrite-och ServiceConfig-rättigheter.</span><span class="sxs-lookup"><span data-stu-id="43776-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="43776-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="43776-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="43776-114">Lägga till en ny delad åtkomst princip i tjänste etablerings tjänsten för Azure IoT Hub med EnrollmentRead rättighet.</span><span class="sxs-lookup"><span data-stu-id="43776-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="43776-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43776-115">PARAMETERS</span></span>

### <span data-ttu-id="43776-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43776-116">-DefaultProfile</span></span>
<span data-ttu-id="43776-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43776-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43776-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="43776-118">-DpsObject</span></span>
<span data-ttu-id="43776-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="43776-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="43776-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="43776-120">-KeyName</span></span>
<span data-ttu-id="43776-121">IoT enhetens konfigurations princip namn för åtkomst till tjänst</span><span class="sxs-lookup"><span data-stu-id="43776-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="43776-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="43776-122">-Name</span></span>
<span data-ttu-id="43776-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="43776-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="43776-124">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="43776-124">-Permissions</span></span>
<span data-ttu-id="43776-125">Tjänst åtkomst principer för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="43776-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="43776-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43776-126">-ResourceGroupName</span></span>
<span data-ttu-id="43776-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="43776-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="43776-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43776-128">-ResourceId</span></span>
<span data-ttu-id="43776-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="43776-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="43776-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43776-130">-Confirm</span></span>
<span data-ttu-id="43776-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43776-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43776-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43776-132">-WhatIf</span></span>
<span data-ttu-id="43776-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43776-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43776-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43776-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43776-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43776-135">CommonParameters</span></span>
<span data-ttu-id="43776-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43776-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43776-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43776-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43776-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43776-138">INPUTS</span></span>

### <span data-ttu-id="43776-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="43776-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="43776-140">Parametrar: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43776-140">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="43776-141">System. String</span><span class="sxs-lookup"><span data-stu-id="43776-141">System.String</span></span>

## <span data-ttu-id="43776-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43776-142">OUTPUTS</span></span>

### <span data-ttu-id="43776-143">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="43776-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="43776-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43776-144">NOTES</span></span>

## <span data-ttu-id="43776-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43776-145">RELATED LINKS</span></span>
