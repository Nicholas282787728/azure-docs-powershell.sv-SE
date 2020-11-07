---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubCertificate.md
ms.openlocfilehash: b38fd64db24a38267b3d06d8046f1bcbb826537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756283"
---
# <span data-ttu-id="1942e-101">Add-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="1942e-101">Add-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="1942e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1942e-102">SYNOPSIS</span></span>
<span data-ttu-id="1942e-103">Skapa/uppdatera ett Azure IoT Hub-certifikat.</span><span class="sxs-lookup"><span data-stu-id="1942e-103">Create/update an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1942e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1942e-104">SYNTAX</span></span>

### <span data-ttu-id="1942e-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1942e-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1942e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1942e-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1942e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1942e-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1942e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1942e-108">DESCRIPTION</span></span>
<span data-ttu-id="1942e-109">Uppladdar ett nytt certifikat eller ersätter det befintliga certifikatet med samma namn.</span><span class="sxs-lookup"><span data-stu-id="1942e-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="1942e-110">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="1942e-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="1942e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1942e-111">EXAMPLES</span></span>

### <span data-ttu-id="1942e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1942e-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

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

<span data-ttu-id="1942e-113">Uppladdar en CER-fil för CA-certifikat till en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="1942e-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="1942e-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1942e-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="1942e-115">Uppdaterar ett CERTIFIKATUTFÄRDARCERTIFIKAT i en IoT-hubb genom att överföra en ny CER-fil.</span><span class="sxs-lookup"><span data-stu-id="1942e-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="1942e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1942e-116">PARAMETERS</span></span>

### <span data-ttu-id="1942e-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="1942e-117">-CertificateName</span></span>
<span data-ttu-id="1942e-118">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="1942e-118">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1942e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1942e-119">-DefaultProfile</span></span>
<span data-ttu-id="1942e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1942e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1942e-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="1942e-121">-Etag</span></span>
<span data-ttu-id="1942e-122">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="1942e-122">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1942e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1942e-123">-InputObject</span></span>
<span data-ttu-id="1942e-124">Certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="1942e-124">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1942e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="1942e-125">-Name</span></span>
<span data-ttu-id="1942e-126">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="1942e-126">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1942e-127">-Path</span><span class="sxs-lookup"><span data-stu-id="1942e-127">-Path</span></span>
<span data-ttu-id="1942e-128">Base-64-representation av X509 Certificate. cer-fil eller PEM-fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="1942e-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1942e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1942e-129">-ResourceGroupName</span></span>
<span data-ttu-id="1942e-130">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="1942e-130">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1942e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1942e-131">-ResourceId</span></span>
<span data-ttu-id="1942e-132">Resurs-ID för certifikat</span><span class="sxs-lookup"><span data-stu-id="1942e-132">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1942e-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1942e-133">-Confirm</span></span>
<span data-ttu-id="1942e-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1942e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1942e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1942e-135">-WhatIf</span></span>
<span data-ttu-id="1942e-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1942e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1942e-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1942e-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1942e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1942e-138">CommonParameters</span></span>
<span data-ttu-id="1942e-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1942e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1942e-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1942e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1942e-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1942e-141">INPUTS</span></span>

### <span data-ttu-id="1942e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1942e-142">System.String</span></span>

## <span data-ttu-id="1942e-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1942e-143">OUTPUTS</span></span>

### <span data-ttu-id="1942e-144">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="1942e-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="1942e-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1942e-145">NOTES</span></span>

## <span data-ttu-id="1942e-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1942e-146">RELATED LINKS</span></span>

