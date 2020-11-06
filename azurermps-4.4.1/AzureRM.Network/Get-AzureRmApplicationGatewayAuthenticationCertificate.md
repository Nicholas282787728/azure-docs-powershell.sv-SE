---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 846cdf57e78ca1d3bacb7673d23fd16d460e4400
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574616"
---
# <span data-ttu-id="b9818-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9818-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b9818-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9818-102">SYNOPSIS</span></span>
<span data-ttu-id="b9818-103">Hämtar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b9818-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9818-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9818-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9818-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9818-105">DESCRIPTION</span></span>
<span data-ttu-id="b9818-106">Cmdleten **Get-AzureRmApplicationGatewayAuthenticationCertificate** hämtar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b9818-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b9818-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9818-107">EXAMPLES</span></span>

## <span data-ttu-id="b9818-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9818-108">PARAMETERS</span></span>

### <span data-ttu-id="b9818-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9818-109">-ApplicationGateway</span></span>
<span data-ttu-id="b9818-110">Anger namnet på den Programgateway som denna cmdlet får ett autentiseringscertifikat för.</span><span class="sxs-lookup"><span data-stu-id="b9818-110">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="b9818-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9818-111">-Name</span></span>
<span data-ttu-id="b9818-112">Anger namnet på det autentiseringscertifikat som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="b9818-112">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b9818-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9818-113">-DefaultProfile</span></span>
<span data-ttu-id="b9818-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9818-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9818-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9818-115">CommonParameters</span></span>
<span data-ttu-id="b9818-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9818-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9818-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9818-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9818-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9818-118">INPUTS</span></span>

### <span data-ttu-id="b9818-119">System. String</span><span class="sxs-lookup"><span data-stu-id="b9818-119">System.String</span></span>

## <span data-ttu-id="b9818-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9818-120">OUTPUTS</span></span>

### <span data-ttu-id="b9818-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9818-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b9818-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9818-122">NOTES</span></span>
* <span data-ttu-id="b9818-123">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="b9818-123">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b9818-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9818-124">RELATED LINKS</span></span>

[<span data-ttu-id="b9818-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9818-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9818-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9818-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9818-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9818-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9818-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9818-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


