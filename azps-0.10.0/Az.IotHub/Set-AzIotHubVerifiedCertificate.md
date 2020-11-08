---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 17149af8eb279f95631aafc50d3c0b21857fec98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924505"
---
# <span data-ttu-id="e6f2c-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="e6f2c-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="e6f2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f2c-103">Verifierar ett Azure IoT Hub-certifikat.</span><span class="sxs-lookup"><span data-stu-id="e6f2c-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="e6f2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6f2c-104">SYNTAX</span></span>

### <span data-ttu-id="e6f2c-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e6f2c-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6f2c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e6f2c-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f2c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e6f2c-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6f2c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6f2c-108">DESCRIPTION</span></span>
<span data-ttu-id="e6f2c-109">Verifiera ett certifikat genom att överföra ett verifierings certifikat som innehåller verifierings koden som hämtas av cmdlet Get-AzIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="e6f2c-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="e6f2c-110">Det här är det sista steget i det beskrivna processen.</span><span class="sxs-lookup"><span data-stu-id="e6f2c-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="e6f2c-111">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="e6f2c-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="e6f2c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6f2c-112">EXAMPLES</span></span>

### <span data-ttu-id="e6f2c-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e6f2c-113">Example 1</span></span>
```
PS C:\> Set-AzIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="e6f2c-114">Verifierar ägandet av min certifikats privata nycklar.</span><span class="sxs-lookup"><span data-stu-id="e6f2c-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="e6f2c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6f2c-115">PARAMETERS</span></span>

### <span data-ttu-id="e6f2c-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e6f2c-116">-CertificateName</span></span>
<span data-ttu-id="e6f2c-117">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="e6f2c-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="e6f2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f2c-118">-DefaultProfile</span></span>
<span data-ttu-id="e6f2c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f2c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6f2c-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="e6f2c-120">-Etag</span></span>
<span data-ttu-id="e6f2c-121">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="e6f2c-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="e6f2c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6f2c-122">-InputObject</span></span>
<span data-ttu-id="e6f2c-123">Certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="e6f2c-123">Certificate Object</span></span>

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

### <span data-ttu-id="e6f2c-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6f2c-124">-Name</span></span>
<span data-ttu-id="e6f2c-125">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="e6f2c-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e6f2c-126">-Path</span><span class="sxs-lookup"><span data-stu-id="e6f2c-126">-Path</span></span>
<span data-ttu-id="e6f2c-127">Base-64-representation av X509 Certificate. cer-fil eller PEM-fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="e6f2c-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="e6f2c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f2c-128">-ResourceGroupName</span></span>
<span data-ttu-id="e6f2c-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e6f2c-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e6f2c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6f2c-130">-ResourceId</span></span>
<span data-ttu-id="e6f2c-131">Resurs-ID för certifikat</span><span class="sxs-lookup"><span data-stu-id="e6f2c-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="e6f2c-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e6f2c-132">-Confirm</span></span>
<span data-ttu-id="e6f2c-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6f2c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f2c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f2c-134">-WhatIf</span></span>
<span data-ttu-id="e6f2c-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e6f2c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f2c-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e6f2c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f2c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f2c-137">CommonParameters</span></span>
<span data-ttu-id="e6f2c-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f2c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f2c-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f2c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f2c-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6f2c-140">INPUTS</span></span>

### <span data-ttu-id="e6f2c-141">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="e6f2c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="e6f2c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e6f2c-142">System.String</span></span>

## <span data-ttu-id="e6f2c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6f2c-143">OUTPUTS</span></span>

### <span data-ttu-id="e6f2c-144">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="e6f2c-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="e6f2c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6f2c-145">NOTES</span></span>

## <span data-ttu-id="e6f2c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6f2c-146">RELATED LINKS</span></span>