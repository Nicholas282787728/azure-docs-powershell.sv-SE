---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: b3a813623ed11a64a23dc35afe2f81c3f5de61da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580111"
---
# <span data-ttu-id="5ea0d-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5ea0d-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="5ea0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ea0d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea0d-103">Ta bort delade åtkomst principer i en Azure IoT Hub-enhet för etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ea0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ea0d-104">SYNTAX</span></span>

### <span data-ttu-id="5ea0d-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5ea0d-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ea0d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5ea0d-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ea0d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5ea0d-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ea0d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ea0d-108">DESCRIPTION</span></span>
<span data-ttu-id="5ea0d-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5ea0d-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5ea0d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ea0d-110">EXAMPLES</span></span>

### <span data-ttu-id="5ea0d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5ea0d-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="5ea0d-112">Ta bort principen "policy" för delad åtkomst i en konfigurations tjänst för en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="5ea0d-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5ea0d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzureRmIoTDpsAccessPolicy
```

<span data-ttu-id="5ea0d-114">Ta bort principen "policy" för delad åtkomst i en tjänste etablerings tjänst från en Azure IoT Hub-enhet med pipeline.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="5ea0d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ea0d-115">PARAMETERS</span></span>

### <span data-ttu-id="5ea0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea0d-116">-DefaultProfile</span></span>
<span data-ttu-id="5ea0d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ea0d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ea0d-118">-InputObject</span></span>
<span data-ttu-id="5ea0d-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="5ea0d-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5ea0d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ea0d-120">-KeyName</span></span>
<span data-ttu-id="5ea0d-121">IoT enhetens konfigurations princip namn för åtkomst till tjänst</span><span class="sxs-lookup"><span data-stu-id="5ea0d-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="5ea0d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ea0d-122">-Name</span></span>
<span data-ttu-id="5ea0d-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="5ea0d-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5ea0d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ea0d-124">-PassThru</span></span>
<span data-ttu-id="5ea0d-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5ea0d-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5ea0d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea0d-126">-ResourceGroupName</span></span>
<span data-ttu-id="5ea0d-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5ea0d-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5ea0d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ea0d-128">-ResourceId</span></span>
<span data-ttu-id="5ea0d-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="5ea0d-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5ea0d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ea0d-130">-Confirm</span></span>
<span data-ttu-id="5ea0d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ea0d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ea0d-132">-WhatIf</span></span>
<span data-ttu-id="5ea0d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ea0d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ea0d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea0d-135">CommonParameters</span></span>
<span data-ttu-id="5ea0d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea0d-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ea0d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea0d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ea0d-138">INPUTS</span></span>

### <span data-ttu-id="5ea0d-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="5ea0d-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="5ea0d-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5ea0d-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5ea0d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5ea0d-141">System.String</span></span>

## <span data-ttu-id="5ea0d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ea0d-142">OUTPUTS</span></span>

### <span data-ttu-id="5ea0d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ea0d-143">System.Boolean</span></span>

## <span data-ttu-id="5ea0d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ea0d-144">NOTES</span></span>

## <span data-ttu-id="5ea0d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ea0d-145">RELATED LINKS</span></span>
