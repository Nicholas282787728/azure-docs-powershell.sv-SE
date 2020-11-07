---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 1efd429489be41f619454fd2b772c7cbb1ebc5c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744305"
---
# <span data-ttu-id="b5c0e-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b5c0e-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="b5c0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c0e-103">Ta bort delade åtkomst principer i en Azure IoT Hub-enhet för etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b5c0e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5c0e-104">SYNTAX</span></span>

### <span data-ttu-id="b5c0e-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b5c0e-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5c0e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b5c0e-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c0e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b5c0e-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5c0e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5c0e-108">DESCRIPTION</span></span>
<span data-ttu-id="b5c0e-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="b5c0e-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b5c0e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5c0e-110">EXAMPLES</span></span>

### <span data-ttu-id="b5c0e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b5c0e-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="b5c0e-112">Ta bort principen "policy" för delad åtkomst i en konfigurations tjänst för en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="b5c0e-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b5c0e-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="b5c0e-114">Ta bort principen "policy" för delad åtkomst i en tjänste etablerings tjänst från en Azure IoT Hub-enhet med pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="b5c0e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5c0e-115">PARAMETERS</span></span>

### <span data-ttu-id="b5c0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c0e-116">-DefaultProfile</span></span>
<span data-ttu-id="b5c0e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5c0e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5c0e-118">-InputObject</span></span>
<span data-ttu-id="b5c0e-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="b5c0e-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="b5c0e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5c0e-120">-KeyName</span></span>
<span data-ttu-id="b5c0e-121">IoT enhetens konfigurations princip namn för åtkomst till tjänst</span><span class="sxs-lookup"><span data-stu-id="b5c0e-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="b5c0e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5c0e-122">-Name</span></span>
<span data-ttu-id="b5c0e-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="b5c0e-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b5c0e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5c0e-124">-PassThru</span></span>
<span data-ttu-id="b5c0e-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b5c0e-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c0e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c0e-126">-ResourceGroupName</span></span>
<span data-ttu-id="b5c0e-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="b5c0e-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b5c0e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c0e-128">-ResourceId</span></span>
<span data-ttu-id="b5c0e-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="b5c0e-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b5c0e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5c0e-130">-Confirm</span></span>
<span data-ttu-id="b5c0e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5c0e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5c0e-132">-WhatIf</span></span>
<span data-ttu-id="b5c0e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5c0e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5c0e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c0e-135">CommonParameters</span></span>
<span data-ttu-id="b5c0e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c0e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c0e-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c0e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c0e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5c0e-138">INPUTS</span></span>

### <span data-ttu-id="b5c0e-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="b5c0e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="b5c0e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b5c0e-140">System.String</span></span>

## <span data-ttu-id="b5c0e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5c0e-141">OUTPUTS</span></span>

### <span data-ttu-id="b5c0e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5c0e-142">System.Boolean</span></span>

## <span data-ttu-id="b5c0e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5c0e-143">NOTES</span></span>

## <span data-ttu-id="b5c0e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5c0e-144">RELATED LINKS</span></span>