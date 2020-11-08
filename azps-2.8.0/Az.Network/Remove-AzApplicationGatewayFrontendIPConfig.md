---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 72cc21b697b2dbdc05ad7106fca5687203aec870
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918133"
---
# <span data-ttu-id="8d274-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8d274-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="8d274-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d274-102">SYNOPSIS</span></span>
<span data-ttu-id="8d274-103">Tar bort en front-IP-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8d274-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="8d274-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d274-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d274-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d274-105">DESCRIPTION</span></span>
<span data-ttu-id="8d274-106">Cmdleten **Remove-AzApplicationGatewayFrontendIPConfig** tar bort nät ports-IP från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8d274-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="8d274-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d274-107">EXAMPLES</span></span>

### <span data-ttu-id="8d274-108">Exempel 1: ta bort en front-IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="8d274-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="8d274-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="8d274-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8d274-110">Det andra kommandot tar bort front-IP-konfigurationen som heter FrontEndIP02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8d274-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="8d274-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d274-111">PARAMETERS</span></span>

### <span data-ttu-id="8d274-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d274-112">-ApplicationGateway</span></span>
<span data-ttu-id="8d274-113">Anger en Programgateway från vilken en front-IP-konfiguration ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8d274-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="8d274-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d274-114">-DefaultProfile</span></span>
<span data-ttu-id="8d274-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d274-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d274-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="8d274-116">-Name</span></span>
<span data-ttu-id="8d274-117">Anger namnet på en klient konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8d274-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="8d274-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d274-118">CommonParameters</span></span>
<span data-ttu-id="8d274-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d274-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d274-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d274-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d274-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d274-121">INPUTS</span></span>

### <span data-ttu-id="8d274-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d274-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d274-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d274-123">OUTPUTS</span></span>

### <span data-ttu-id="8d274-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d274-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d274-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d274-125">NOTES</span></span>

## <span data-ttu-id="8d274-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d274-126">RELATED LINKS</span></span>

[<span data-ttu-id="8d274-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8d274-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="8d274-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8d274-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="8d274-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8d274-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="8d274-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8d274-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)

