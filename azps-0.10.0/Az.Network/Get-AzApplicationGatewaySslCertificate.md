---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 62c73fe60e147ca34083851db50c3830198dd60e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922317"
---
# <span data-ttu-id="c6416-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c6416-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c6416-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6416-102">SYNOPSIS</span></span>
<span data-ttu-id="c6416-103">Hämtar ett SSL-certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c6416-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="c6416-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6416-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6416-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6416-105">DESCRIPTION</span></span>
<span data-ttu-id="c6416-106">Cmdleten **Get-AzApplicationGatewaySslCertificate** får ett SSL-certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c6416-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="c6416-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6416-107">EXAMPLES</span></span>

### <span data-ttu-id="c6416-108">Exempel 1: skaffa ett specifikt SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="c6416-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="c6416-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c6416-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c6416-110">Det andra kommandot får SSL-certifikatet som heter Cert01 från den Application Gateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c6416-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="c6416-111">Kommandot lagrar certifikatet i variabeln som heter $Cert.</span><span class="sxs-lookup"><span data-stu-id="c6416-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="c6416-112">Exempel 2: skaffa en lista över SSL-certifikat</span><span class="sxs-lookup"><span data-stu-id="c6416-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="c6416-113">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c6416-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c6416-114">Det andra kommandot får en lista med SSL-certifikat från den Programgateway som lagras i variabeln $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c6416-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="c6416-115">Då sparas resultaten i variabeln $Certs.</span><span class="sxs-lookup"><span data-stu-id="c6416-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="c6416-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6416-116">PARAMETERS</span></span>

### <span data-ttu-id="c6416-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c6416-117">-ApplicationGateway</span></span>
<span data-ttu-id="c6416-118">Anger det Application Gateway-objekt som innehåller SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c6416-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6416-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6416-119">-DefaultProfile</span></span>
<span data-ttu-id="c6416-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6416-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6416-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6416-121">-Name</span></span>
<span data-ttu-id="c6416-122">Anger namnet på den SSL-certifikatmall som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c6416-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c6416-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6416-123">CommonParameters</span></span>
<span data-ttu-id="c6416-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6416-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6416-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6416-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6416-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6416-126">INPUTS</span></span>

### <span data-ttu-id="c6416-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c6416-127">System.String</span></span>

## <span data-ttu-id="c6416-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6416-128">OUTPUTS</span></span>

### <span data-ttu-id="c6416-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c6416-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c6416-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6416-130">NOTES</span></span>

## <span data-ttu-id="c6416-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6416-131">RELATED LINKS</span></span>

[<span data-ttu-id="c6416-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c6416-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c6416-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c6416-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c6416-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c6416-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c6416-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c6416-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


