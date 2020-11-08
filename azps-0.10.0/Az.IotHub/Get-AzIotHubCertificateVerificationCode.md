---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: d4a9d20981c9777e02fd22e1dbbb70b24e91e282
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922825"
---
# <span data-ttu-id="3fc15-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="3fc15-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="3fc15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3fc15-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc15-103">Genererar en verifierings kod för ett Azure IoT Hub-certifikat.</span><span class="sxs-lookup"><span data-stu-id="3fc15-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="3fc15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3fc15-104">SYNTAX</span></span>

### <span data-ttu-id="3fc15-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3fc15-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fc15-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3fc15-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fc15-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3fc15-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fc15-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3fc15-108">DESCRIPTION</span></span>
<span data-ttu-id="3fc15-109">Den här verifierings koden används för att slutföra beviset för en besittning för ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="3fc15-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="3fc15-110">Använd den här verifierings koden som CN för ett nytt certifikat som är signerat med rot certifikatets privata nycklar.</span><span class="sxs-lookup"><span data-stu-id="3fc15-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="3fc15-111">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="3fc15-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="3fc15-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3fc15-112">EXAMPLES</span></span>

### <span data-ttu-id="3fc15-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3fc15-113">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="3fc15-114">Genererar en verifierings kod för mina certifikat</span><span class="sxs-lookup"><span data-stu-id="3fc15-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="3fc15-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3fc15-115">PARAMETERS</span></span>

### <span data-ttu-id="3fc15-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="3fc15-116">-CertificateName</span></span>
<span data-ttu-id="3fc15-117">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="3fc15-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="3fc15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc15-118">-DefaultProfile</span></span>
<span data-ttu-id="3fc15-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc15-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fc15-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="3fc15-120">-Etag</span></span>
<span data-ttu-id="3fc15-121">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="3fc15-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="3fc15-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fc15-122">-InputObject</span></span>
<span data-ttu-id="3fc15-123">Certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="3fc15-123">Certificate Object</span></span>

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

### <span data-ttu-id="3fc15-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3fc15-124">-Name</span></span>
<span data-ttu-id="3fc15-125">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="3fc15-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3fc15-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fc15-126">-ResourceGroupName</span></span>
<span data-ttu-id="3fc15-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="3fc15-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3fc15-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fc15-128">-ResourceId</span></span>
<span data-ttu-id="3fc15-129">Resurs-ID för certifikat</span><span class="sxs-lookup"><span data-stu-id="3fc15-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="3fc15-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc15-130">CommonParameters</span></span>
<span data-ttu-id="3fc15-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fc15-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc15-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fc15-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc15-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3fc15-133">INPUTS</span></span>

### <span data-ttu-id="3fc15-134">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="3fc15-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="3fc15-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3fc15-135">System.String</span></span>

## <span data-ttu-id="3fc15-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3fc15-136">OUTPUTS</span></span>

### <span data-ttu-id="3fc15-137">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="3fc15-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="3fc15-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3fc15-138">NOTES</span></span>

## <span data-ttu-id="3fc15-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3fc15-139">RELATED LINKS</span></span>