---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: 7b83e7f8ca372faf8158e248d326595a0d162d6a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929042"
---
# <span data-ttu-id="ff69a-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff69a-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ff69a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff69a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff69a-103">Hämtar WAF konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ff69a-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff69a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff69a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff69a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff69a-105">DESCRIPTION</span></span>
<span data-ttu-id="ff69a-106">Cmdleten **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** hämtar webb program brand väggen (WAF) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ff69a-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="ff69a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff69a-107">EXAMPLES</span></span>

### <span data-ttu-id="ff69a-108">Exempel 1: Hämta en brand Väggs konfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ff69a-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="ff69a-109">Det första kommandot hämtar programgatewayen med namnet ApplicationGateway01 och lagrar den sedan i $AppGW variabel.</span><span class="sxs-lookup"><span data-stu-id="ff69a-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="ff69a-110">Det andra kommandot får brand Väggs konfigurationen för programgatewayen i $AppGW och lagrar den sedan i $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="ff69a-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="ff69a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff69a-111">PARAMETERS</span></span>

### <span data-ttu-id="ff69a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff69a-112">-ApplicationGateway</span></span>
<span data-ttu-id="ff69a-113">Anger ett Application Gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="ff69a-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="ff69a-114">Du kan använda Get-AzureRmApplicationGateway cmdlet för att hämta ett objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ff69a-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="ff69a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff69a-115">-DefaultProfile</span></span>
<span data-ttu-id="ff69a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff69a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff69a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff69a-117">CommonParameters</span></span>
<span data-ttu-id="ff69a-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff69a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff69a-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff69a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff69a-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff69a-120">INPUTS</span></span>

### <span data-ttu-id="ff69a-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff69a-121">PSApplicationGateway</span></span>
<span data-ttu-id="ff69a-122">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ff69a-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ff69a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff69a-123">OUTPUTS</span></span>

### <span data-ttu-id="ff69a-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff69a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ff69a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff69a-125">NOTES</span></span>

## <span data-ttu-id="ff69a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff69a-126">RELATED LINKS</span></span>

[<span data-ttu-id="ff69a-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff69a-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="ff69a-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff69a-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="ff69a-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff69a-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


