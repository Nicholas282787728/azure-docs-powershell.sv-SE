---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 64de44e74b5c6ea21d9d49b1911bcd34a74a374a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756176"
---
# <span data-ttu-id="c2f69-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="c2f69-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="c2f69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2f69-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f69-103">Ta bort ett certifikat för konfiguration av en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="c2f69-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2f69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2f69-104">SYNTAX</span></span>

### <span data-ttu-id="c2f69-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c2f69-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f69-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c2f69-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f69-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c2f69-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2f69-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2f69-108">DESCRIPTION</span></span>
<span data-ttu-id="c2f69-109">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i konfigurations tjänsten för Azure IoT Hub-enheter finns i https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="c2f69-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="c2f69-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2f69-110">EXAMPLES</span></span>

### <span data-ttu-id="c2f69-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2f69-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="c2f69-112">Ta bort "certifikatet" i en konfigurations tjänst för en Azure IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="c2f69-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c2f69-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2f69-113">PARAMETERS</span></span>

### <span data-ttu-id="c2f69-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c2f69-114">-CertificateName</span></span>
<span data-ttu-id="c2f69-115">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="c2f69-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="c2f69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f69-116">-DefaultProfile</span></span>
<span data-ttu-id="c2f69-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f69-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2f69-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="c2f69-118">-Etag</span></span>
<span data-ttu-id="c2f69-119">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="c2f69-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="c2f69-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2f69-120">-InputObject</span></span>
<span data-ttu-id="c2f69-121">Objekt för webb tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="c2f69-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="c2f69-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2f69-122">-Name</span></span>
<span data-ttu-id="c2f69-123">Namn på IoT-etablerings tjänsten</span><span class="sxs-lookup"><span data-stu-id="c2f69-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c2f69-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2f69-124">-PassThru</span></span>
<span data-ttu-id="c2f69-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c2f69-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c2f69-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2f69-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2f69-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c2f69-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c2f69-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2f69-128">-ResourceId</span></span>
<span data-ttu-id="c2f69-129">ID för tjänst certifikat för IoT</span><span class="sxs-lookup"><span data-stu-id="c2f69-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="c2f69-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2f69-130">-Confirm</span></span>
<span data-ttu-id="c2f69-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2f69-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2f69-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f69-132">-WhatIf</span></span>
<span data-ttu-id="c2f69-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2f69-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2f69-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2f69-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2f69-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f69-135">CommonParameters</span></span>
<span data-ttu-id="c2f69-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f69-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f69-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2f69-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f69-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2f69-138">INPUTS</span></span>

### <span data-ttu-id="c2f69-139">Microsoft. Azure. commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="c2f69-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="c2f69-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c2f69-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c2f69-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c2f69-141">System.String</span></span>

## <span data-ttu-id="c2f69-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2f69-142">OUTPUTS</span></span>

### <span data-ttu-id="c2f69-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2f69-143">System.Boolean</span></span>

## <span data-ttu-id="c2f69-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2f69-144">NOTES</span></span>

## <span data-ttu-id="c2f69-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2f69-145">RELATED LINKS</span></span>
