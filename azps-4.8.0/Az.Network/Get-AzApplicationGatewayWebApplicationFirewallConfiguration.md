---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9a27e88557bd263df3f08ce8e6d43ea26faa67b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258842"
---
# <span data-ttu-id="ed40e-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed40e-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ed40e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed40e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed40e-103">Hämtar WAF konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ed40e-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="ed40e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed40e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed40e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed40e-105">DESCRIPTION</span></span>
<span data-ttu-id="ed40e-106">Cmdleten **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** hämtar webb program brand väggen (WAF) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ed40e-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="ed40e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed40e-107">EXAMPLES</span></span>

### <span data-ttu-id="ed40e-108">Exempel 1: Hämta en brand Väggs konfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ed40e-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="ed40e-109">Det första kommandot hämtar programgatewayen med namnet ApplicationGateway01 och lagrar den sedan i $AppGW variabel.</span><span class="sxs-lookup"><span data-stu-id="ed40e-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="ed40e-110">Det andra kommandot får brand Väggs konfigurationen för programgatewayen i $AppGW och lagrar den sedan i $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="ed40e-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="ed40e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed40e-111">PARAMETERS</span></span>

### <span data-ttu-id="ed40e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed40e-112">-ApplicationGateway</span></span>
<span data-ttu-id="ed40e-113">Anger ett Application Gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="ed40e-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="ed40e-114">Du kan använda Get-AzApplicationGateway cmdlet för att hämta ett objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ed40e-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="ed40e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed40e-115">-DefaultProfile</span></span>
<span data-ttu-id="ed40e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed40e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed40e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed40e-117">CommonParameters</span></span>
<span data-ttu-id="ed40e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed40e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed40e-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed40e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed40e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed40e-120">INPUTS</span></span>

### <span data-ttu-id="ed40e-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed40e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed40e-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed40e-122">OUTPUTS</span></span>

### <span data-ttu-id="ed40e-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed40e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ed40e-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed40e-124">NOTES</span></span>

## <span data-ttu-id="ed40e-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed40e-125">RELATED LINKS</span></span>

[<span data-ttu-id="ed40e-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed40e-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="ed40e-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed40e-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="ed40e-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed40e-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


