---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b03d35b511bafefe0ba062eb15a9c1eee8961585
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259281"
---
# <span data-ttu-id="edd2d-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="edd2d-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="edd2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="edd2d-102">SYNOPSIS</span></span>
<span data-ttu-id="edd2d-103">Tar bort ett SSL-certifikat från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="edd2d-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="edd2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="edd2d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edd2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="edd2d-105">DESCRIPTION</span></span>
<span data-ttu-id="edd2d-106">Cmdleten **Remove-AzApplicationGatewaySslCertificate** tar bort ett SSL-certifikat från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="edd2d-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="edd2d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="edd2d-107">EXAMPLES</span></span>

### <span data-ttu-id="edd2d-108">Exempel 1: ta bort ett SSL-certifikat från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="edd2d-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="edd2d-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="edd2d-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="edd2d-110">Det andra kommandot tar bort SSL-certifikatet som heter Cert02 från Application Gateway som lagras i $AppGW variabel.</span><span class="sxs-lookup"><span data-stu-id="edd2d-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="edd2d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="edd2d-111">PARAMETERS</span></span>

### <span data-ttu-id="edd2d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="edd2d-112">-ApplicationGateway</span></span>
<span data-ttu-id="edd2d-113">Anger den Programgateway som den här cmdleten tar bort ett SSL-certifikat från.</span><span class="sxs-lookup"><span data-stu-id="edd2d-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="edd2d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd2d-114">-DefaultProfile</span></span>
<span data-ttu-id="edd2d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="edd2d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edd2d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="edd2d-116">-Name</span></span>
<span data-ttu-id="edd2d-117">Anger namnet på ett SSL-certifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="edd2d-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd2d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd2d-118">CommonParameters</span></span>
<span data-ttu-id="edd2d-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd2d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd2d-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd2d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd2d-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="edd2d-121">INPUTS</span></span>

### <span data-ttu-id="edd2d-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="edd2d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="edd2d-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="edd2d-123">OUTPUTS</span></span>

### <span data-ttu-id="edd2d-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="edd2d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="edd2d-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="edd2d-125">NOTES</span></span>

## <span data-ttu-id="edd2d-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="edd2d-126">RELATED LINKS</span></span>

[<span data-ttu-id="edd2d-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="edd2d-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="edd2d-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="edd2d-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="edd2d-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="edd2d-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="edd2d-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="edd2d-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)

