---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263225"
---
# <span data-ttu-id="39af6-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="39af6-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="39af6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39af6-102">SYNOPSIS</span></span>
<span data-ttu-id="39af6-103">Ta bort en enhets registrerings post.</span><span class="sxs-lookup"><span data-stu-id="39af6-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="39af6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39af6-104">SYNTAX</span></span>

### <span data-ttu-id="39af6-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="39af6-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39af6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="39af6-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39af6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="39af6-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39af6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39af6-108">DESCRIPTION</span></span>
<span data-ttu-id="39af6-109">Ta bort en enhets registrering i en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="39af6-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="39af6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39af6-110">EXAMPLES</span></span>

### <span data-ttu-id="39af6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="39af6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="39af6-112">Ta bort en angiven registrerings post.</span><span class="sxs-lookup"><span data-stu-id="39af6-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="39af6-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="39af6-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="39af6-114">Ta bort alla registrerings poster.</span><span class="sxs-lookup"><span data-stu-id="39af6-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="39af6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39af6-115">PARAMETERS</span></span>

### <span data-ttu-id="39af6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39af6-116">-DefaultProfile</span></span>
<span data-ttu-id="39af6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39af6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39af6-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="39af6-118">-DpsName</span></span>
<span data-ttu-id="39af6-119">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="39af6-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="39af6-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="39af6-120">-DpsObject</span></span>
<span data-ttu-id="39af6-121">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="39af6-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="39af6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39af6-122">-PassThru</span></span>
<span data-ttu-id="39af6-123">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="39af6-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="39af6-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="39af6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="39af6-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="39af6-125">-RegistrationId</span></span>
<span data-ttu-id="39af6-126">Registrerings-ID för individuell registrering.</span><span class="sxs-lookup"><span data-stu-id="39af6-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="39af6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39af6-127">-ResourceGroupName</span></span>
<span data-ttu-id="39af6-128">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="39af6-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="39af6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39af6-129">-ResourceId</span></span>
<span data-ttu-id="39af6-130">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="39af6-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="39af6-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="39af6-131">-Confirm</span></span>
<span data-ttu-id="39af6-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39af6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39af6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39af6-133">-WhatIf</span></span>
<span data-ttu-id="39af6-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="39af6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39af6-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="39af6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39af6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39af6-136">CommonParameters</span></span>
<span data-ttu-id="39af6-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39af6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39af6-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39af6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39af6-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39af6-139">INPUTS</span></span>

### <span data-ttu-id="39af6-140">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="39af6-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="39af6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="39af6-141">System.String</span></span>

## <span data-ttu-id="39af6-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39af6-142">OUTPUTS</span></span>

### <span data-ttu-id="39af6-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39af6-143">System.Boolean</span></span>

## <span data-ttu-id="39af6-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39af6-144">NOTES</span></span>

## <span data-ttu-id="39af6-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39af6-145">RELATED LINKS</span></span>
