---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261336"
---
# <span data-ttu-id="177c1-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="177c1-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="177c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="177c1-102">SYNOPSIS</span></span>
<span data-ttu-id="177c1-103">Tar bort enhetens registrering.</span><span class="sxs-lookup"><span data-stu-id="177c1-103">Deletes the device registration.</span></span>

## <span data-ttu-id="177c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="177c1-104">SYNTAX</span></span>

### <span data-ttu-id="177c1-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="177c1-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="177c1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="177c1-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="177c1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="177c1-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="177c1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="177c1-108">DESCRIPTION</span></span>
<span data-ttu-id="177c1-109">Ta bort en enhets registrering i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="177c1-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="177c1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="177c1-110">EXAMPLES</span></span>

### <span data-ttu-id="177c1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="177c1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="177c1-112">Ta bort en enhets registrering i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="177c1-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="177c1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="177c1-113">PARAMETERS</span></span>

### <span data-ttu-id="177c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="177c1-114">-DefaultProfile</span></span>
<span data-ttu-id="177c1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="177c1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="177c1-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="177c1-116">-DpsName</span></span>
<span data-ttu-id="177c1-117">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="177c1-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="177c1-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="177c1-118">-DpsObject</span></span>
<span data-ttu-id="177c1-119">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="177c1-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="177c1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="177c1-120">-PassThru</span></span>
<span data-ttu-id="177c1-121">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="177c1-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="177c1-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="177c1-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="177c1-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="177c1-123">-RegistrationId</span></span>
<span data-ttu-id="177c1-124">ID för enhets registrering.</span><span class="sxs-lookup"><span data-stu-id="177c1-124">ID of device registration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="177c1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="177c1-125">-ResourceGroupName</span></span>
<span data-ttu-id="177c1-126">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="177c1-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="177c1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="177c1-127">-ResourceId</span></span>
<span data-ttu-id="177c1-128">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="177c1-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="177c1-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="177c1-129">-Confirm</span></span>
<span data-ttu-id="177c1-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="177c1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="177c1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="177c1-131">-WhatIf</span></span>
<span data-ttu-id="177c1-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="177c1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="177c1-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="177c1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="177c1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="177c1-134">CommonParameters</span></span>
<span data-ttu-id="177c1-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="177c1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="177c1-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="177c1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="177c1-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="177c1-137">INPUTS</span></span>

### <span data-ttu-id="177c1-138">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="177c1-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="177c1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="177c1-139">System.String</span></span>

## <span data-ttu-id="177c1-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="177c1-140">OUTPUTS</span></span>

### <span data-ttu-id="177c1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="177c1-141">System.Boolean</span></span>

## <span data-ttu-id="177c1-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="177c1-142">NOTES</span></span>

## <span data-ttu-id="177c1-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="177c1-143">RELATED LINKS</span></span>
