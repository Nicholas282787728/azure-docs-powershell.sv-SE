---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BA63476C-25CC-444D-AD2C-51BF76374FBC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76ac1f2d1ba5c64fb12bc10320efff8c34538ab8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093462"
---
# <span data-ttu-id="84a69-101">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="84a69-101">Add-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="84a69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84a69-102">SYNOPSIS</span></span>
<span data-ttu-id="84a69-103">Lägger till ett SSL-certifikat i en programport.</span><span class="sxs-lookup"><span data-stu-id="84a69-103">Adds an SSL certificate to an Application Gateway.</span></span>

## <span data-ttu-id="84a69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84a69-104">SYNTAX</span></span>

```
Add-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String> -Password <String>
 -CertificateFile <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="84a69-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84a69-105">DESCRIPTION</span></span>
<span data-ttu-id="84a69-106">Cmdleten **Add-AzureApplicationGatewaySslCertificate** lägger till ett SSL-certifikat i en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="84a69-106">The **Add-AzureApplicationGatewaySslCertificate** cmdlet adds a Secure Sockets Layer (SSL) certificate to an Azure Application Gateway.</span></span>

## <span data-ttu-id="84a69-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84a69-107">EXAMPLES</span></span>

### <span data-ttu-id="84a69-108">Exempel 1: lägga till ett SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="84a69-108">Example 1: Add an SSL certificate</span></span>
```
PS C:\> Add-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13" -Password "password" -CertificateFile "c:\Certs\sslCertificate.pfx"
```

<span data-ttu-id="84a69-109">Det här kommandot lägger till ett SSL-certifikat med namnet SslCertificate13 i programgatewayen med namnet ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="84a69-109">This command adds an SSL certificate named SslCertificate13 to the Application Gateway named ApplicationGateway08.</span></span>
<span data-ttu-id="84a69-110">Kommandot anger sökvägen till certifikat filen och lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="84a69-110">The command specifies the path of the certificate file and the password for the certificate.</span></span>

## <span data-ttu-id="84a69-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84a69-111">PARAMETERS</span></span>

### <span data-ttu-id="84a69-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="84a69-112">-CertificateFile</span></span>
<span data-ttu-id="84a69-113">Anger sökvägen till en SSL-certifikatfil.</span><span class="sxs-lookup"><span data-stu-id="84a69-113">Specifies the path of an SSL certificate file.</span></span>
<span data-ttu-id="84a69-114">Denna cmdlet lägger till certifikatet i filen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="84a69-114">This cmdlet adds the certificate in the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="84a69-115">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="84a69-115">-CertificateName</span></span>
<span data-ttu-id="84a69-116">Anger namnet på ett SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="84a69-116">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="84a69-117">Denna cmdlet lägger till det certifikat som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="84a69-117">This cmdlet adds the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="84a69-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="84a69-118">-Name</span></span>
<span data-ttu-id="84a69-119">Anger namnet på den Programgateway som denna cmdlet lägger till ett SSL-certifikat för.</span><span class="sxs-lookup"><span data-stu-id="84a69-119">Specifies the name of the Application Gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="84a69-120">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="84a69-120">-Password</span></span>
<span data-ttu-id="84a69-121">Anger lösen ordet för det SSL-certifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="84a69-121">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="84a69-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="84a69-122">-Profile</span></span>
<span data-ttu-id="84a69-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="84a69-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="84a69-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="84a69-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="84a69-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a69-125">CommonParameters</span></span>
<span data-ttu-id="84a69-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a69-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a69-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84a69-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a69-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84a69-128">INPUTS</span></span>

### <span data-ttu-id="84a69-129">System. String</span><span class="sxs-lookup"><span data-stu-id="84a69-129">System.String</span></span>

## <span data-ttu-id="84a69-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84a69-130">OUTPUTS</span></span>

### <span data-ttu-id="84a69-131">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="84a69-131">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="84a69-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84a69-132">NOTES</span></span>

## <span data-ttu-id="84a69-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84a69-133">RELATED LINKS</span></span>

[<span data-ttu-id="84a69-134">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="84a69-134">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="84a69-135">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="84a69-135">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
