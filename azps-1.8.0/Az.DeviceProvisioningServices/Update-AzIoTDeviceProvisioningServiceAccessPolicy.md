---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 2da931326b9f900dbf3af3cfcb2e504b413cef33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754134"
---
# <span data-ttu-id="10bae-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="10bae-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="10bae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10bae-102">SYNOPSIS</span></span>
<span data-ttu-id="10bae-103">Uppdatera en delad åtkomst policy i en Azure IoT Hub-enhet för etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="10bae-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="10bae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10bae-104">SYNTAX</span></span>

### <span data-ttu-id="10bae-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="10bae-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10bae-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="10bae-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10bae-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="10bae-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10bae-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10bae-108">DESCRIPTION</span></span>
<span data-ttu-id="10bae-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="10bae-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="10bae-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10bae-110">EXAMPLES</span></span>

### <span data-ttu-id="10bae-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="10bae-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="10bae-112">Uppdatering av princip "policy" i en konfigurations tjänst för Azure IoT Hub med EnrollmentWrite rättighet.</span><span class="sxs-lookup"><span data-stu-id="10bae-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="10bae-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="10bae-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="10bae-114">Uppdatering av princip "policy" i en konfigurations tjänst för Azure IoT Hub med EnrollmentWrite direkt med pipelinen.</span><span class="sxs-lookup"><span data-stu-id="10bae-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="10bae-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10bae-115">PARAMETERS</span></span>

### <span data-ttu-id="10bae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10bae-116">-DefaultProfile</span></span>
<span data-ttu-id="10bae-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10bae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10bae-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10bae-118">-InputObject</span></span>
<span data-ttu-id="10bae-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="10bae-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="10bae-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="10bae-120">-KeyName</span></span>
<span data-ttu-id="10bae-121">IoT enhetens konfigurations princip namn för åtkomst till tjänst</span><span class="sxs-lookup"><span data-stu-id="10bae-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="10bae-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="10bae-122">-Name</span></span>
<span data-ttu-id="10bae-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="10bae-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="10bae-124">-Behörigheter</span><span class="sxs-lookup"><span data-stu-id="10bae-124">-Permissions</span></span>
<span data-ttu-id="10bae-125">Tjänst åtkomst principer för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="10bae-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="10bae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10bae-126">-ResourceGroupName</span></span>
<span data-ttu-id="10bae-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="10bae-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="10bae-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10bae-128">-ResourceId</span></span>
<span data-ttu-id="10bae-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="10bae-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="10bae-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10bae-130">-Confirm</span></span>
<span data-ttu-id="10bae-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10bae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10bae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10bae-132">-WhatIf</span></span>
<span data-ttu-id="10bae-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10bae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10bae-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10bae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10bae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10bae-135">CommonParameters</span></span>
<span data-ttu-id="10bae-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10bae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10bae-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10bae-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10bae-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10bae-138">INPUTS</span></span>

### <span data-ttu-id="10bae-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="10bae-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="10bae-140">System. String</span><span class="sxs-lookup"><span data-stu-id="10bae-140">System.String</span></span>

## <span data-ttu-id="10bae-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10bae-141">OUTPUTS</span></span>

### <span data-ttu-id="10bae-142">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="10bae-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="10bae-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10bae-143">NOTES</span></span>

## <span data-ttu-id="10bae-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10bae-144">RELATED LINKS</span></span>
