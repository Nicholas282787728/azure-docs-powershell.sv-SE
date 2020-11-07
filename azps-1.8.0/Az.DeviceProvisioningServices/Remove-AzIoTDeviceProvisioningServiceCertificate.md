---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: e03bb9f8f996c274abe07dd3e1b005760756d632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754143"
---
# <span data-ttu-id="6fd06-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="6fd06-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="6fd06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6fd06-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd06-103">Ta bort ett certifikat för konfiguration av en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="6fd06-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="6fd06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6fd06-104">SYNTAX</span></span>

### <span data-ttu-id="6fd06-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6fd06-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd06-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6fd06-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd06-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6fd06-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd06-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6fd06-108">DESCRIPTION</span></span>
<span data-ttu-id="6fd06-109">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i konfigurations tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="6fd06-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="6fd06-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6fd06-110">EXAMPLES</span></span>

### <span data-ttu-id="6fd06-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6fd06-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="6fd06-112">Ta bort "certifikatet" i en konfigurations tjänst för en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="6fd06-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="6fd06-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6fd06-113">PARAMETERS</span></span>

### <span data-ttu-id="6fd06-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="6fd06-114">-CertificateName</span></span>
<span data-ttu-id="6fd06-115">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="6fd06-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd06-116">-DefaultProfile</span></span>
<span data-ttu-id="6fd06-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd06-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd06-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="6fd06-118">-Etag</span></span>
<span data-ttu-id="6fd06-119">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="6fd06-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="6fd06-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fd06-120">-InputObject</span></span>
<span data-ttu-id="6fd06-121">Objekt för webb tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="6fd06-121">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd06-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="6fd06-122">-Name</span></span>
<span data-ttu-id="6fd06-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="6fd06-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6fd06-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fd06-124">-PassThru</span></span>
<span data-ttu-id="6fd06-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6fd06-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6fd06-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd06-126">-ResourceGroupName</span></span>
<span data-ttu-id="6fd06-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="6fd06-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6fd06-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd06-128">-ResourceId</span></span>
<span data-ttu-id="6fd06-129">ID för tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="6fd06-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="6fd06-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6fd06-130">-Confirm</span></span>
<span data-ttu-id="6fd06-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6fd06-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd06-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd06-132">-WhatIf</span></span>
<span data-ttu-id="6fd06-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6fd06-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fd06-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6fd06-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd06-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd06-135">CommonParameters</span></span>
<span data-ttu-id="6fd06-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd06-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd06-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd06-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd06-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6fd06-138">INPUTS</span></span>

### <span data-ttu-id="6fd06-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="6fd06-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="6fd06-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6fd06-140">System.String</span></span>

## <span data-ttu-id="6fd06-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6fd06-141">OUTPUTS</span></span>

### <span data-ttu-id="6fd06-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6fd06-142">System.Boolean</span></span>

## <span data-ttu-id="6fd06-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6fd06-143">NOTES</span></span>

## <span data-ttu-id="6fd06-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6fd06-144">RELATED LINKS</span></span>
