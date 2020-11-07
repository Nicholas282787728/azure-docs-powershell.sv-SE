---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f5d750dc795619f32f6c4f16a5fe1e3b5e111106
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757890"
---
# <span data-ttu-id="ca9ab-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca9ab-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="ca9ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9ab-103">Uppdatera en delad åtkomst policy i en Azure IoT Hub-enhet för etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca9ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca9ab-104">SYNTAX</span></span>

### <span data-ttu-id="ca9ab-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ca9ab-105">ResourceSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca9ab-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca9ab-106">InputObjectSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca9ab-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca9ab-107">ResourceIdSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca9ab-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca9ab-108">DESCRIPTION</span></span>
<span data-ttu-id="ca9ab-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="ca9ab-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ca9ab-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca9ab-110">EXAMPLES</span></span>

### <span data-ttu-id="ca9ab-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ca9ab-111">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="ca9ab-112">Uppdatering av princip "policy" i en konfigurations tjänst för Azure IoT Hub med EnrollmentWrite rättighet.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="ca9ab-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ca9ab-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzureRmIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="ca9ab-114">Uppdatering av princip "policy" i en konfigurations tjänst för Azure IoT Hub med EnrollmentWrite direkt med pipelinen.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="ca9ab-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca9ab-115">PARAMETERS</span></span>

### <span data-ttu-id="ca9ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9ab-116">-DefaultProfile</span></span>
<span data-ttu-id="ca9ab-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca9ab-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca9ab-118">-InputObject</span></span>
<span data-ttu-id="ca9ab-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="ca9ab-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9ab-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca9ab-120">-KeyName</span></span>
<span data-ttu-id="ca9ab-121">IoT enhetens konfigurations princip namn för åtkomst till tjänst</span><span class="sxs-lookup"><span data-stu-id="ca9ab-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="ca9ab-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca9ab-122">-Name</span></span>
<span data-ttu-id="ca9ab-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="ca9ab-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ca9ab-124">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="ca9ab-124">-Permissions</span></span>
<span data-ttu-id="ca9ab-125">Tjänst åtkomst principer för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="ca9ab-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="ca9ab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9ab-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca9ab-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="ca9ab-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ca9ab-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca9ab-128">-ResourceId</span></span>
<span data-ttu-id="ca9ab-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="ca9ab-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ca9ab-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ca9ab-130">-Confirm</span></span>
<span data-ttu-id="ca9ab-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca9ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca9ab-132">-WhatIf</span></span>
<span data-ttu-id="ca9ab-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca9ab-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca9ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9ab-135">CommonParameters</span></span>
<span data-ttu-id="ca9ab-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9ab-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9ab-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9ab-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca9ab-138">INPUTS</span></span>

### <span data-ttu-id="ca9ab-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="ca9ab-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="ca9ab-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ca9ab-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ca9ab-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ca9ab-141">System.String</span></span>

## <span data-ttu-id="ca9ab-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca9ab-142">OUTPUTS</span></span>

### <span data-ttu-id="ca9ab-143">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="ca9ab-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="ca9ab-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca9ab-144">NOTES</span></span>

## <span data-ttu-id="ca9ab-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca9ab-145">RELATED LINKS</span></span>
