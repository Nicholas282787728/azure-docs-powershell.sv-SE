---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 033ca62f766f854be27ad75a6b63a8f883ba58d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931341"
---
# <span data-ttu-id="0717c-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0717c-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="0717c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0717c-102">SYNOPSIS</span></span>
<span data-ttu-id="0717c-103">Hämtar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0717c-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0717c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0717c-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0717c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0717c-105">DESCRIPTION</span></span>
<span data-ttu-id="0717c-106">Cmdleten **Get-AzureRmApplicationGatewayAuthenticationCertificate** hämtar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0717c-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="0717c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0717c-107">EXAMPLES</span></span>

### <span data-ttu-id="0717c-108">9.1</span><span class="sxs-lookup"><span data-stu-id="0717c-108">1:</span></span>
```

```

## <span data-ttu-id="0717c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0717c-109">PARAMETERS</span></span>

### <span data-ttu-id="0717c-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0717c-110">-ApplicationGateway</span></span>
<span data-ttu-id="0717c-111">Anger namnet på den Programgateway som denna cmdlet får ett autentiseringscertifikat för.</span><span class="sxs-lookup"><span data-stu-id="0717c-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="0717c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0717c-112">-DefaultProfile</span></span>
<span data-ttu-id="0717c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0717c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0717c-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="0717c-114">-Name</span></span>
<span data-ttu-id="0717c-115">Anger namnet på det autentiseringscertifikat som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="0717c-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0717c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0717c-116">CommonParameters</span></span>
<span data-ttu-id="0717c-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0717c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0717c-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0717c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0717c-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0717c-119">INPUTS</span></span>

### <span data-ttu-id="0717c-120">System. String</span><span class="sxs-lookup"><span data-stu-id="0717c-120">System.String</span></span>

## <span data-ttu-id="0717c-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0717c-121">OUTPUTS</span></span>

### <span data-ttu-id="0717c-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0717c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="0717c-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0717c-123">NOTES</span></span>
* <span data-ttu-id="0717c-124">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="0717c-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0717c-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0717c-125">RELATED LINKS</span></span>

[<span data-ttu-id="0717c-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0717c-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0717c-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0717c-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0717c-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0717c-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0717c-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0717c-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


