---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1efce67698ca6d2e3a8bc9eeab3d89e00e1833f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389451"
---
# <span data-ttu-id="c6fd0-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c6fd0-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="c6fd0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="c6fd0-103">Hämtar klientens front-IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c6fd0-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="c6fd0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6fd0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6fd0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="c6fd0-106">Cmdleten **Get-AzApplicationGatewayFrontendIPConfig** hämtar klientens front-IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c6fd0-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="c6fd0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6fd0-107">EXAMPLES</span></span>

### <span data-ttu-id="c6fd0-108">Exempel 1: Hämta en viss front-IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="c6fd0-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="c6fd0-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 från resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot får klient konfigurationen front-end som heter FrontEndIP01 från $AppGw och lagrar den i $FrontEndIP-variabeln.</span><span class="sxs-lookup"><span data-stu-id="c6fd0-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="c6fd0-110">Exempel 2: Hämta en lista över front-IP-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="c6fd0-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="c6fd0-111">Det första kommandot får en Programgateway som heter ApplicationGateway01 från resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot får en lista med front-IP-konfigurationer från $AppGw och lagrar dem i $FrontEndIPs-variabeln.</span><span class="sxs-lookup"><span data-stu-id="c6fd0-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="c6fd0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6fd0-112">PARAMETERS</span></span>

### <span data-ttu-id="c6fd0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c6fd0-113">-ApplicationGateway</span></span>
<span data-ttu-id="c6fd0-114">Anger det Application Gateway-objekt som innehåller front-IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c6fd0-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="c6fd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6fd0-115">-DefaultProfile</span></span>
<span data-ttu-id="c6fd0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6fd0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6fd0-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6fd0-117">-Name</span></span>
<span data-ttu-id="c6fd0-118">Anger namnet på den front-end IP-konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="c6fd0-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c6fd0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6fd0-119">CommonParameters</span></span>
<span data-ttu-id="c6fd0-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6fd0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6fd0-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6fd0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6fd0-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6fd0-122">INPUTS</span></span>

### <span data-ttu-id="c6fd0-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c6fd0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c6fd0-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6fd0-124">OUTPUTS</span></span>

### <span data-ttu-id="c6fd0-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6fd0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="c6fd0-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6fd0-126">NOTES</span></span>

## <span data-ttu-id="c6fd0-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6fd0-127">RELATED LINKS</span></span>

[<span data-ttu-id="c6fd0-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c6fd0-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c6fd0-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c6fd0-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c6fd0-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c6fd0-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c6fd0-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c6fd0-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


