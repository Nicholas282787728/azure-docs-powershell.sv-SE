---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: de24d9d16af5b429dcf59ffc8f4cbeb7dd0654f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755949"
---
# <span data-ttu-id="0e5bd-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="0e5bd-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="0e5bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e5bd-102">SYNOPSIS</span></span>
<span data-ttu-id="0e5bd-103">Tar bort ett Azure IoT Hub-certifikat.</span><span class="sxs-lookup"><span data-stu-id="0e5bd-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e5bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e5bd-104">SYNTAX</span></span>

### <span data-ttu-id="0e5bd-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0e5bd-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e5bd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0e5bd-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e5bd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0e5bd-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e5bd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e5bd-108">DESCRIPTION</span></span>
<span data-ttu-id="0e5bd-109">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="0e5bd-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="0e5bd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e5bd-110">EXAMPLES</span></span>

### <span data-ttu-id="0e5bd-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0e5bd-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="0e5bd-112">Tar bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="0e5bd-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="0e5bd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e5bd-113">PARAMETERS</span></span>

### <span data-ttu-id="0e5bd-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="0e5bd-114">-CertificateName</span></span>
<span data-ttu-id="0e5bd-115">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="0e5bd-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="0e5bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e5bd-116">-DefaultProfile</span></span>
<span data-ttu-id="0e5bd-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e5bd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e5bd-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="0e5bd-118">-Etag</span></span>
<span data-ttu-id="0e5bd-119">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="0e5bd-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="0e5bd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e5bd-120">-InputObject</span></span>
<span data-ttu-id="0e5bd-121">Certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="0e5bd-121">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5bd-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e5bd-122">-Name</span></span>
<span data-ttu-id="0e5bd-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="0e5bd-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5bd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e5bd-124">-PassThru</span></span>
<span data-ttu-id="0e5bd-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0e5bd-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0e5bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e5bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="0e5bd-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="0e5bd-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5bd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e5bd-128">-ResourceId</span></span>
<span data-ttu-id="0e5bd-129">Resurs-ID för certifikat</span><span class="sxs-lookup"><span data-stu-id="0e5bd-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="0e5bd-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e5bd-130">-Confirm</span></span>
<span data-ttu-id="0e5bd-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e5bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e5bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e5bd-132">-WhatIf</span></span>
<span data-ttu-id="0e5bd-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e5bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e5bd-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e5bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e5bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e5bd-135">CommonParameters</span></span>
<span data-ttu-id="0e5bd-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e5bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e5bd-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e5bd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e5bd-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e5bd-138">INPUTS</span></span>

### <span data-ttu-id="0e5bd-139">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="0e5bd-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="0e5bd-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0e5bd-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0e5bd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0e5bd-141">System.String</span></span>

## <span data-ttu-id="0e5bd-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e5bd-142">OUTPUTS</span></span>

### <span data-ttu-id="0e5bd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e5bd-143">System.Boolean</span></span>

## <span data-ttu-id="0e5bd-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e5bd-144">NOTES</span></span>

## <span data-ttu-id="0e5bd-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e5bd-145">RELATED LINKS</span></span>
