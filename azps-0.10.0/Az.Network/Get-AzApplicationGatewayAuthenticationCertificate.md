---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 465567242c0ff13ea695c767cf1dda7f04f54174
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922342"
---
# <span data-ttu-id="62116-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="62116-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="62116-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62116-102">SYNOPSIS</span></span>
<span data-ttu-id="62116-103">Hämtar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="62116-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="62116-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62116-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62116-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62116-105">DESCRIPTION</span></span>
<span data-ttu-id="62116-106">Cmdleten **Get-AzApplicationGatewayAuthenticationCertificate** hämtar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="62116-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="62116-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62116-107">EXAMPLES</span></span>

### <span data-ttu-id="62116-108">9.1</span><span class="sxs-lookup"><span data-stu-id="62116-108">1:</span></span>
```

```

## <span data-ttu-id="62116-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62116-109">PARAMETERS</span></span>

### <span data-ttu-id="62116-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62116-110">-ApplicationGateway</span></span>
<span data-ttu-id="62116-111">Anger namnet på den Programgateway som denna cmdlet får ett autentiseringscertifikat för.</span><span class="sxs-lookup"><span data-stu-id="62116-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="62116-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62116-112">-DefaultProfile</span></span>
<span data-ttu-id="62116-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62116-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62116-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="62116-114">-Name</span></span>
<span data-ttu-id="62116-115">Anger namnet på det autentiseringscertifikat som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="62116-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="62116-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62116-116">CommonParameters</span></span>
<span data-ttu-id="62116-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62116-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62116-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62116-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62116-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62116-119">INPUTS</span></span>

### <span data-ttu-id="62116-120">System. String</span><span class="sxs-lookup"><span data-stu-id="62116-120">System.String</span></span>

## <span data-ttu-id="62116-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62116-121">OUTPUTS</span></span>

### <span data-ttu-id="62116-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="62116-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="62116-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62116-123">NOTES</span></span>
* <span data-ttu-id="62116-124">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="62116-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="62116-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62116-125">RELATED LINKS</span></span>

[<span data-ttu-id="62116-126">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="62116-126">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="62116-127">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="62116-127">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="62116-128">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="62116-128">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="62116-129">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="62116-129">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


