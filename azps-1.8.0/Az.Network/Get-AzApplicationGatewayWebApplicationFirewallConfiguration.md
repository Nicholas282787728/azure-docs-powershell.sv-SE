---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: e2f477aa657bc4d21a650edffb7f014ae3c1ba62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748348"
---
# <span data-ttu-id="9b2c2-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b2c2-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="9b2c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2c2-103">Hämtar WAF konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="9b2c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b2c2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b2c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b2c2-105">DESCRIPTION</span></span>
<span data-ttu-id="9b2c2-106">Cmdleten **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** hämtar webb program brand väggen (WAF) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="9b2c2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b2c2-107">EXAMPLES</span></span>

### <span data-ttu-id="9b2c2-108">Exempel 1: Hämta en brand Väggs konfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="9b2c2-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="9b2c2-109">Det första kommandot hämtar programgatewayen med namnet ApplicationGateway01 och lagrar den sedan i $AppGW variabel.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="9b2c2-110">Det andra kommandot får brand Väggs konfigurationen för programgatewayen i $AppGW och lagrar den sedan i $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="9b2c2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b2c2-111">PARAMETERS</span></span>

### <span data-ttu-id="9b2c2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b2c2-112">-ApplicationGateway</span></span>
<span data-ttu-id="9b2c2-113">Anger ett Application Gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="9b2c2-114">Du kan använda Get-AzApplicationGateway cmdlet för att hämta ett objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="9b2c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2c2-115">-DefaultProfile</span></span>
<span data-ttu-id="9b2c2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b2c2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2c2-117">CommonParameters</span></span>
<span data-ttu-id="9b2c2-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b2c2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2c2-119">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b2c2-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2c2-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b2c2-120">INPUTS</span></span>

### <span data-ttu-id="9b2c2-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b2c2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b2c2-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b2c2-122">OUTPUTS</span></span>

### <span data-ttu-id="9b2c2-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b2c2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="9b2c2-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b2c2-124">NOTES</span></span>

## <span data-ttu-id="9b2c2-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b2c2-125">RELATED LINKS</span></span>

[<span data-ttu-id="9b2c2-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b2c2-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="9b2c2-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b2c2-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="9b2c2-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b2c2-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

