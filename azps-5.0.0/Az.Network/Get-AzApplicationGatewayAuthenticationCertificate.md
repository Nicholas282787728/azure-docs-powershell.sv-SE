---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: fbab2b1b9887fa7a5d509b46909f29eb741959bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271596"
---
# <span data-ttu-id="c6e36-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c6e36-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c6e36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6e36-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e36-103">Hämtar ett autentiseringscertifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c6e36-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="c6e36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6e36-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6e36-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6e36-105">DESCRIPTION</span></span>
<span data-ttu-id="c6e36-106">Cmdleten **Get-AzApplicationGatewayAuthenticationCertificate** hämtar ett autentiseringscertifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c6e36-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="c6e36-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6e36-107">EXAMPLES</span></span>

### <span data-ttu-id="c6e36-108">Exempel 1: Hämta ett angivet autentiseringscertifikat</span><span class="sxs-lookup"><span data-stu-id="c6e36-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="c6e36-109">Det första kommandot får programgatewayen som heter appGwName och lagrar den i $appgw variabeln.</span><span class="sxs-lookup"><span data-stu-id="c6e36-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="c6e36-110">Det andra kommandot får autentiseringscertifikatet med namnet pool01 och lagrar det i $pool variabeln.</span><span class="sxs-lookup"><span data-stu-id="c6e36-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="c6e36-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6e36-111">PARAMETERS</span></span>

### <span data-ttu-id="c6e36-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c6e36-112">-ApplicationGateway</span></span>
<span data-ttu-id="c6e36-113">Anger namnet på den Programgateway som denna cmdlet får ett autentiseringscertifikat för.</span><span class="sxs-lookup"><span data-stu-id="c6e36-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="c6e36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e36-114">-DefaultProfile</span></span>
<span data-ttu-id="c6e36-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e36-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6e36-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6e36-116">-Name</span></span>
<span data-ttu-id="c6e36-117">Anger namnet på det autentiseringscertifikat som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c6e36-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c6e36-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e36-118">CommonParameters</span></span>
<span data-ttu-id="c6e36-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e36-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e36-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6e36-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e36-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6e36-121">INPUTS</span></span>

### <span data-ttu-id="c6e36-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c6e36-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c6e36-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6e36-123">OUTPUTS</span></span>

### <span data-ttu-id="c6e36-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c6e36-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c6e36-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6e36-125">NOTES</span></span>
* <span data-ttu-id="c6e36-126">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="c6e36-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c6e36-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6e36-127">RELATED LINKS</span></span>

[<span data-ttu-id="c6e36-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c6e36-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c6e36-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c6e36-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c6e36-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c6e36-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c6e36-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c6e36-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


