---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093390"
---
# <span data-ttu-id="2f056-101">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f056-101">Get-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="2f056-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f056-102">SYNOPSIS</span></span>
<span data-ttu-id="2f056-103">Hämtar Application Gateway-certifikat.</span><span class="sxs-lookup"><span data-stu-id="2f056-103">Gets Application Gateway certificates.</span></span>

## <span data-ttu-id="2f056-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f056-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2f056-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f056-105">DESCRIPTION</span></span>
<span data-ttu-id="2f056-106">Cmdleten **Get-AzureApplicationGatewaySslCertificate** hämtar SSL-certifikat (Secure Sockets Layer) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2f056-106">The **Get-AzureApplicationGatewaySslCertificate** cmdlet gets Secure Sockets Layer (SSL) certificates for an Azure Application Gateway.</span></span>

## <span data-ttu-id="2f056-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f056-107">EXAMPLES</span></span>

### <span data-ttu-id="2f056-108">Exempel 1: skaffa ett SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="2f056-108">Example 1: Get an SSL certificate</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="2f056-109">Det här kommandot får ett SSL-certifikat som heter SslCertificate13 på programgatewayen med namnet ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="2f056-109">This command gets an SSL certificate named SslCertificate13 on the Application Gateway named ApplicationGateway08.</span></span>

### <span data-ttu-id="2f056-110">Exempel 2: Hämta alla SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="2f056-110">Example 2: Get all SSL certificates</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

<span data-ttu-id="2f056-111">Det här kommandot får alla SSL-certifikat på programgatewayen med namnet ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="2f056-111">This command gets all the SSL certificates on the Application Gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="2f056-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f056-112">PARAMETERS</span></span>

### <span data-ttu-id="2f056-113">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2f056-113">-CertificateName</span></span>
<span data-ttu-id="2f056-114">Anger namnet på ett SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="2f056-114">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="2f056-115">Denna cmdlet hämtar certifikatet som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2f056-115">This cmdlet gets the certificate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f056-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f056-116">-Name</span></span>
<span data-ttu-id="2f056-117">Anger namnet på den Programgateway som den här cmdleten får ett SSL-certifikat från.</span><span class="sxs-lookup"><span data-stu-id="2f056-117">Specifies the name of the Application Gateway from which this cmdlet gets an SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f056-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="2f056-118">-Profile</span></span>
<span data-ttu-id="2f056-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="2f056-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f056-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="2f056-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f056-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f056-121">CommonParameters</span></span>
<span data-ttu-id="2f056-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f056-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f056-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f056-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f056-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f056-124">INPUTS</span></span>

### <span data-ttu-id="2f056-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2f056-125">System.String</span></span>

## <span data-ttu-id="2f056-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f056-126">OUTPUTS</span></span>

### <span data-ttu-id="2f056-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, list<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate></span><span class="sxs-lookup"><span data-stu-id="2f056-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate, List<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate></span></span>

## <span data-ttu-id="2f056-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f056-128">NOTES</span></span>

## <span data-ttu-id="2f056-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f056-129">RELATED LINKS</span></span>

[<span data-ttu-id="2f056-130">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f056-130">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2f056-131">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f056-131">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
