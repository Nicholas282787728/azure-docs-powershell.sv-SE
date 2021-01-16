---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 6d77bcc6d940c5891b4fc06875dc353af5f75939
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397096"
---
# <span data-ttu-id="0531f-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="0531f-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="0531f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0531f-102">SYNOPSIS</span></span>
<span data-ttu-id="0531f-103">Skapa/uppdatera ett Azure IoT Hub-certifikat.</span><span class="sxs-lookup"><span data-stu-id="0531f-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="0531f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0531f-104">SYNTAX</span></span>

### <span data-ttu-id="0531f-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0531f-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0531f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0531f-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0531f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0531f-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0531f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0531f-108">DESCRIPTION</span></span>
<span data-ttu-id="0531f-109">Uppladdar ett nytt certifikat eller ersätter det befintliga certifikatet med samma namn.</span><span class="sxs-lookup"><span data-stu-id="0531f-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="0531f-110">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="0531f-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="0531f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0531f-111">EXAMPLES</span></span>

### <span data-ttu-id="0531f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0531f-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="0531f-113">Uppladdar en CER-fil för CA-certifikat till en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="0531f-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="0531f-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0531f-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="0531f-115">Uppdaterar ett CERTIFIKATUTFÄRDARCERTIFIKAT i en IoT-hubb genom att överföra en ny CER-fil.</span><span class="sxs-lookup"><span data-stu-id="0531f-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="0531f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0531f-116">PARAMETERS</span></span>

### <span data-ttu-id="0531f-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="0531f-117">-CertificateName</span></span>
<span data-ttu-id="0531f-118">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="0531f-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="0531f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0531f-119">-DefaultProfile</span></span>
<span data-ttu-id="0531f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0531f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0531f-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="0531f-121">-Etag</span></span>
<span data-ttu-id="0531f-122">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="0531f-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="0531f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0531f-123">-InputObject</span></span>
<span data-ttu-id="0531f-124">Certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="0531f-124">Certificate Object</span></span>

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

### <span data-ttu-id="0531f-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="0531f-125">-Name</span></span>
<span data-ttu-id="0531f-126">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="0531f-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0531f-127">-Path</span><span class="sxs-lookup"><span data-stu-id="0531f-127">-Path</span></span>
<span data-ttu-id="0531f-128">Base-64-representation av X509 Certificate. cer-fil eller PEM-fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="0531f-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0531f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0531f-129">-ResourceGroupName</span></span>
<span data-ttu-id="0531f-130">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="0531f-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0531f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0531f-131">-ResourceId</span></span>
<span data-ttu-id="0531f-132">Resurs-ID för certifikat</span><span class="sxs-lookup"><span data-stu-id="0531f-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="0531f-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0531f-133">-Confirm</span></span>
<span data-ttu-id="0531f-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0531f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0531f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0531f-135">-WhatIf</span></span>
<span data-ttu-id="0531f-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0531f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0531f-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0531f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0531f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0531f-138">CommonParameters</span></span>
<span data-ttu-id="0531f-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0531f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0531f-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0531f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0531f-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0531f-141">INPUTS</span></span>

### <span data-ttu-id="0531f-142">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="0531f-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="0531f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="0531f-143">System.String</span></span>

## <span data-ttu-id="0531f-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0531f-144">OUTPUTS</span></span>

### <span data-ttu-id="0531f-145">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="0531f-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="0531f-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0531f-146">NOTES</span></span>

## <span data-ttu-id="0531f-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0531f-147">RELATED LINKS</span></span>
