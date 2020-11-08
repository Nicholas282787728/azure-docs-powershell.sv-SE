---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: ab23988d5594c2285ac8d6eee02b18b0ae4dbf43
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089624"
---
# <span data-ttu-id="6171d-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6171d-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="6171d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6171d-102">SYNOPSIS</span></span>
<span data-ttu-id="6171d-103">Uppdatera en delad åtkomst policy i en Azure IoT Hub-enhet för etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="6171d-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="6171d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6171d-104">SYNTAX</span></span>

### <span data-ttu-id="6171d-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6171d-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6171d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6171d-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6171d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6171d-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6171d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6171d-108">DESCRIPTION</span></span>
<span data-ttu-id="6171d-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="6171d-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="6171d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6171d-110">EXAMPLES</span></span>

### <span data-ttu-id="6171d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6171d-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="6171d-112">Uppdatering av princip "policy" i en konfigurations tjänst för Azure IoT Hub med EnrollmentWrite rättighet.</span><span class="sxs-lookup"><span data-stu-id="6171d-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="6171d-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6171d-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="6171d-114">Uppdatering av princip "policy" i en konfigurations tjänst för Azure IoT Hub med EnrollmentWrite direkt med pipelinen.</span><span class="sxs-lookup"><span data-stu-id="6171d-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="6171d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6171d-115">PARAMETERS</span></span>

### <span data-ttu-id="6171d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6171d-116">-DefaultProfile</span></span>
<span data-ttu-id="6171d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6171d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6171d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6171d-118">-InputObject</span></span>
<span data-ttu-id="6171d-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="6171d-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6171d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6171d-120">-KeyName</span></span>
<span data-ttu-id="6171d-121">IoT enhetens konfigurations princip namn för åtkomst till tjänst</span><span class="sxs-lookup"><span data-stu-id="6171d-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="6171d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="6171d-122">-Name</span></span>
<span data-ttu-id="6171d-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="6171d-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6171d-124">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="6171d-124">-Permissions</span></span>
<span data-ttu-id="6171d-125">Tjänst åtkomst principer för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="6171d-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="6171d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6171d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6171d-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="6171d-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6171d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6171d-128">-ResourceId</span></span>
<span data-ttu-id="6171d-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="6171d-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6171d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6171d-130">-Confirm</span></span>
<span data-ttu-id="6171d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6171d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6171d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6171d-132">-WhatIf</span></span>
<span data-ttu-id="6171d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6171d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6171d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6171d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6171d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6171d-135">CommonParameters</span></span>
<span data-ttu-id="6171d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6171d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6171d-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6171d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6171d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6171d-138">INPUTS</span></span>

### <span data-ttu-id="6171d-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="6171d-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="6171d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6171d-140">System.String</span></span>

## <span data-ttu-id="6171d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6171d-141">OUTPUTS</span></span>

### <span data-ttu-id="6171d-142">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="6171d-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="6171d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6171d-143">NOTES</span></span>

## <span data-ttu-id="6171d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6171d-144">RELATED LINKS</span></span>