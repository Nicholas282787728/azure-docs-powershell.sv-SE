---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
ms.openlocfilehash: 45afd8c7f690be7785a14d336fabe7ac52a6f44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584228"
---
# <span data-ttu-id="5fac7-101">Set-AzureRmIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="5fac7-101">Set-AzureRmIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="5fac7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fac7-102">SYNOPSIS</span></span>
<span data-ttu-id="5fac7-103">Verifierar ett Azure IoT Hub-certifikat.</span><span class="sxs-lookup"><span data-stu-id="5fac7-103">Verifies an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fac7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fac7-104">SYNTAX</span></span>

### <span data-ttu-id="5fac7-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5fac7-105">ResourceSet (Default)</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fac7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5fac7-106">InputObjectSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fac7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5fac7-107">ResourceIdSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fac7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fac7-108">DESCRIPTION</span></span>
<span data-ttu-id="5fac7-109">Verifiera ett certifikat genom att överföra ett verifierings certifikat som innehåller verifierings koden som hämtas av cmdlet Get-AzureRmIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="5fac7-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzureRmIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="5fac7-110">Det här är det sista steget i det beskrivna processen.</span><span class="sxs-lookup"><span data-stu-id="5fac7-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="5fac7-111">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="5fac7-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="5fac7-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fac7-112">EXAMPLES</span></span>

### <span data-ttu-id="5fac7-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5fac7-113">Example 1</span></span>
```
PS C:\> Set-AzureRmIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="5fac7-114">Verifierar ägandet av min certifikats privata nycklar.</span><span class="sxs-lookup"><span data-stu-id="5fac7-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="5fac7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fac7-115">PARAMETERS</span></span>

### <span data-ttu-id="5fac7-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="5fac7-116">-CertificateName</span></span>
<span data-ttu-id="5fac7-117">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="5fac7-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="5fac7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fac7-118">-DefaultProfile</span></span>
<span data-ttu-id="5fac7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fac7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fac7-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="5fac7-120">-Etag</span></span>
<span data-ttu-id="5fac7-121">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="5fac7-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="5fac7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fac7-122">-InputObject</span></span>
<span data-ttu-id="5fac7-123">Certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="5fac7-123">Certificate Object</span></span>

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

### <span data-ttu-id="5fac7-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="5fac7-124">-Name</span></span>
<span data-ttu-id="5fac7-125">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="5fac7-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5fac7-126">-Path</span><span class="sxs-lookup"><span data-stu-id="5fac7-126">-Path</span></span>
<span data-ttu-id="5fac7-127">Base-64-representation av X509 Certificate. cer-fil eller PEM-fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="5fac7-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="5fac7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fac7-128">-ResourceGroupName</span></span>
<span data-ttu-id="5fac7-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5fac7-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5fac7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fac7-130">-ResourceId</span></span>
<span data-ttu-id="5fac7-131">Resurs-ID för certifikat</span><span class="sxs-lookup"><span data-stu-id="5fac7-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="5fac7-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5fac7-132">-Confirm</span></span>
<span data-ttu-id="5fac7-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5fac7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fac7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fac7-134">-WhatIf</span></span>
<span data-ttu-id="5fac7-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5fac7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fac7-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5fac7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fac7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fac7-137">CommonParameters</span></span>
<span data-ttu-id="5fac7-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fac7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fac7-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fac7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fac7-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fac7-140">INPUTS</span></span>

### <span data-ttu-id="5fac7-141">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="5fac7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="5fac7-142">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5fac7-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5fac7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5fac7-143">System.String</span></span>

## <span data-ttu-id="5fac7-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fac7-144">OUTPUTS</span></span>

### <span data-ttu-id="5fac7-145">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="5fac7-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="5fac7-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fac7-146">NOTES</span></span>

## <span data-ttu-id="5fac7-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fac7-147">RELATED LINKS</span></span>
