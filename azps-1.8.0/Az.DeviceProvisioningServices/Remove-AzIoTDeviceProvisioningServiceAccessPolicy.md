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
ms.locfileid: "93754147"
---
# <span data-ttu-id="afafd-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="afafd-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="afafd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afafd-102">SYNOPSIS</span></span>
<span data-ttu-id="afafd-103">Ta bort delade åtkomst principer i en Azure IoT Hub-enhet för etablerings tjänst.</span><span class="sxs-lookup"><span data-stu-id="afafd-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="afafd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afafd-104">SYNTAX</span></span>

### <span data-ttu-id="afafd-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="afafd-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afafd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="afafd-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afafd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="afafd-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afafd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afafd-108">DESCRIPTION</span></span>
<span data-ttu-id="afafd-109">En introduktion till tjänste etablerings tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="afafd-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="afafd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afafd-110">EXAMPLES</span></span>

### <span data-ttu-id="afafd-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="afafd-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="afafd-112">Ta bort principen "policy" för delad åtkomst i en konfigurations tjänst för en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="afafd-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="afafd-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="afafd-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="afafd-114">Ta bort principen "policy" för delad åtkomst i en tjänste etablerings tjänst från en Azure IoT Hub-enhet med pipeline.</span><span class="sxs-lookup"><span data-stu-id="afafd-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="afafd-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afafd-115">PARAMETERS</span></span>

### <span data-ttu-id="afafd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afafd-116">-DefaultProfile</span></span>
<span data-ttu-id="afafd-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="afafd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afafd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afafd-118">-InputObject</span></span>
<span data-ttu-id="afafd-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="afafd-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="afafd-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="afafd-120">-KeyName</span></span>
<span data-ttu-id="afafd-121">IoT enhetens konfigurations princip namn för åtkomst till tjänst</span><span class="sxs-lookup"><span data-stu-id="afafd-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="afafd-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="afafd-122">-Name</span></span>
<span data-ttu-id="afafd-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="afafd-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="afafd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afafd-124">-PassThru</span></span>
<span data-ttu-id="afafd-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="afafd-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="afafd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afafd-126">-ResourceGroupName</span></span>
<span data-ttu-id="afafd-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="afafd-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="afafd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afafd-128">-ResourceId</span></span>
<span data-ttu-id="afafd-129">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="afafd-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="afafd-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="afafd-130">-Confirm</span></span>
<span data-ttu-id="afafd-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="afafd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afafd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afafd-132">-WhatIf</span></span>
<span data-ttu-id="afafd-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="afafd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afafd-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="afafd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afafd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afafd-135">CommonParameters</span></span>
<span data-ttu-id="afafd-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afafd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afafd-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afafd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afafd-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afafd-138">INPUTS</span></span>

### <span data-ttu-id="afafd-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="afafd-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="afafd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="afafd-140">System.String</span></span>

## <span data-ttu-id="afafd-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afafd-141">OUTPUTS</span></span>

### <span data-ttu-id="afafd-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="afafd-142">System.Boolean</span></span>

## <span data-ttu-id="afafd-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afafd-143">NOTES</span></span>

## <span data-ttu-id="afafd-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afafd-144">RELATED LINKS</span></span>
