---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099724"
---
# <span data-ttu-id="15e36-101">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15e36-101">Remove-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="15e36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15e36-102">SYNOPSIS</span></span>
<span data-ttu-id="15e36-103">Tar bort ett SSL-certifikat från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="15e36-103">Removes an SSL certificate from an application gateway.</span></span>

## <span data-ttu-id="15e36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15e36-104">SYNTAX</span></span>

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="15e36-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15e36-105">DESCRIPTION</span></span>
<span data-ttu-id="15e36-106">Cmdleten **Remove-AzureApplicationGatewaySslCertificate** tar bort ett SSL-certifikat från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="15e36-106">The **Remove-AzureApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an application gateway.</span></span>

## <span data-ttu-id="15e36-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15e36-107">EXAMPLES</span></span>

### <span data-ttu-id="15e36-108">Exempel 1: ta bort ett SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="15e36-108">Example 1: Remove an SSL certificate</span></span>
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="15e36-109">Det här kommandot tar bort ett SSL-certifikat som heter SslCertificate13 från programgatewayen med namnet ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="15e36-109">This command removes an SSL certificate named SslCertificate13 from the application gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="15e36-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15e36-110">PARAMETERS</span></span>

### <span data-ttu-id="15e36-111">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="15e36-111">-CertificateName</span></span>
<span data-ttu-id="15e36-112">Anger namnet på ett SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="15e36-112">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="15e36-113">Denna cmdlet tar bort certifikatet som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="15e36-113">This cmdlet removes the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="15e36-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="15e36-114">-Name</span></span>
<span data-ttu-id="15e36-115">Anger namnet på den Programgateway som den här cmdleten tar bort ett SSL-certifikat från.</span><span class="sxs-lookup"><span data-stu-id="15e36-115">Specifies the name of the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="15e36-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="15e36-116">-Profile</span></span>
<span data-ttu-id="15e36-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="15e36-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="15e36-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="15e36-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="15e36-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e36-119">CommonParameters</span></span>
<span data-ttu-id="15e36-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15e36-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e36-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15e36-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e36-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15e36-122">INPUTS</span></span>

### <span data-ttu-id="15e36-123">System. String</span><span class="sxs-lookup"><span data-stu-id="15e36-123">System.String</span></span>

## <span data-ttu-id="15e36-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15e36-124">OUTPUTS</span></span>

### <span data-ttu-id="15e36-125">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="15e36-125">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="15e36-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15e36-126">NOTES</span></span>

## <span data-ttu-id="15e36-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15e36-127">RELATED LINKS</span></span>

[<span data-ttu-id="15e36-128">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15e36-128">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="15e36-129">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15e36-129">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)
