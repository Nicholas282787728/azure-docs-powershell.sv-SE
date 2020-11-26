---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270707"
---
# <span data-ttu-id="2bc32-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="2bc32-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="2bc32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bc32-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc32-103">Ta bort en enhets registrerings grupp.</span><span class="sxs-lookup"><span data-stu-id="2bc32-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="2bc32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bc32-104">SYNTAX</span></span>

### <span data-ttu-id="2bc32-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2bc32-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bc32-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2bc32-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bc32-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2bc32-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bc32-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bc32-108">DESCRIPTION</span></span>
<span data-ttu-id="2bc32-109">Ta bort en registrerings grupp i en Azure IoT Hub-enhet för etablering.</span><span class="sxs-lookup"><span data-stu-id="2bc32-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2bc32-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bc32-110">EXAMPLES</span></span>

### <span data-ttu-id="2bc32-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2bc32-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="2bc32-112">Ta bort en angiven registrerings grupp.</span><span class="sxs-lookup"><span data-stu-id="2bc32-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="2bc32-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2bc32-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="2bc32-114">Ta bort alla registrerings grupper.</span><span class="sxs-lookup"><span data-stu-id="2bc32-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="2bc32-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bc32-115">PARAMETERS</span></span>

### <span data-ttu-id="2bc32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc32-116">-DefaultProfile</span></span>
<span data-ttu-id="2bc32-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc32-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bc32-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="2bc32-118">-DpsName</span></span>
<span data-ttu-id="2bc32-119">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="2bc32-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2bc32-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2bc32-120">-DpsObject</span></span>
<span data-ttu-id="2bc32-121">Tjänst objekt för IoT-enhetsupptäckning</span><span class="sxs-lookup"><span data-stu-id="2bc32-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2bc32-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="2bc32-122">-Name</span></span>
<span data-ttu-id="2bc32-123">Namn på registrerings gruppen.</span><span class="sxs-lookup"><span data-stu-id="2bc32-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="2bc32-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bc32-124">-PassThru</span></span>
<span data-ttu-id="2bc32-125">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="2bc32-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="2bc32-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2bc32-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2bc32-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bc32-127">-ResourceGroupName</span></span>
<span data-ttu-id="2bc32-128">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="2bc32-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2bc32-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bc32-129">-ResourceId</span></span>
<span data-ttu-id="2bc32-130">ID för IoT-etablerings tjänst</span><span class="sxs-lookup"><span data-stu-id="2bc32-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2bc32-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2bc32-131">-Confirm</span></span>
<span data-ttu-id="2bc32-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2bc32-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bc32-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bc32-133">-WhatIf</span></span>
<span data-ttu-id="2bc32-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2bc32-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bc32-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2bc32-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bc32-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc32-136">CommonParameters</span></span>
<span data-ttu-id="2bc32-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc32-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc32-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bc32-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc32-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bc32-139">INPUTS</span></span>

### <span data-ttu-id="2bc32-140">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2bc32-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2bc32-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2bc32-141">System.String</span></span>

## <span data-ttu-id="2bc32-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bc32-142">OUTPUTS</span></span>

### <span data-ttu-id="2bc32-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2bc32-143">System.Boolean</span></span>

## <span data-ttu-id="2bc32-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bc32-144">NOTES</span></span>

## <span data-ttu-id="2bc32-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bc32-145">RELATED LINKS</span></span>