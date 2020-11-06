---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: da831810461e763acc51319ea4d6662c45a1c3ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576714"
---
# <span data-ttu-id="1f6d1-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1f6d1-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="1f6d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6d1-103">Hämtar ett SSL-certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f6d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f6d1-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f6d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f6d1-105">DESCRIPTION</span></span>
<span data-ttu-id="1f6d1-106">Cmdleten **Get-AzureRmApplicationGatewaySslCertificate** får ett SSL-certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="1f6d1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f6d1-107">EXAMPLES</span></span>

### <span data-ttu-id="1f6d1-108">Exempel 1: skaffa ett specifikt SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="1f6d1-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="1f6d1-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="1f6d1-110">Det andra kommandot får SSL-certifikatet som heter Cert01 från den Application Gateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="1f6d1-111">Kommandot lagrar certifikatet i variabeln som heter $Cert.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="1f6d1-112">Exempel 2: skaffa en lista över SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="1f6d1-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="1f6d1-113">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="1f6d1-114">Det andra kommandot får en lista med SSL-certifikat från den Programgateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="1f6d1-115">Då sparas resultaten i variabeln $Certs.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="1f6d1-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f6d1-116">PARAMETERS</span></span>

### <span data-ttu-id="1f6d1-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f6d1-117">-ApplicationGateway</span></span>
<span data-ttu-id="1f6d1-118">Anger det Application Gateway-objekt som innehåller SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f6d1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f6d1-119">-Name</span></span>
<span data-ttu-id="1f6d1-120">Anger namnet på den SSL-certifikatmall som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-120">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1f6d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6d1-121">-DefaultProfile</span></span>
<span data-ttu-id="1f6d1-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f6d1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6d1-123">CommonParameters</span></span>
<span data-ttu-id="1f6d1-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f6d1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6d1-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f6d1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6d1-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f6d1-126">INPUTS</span></span>

### <span data-ttu-id="1f6d1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1f6d1-127">System.String</span></span>

## <span data-ttu-id="1f6d1-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f6d1-128">OUTPUTS</span></span>

### <span data-ttu-id="1f6d1-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1f6d1-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="1f6d1-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f6d1-130">NOTES</span></span>

## <span data-ttu-id="1f6d1-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f6d1-131">RELATED LINKS</span></span>

[<span data-ttu-id="1f6d1-132">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1f6d1-132">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1f6d1-133">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1f6d1-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1f6d1-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1f6d1-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1f6d1-135">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1f6d1-135">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


