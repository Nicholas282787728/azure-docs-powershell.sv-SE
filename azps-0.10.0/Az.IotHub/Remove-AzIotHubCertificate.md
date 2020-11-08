---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 94df7d1870577711174dc4f810c74af528256cb0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922790"
---
# <span data-ttu-id="55036-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="55036-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="55036-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55036-102">SYNOPSIS</span></span>
<span data-ttu-id="55036-103">Tar bort ett Azure IoT Hub-certifikat.</span><span class="sxs-lookup"><span data-stu-id="55036-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="55036-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55036-104">SYNTAX</span></span>

### <span data-ttu-id="55036-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="55036-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55036-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="55036-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55036-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="55036-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55036-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55036-108">DESCRIPTION</span></span>
<span data-ttu-id="55036-109">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="55036-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="55036-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55036-110">EXAMPLES</span></span>

### <span data-ttu-id="55036-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="55036-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="55036-112">Tar bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="55036-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="55036-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55036-113">PARAMETERS</span></span>

### <span data-ttu-id="55036-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="55036-114">-CertificateName</span></span>
<span data-ttu-id="55036-115">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="55036-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="55036-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55036-116">-DefaultProfile</span></span>
<span data-ttu-id="55036-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55036-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55036-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="55036-118">-Etag</span></span>
<span data-ttu-id="55036-119">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="55036-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="55036-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55036-120">-InputObject</span></span>
<span data-ttu-id="55036-121">Certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="55036-121">Certificate Object</span></span>

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

### <span data-ttu-id="55036-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="55036-122">-Name</span></span>
<span data-ttu-id="55036-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="55036-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="55036-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55036-124">-PassThru</span></span>
<span data-ttu-id="55036-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="55036-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="55036-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55036-126">-ResourceGroupName</span></span>
<span data-ttu-id="55036-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="55036-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="55036-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55036-128">-ResourceId</span></span>
<span data-ttu-id="55036-129">Resurs-ID för certifikat</span><span class="sxs-lookup"><span data-stu-id="55036-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="55036-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="55036-130">-Confirm</span></span>
<span data-ttu-id="55036-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="55036-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55036-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55036-132">-WhatIf</span></span>
<span data-ttu-id="55036-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="55036-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55036-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="55036-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55036-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55036-135">CommonParameters</span></span>
<span data-ttu-id="55036-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55036-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55036-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55036-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55036-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55036-138">INPUTS</span></span>

### <span data-ttu-id="55036-139">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="55036-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="55036-140">System. String</span><span class="sxs-lookup"><span data-stu-id="55036-140">System.String</span></span>

## <span data-ttu-id="55036-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55036-141">OUTPUTS</span></span>

### <span data-ttu-id="55036-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55036-142">System.Boolean</span></span>

## <span data-ttu-id="55036-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55036-143">NOTES</span></span>

## <span data-ttu-id="55036-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55036-144">RELATED LINKS</span></span>