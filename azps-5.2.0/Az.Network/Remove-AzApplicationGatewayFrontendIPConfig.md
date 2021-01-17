---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d376bc1e70d0441f139b64c19466a88daf6877c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398256"
---
# <span data-ttu-id="0e1ca-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0e1ca-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="0e1ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1ca-103">Tar bort en front-IP-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0e1ca-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="0e1ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e1ca-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e1ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="0e1ca-106">Cmdleten **Remove-AzApplicationGatewayFrontendIPConfig** tar bort nät ports-IP från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0e1ca-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="0e1ca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e1ca-107">EXAMPLES</span></span>

### <span data-ttu-id="0e1ca-108">Exempel 1: ta bort en front-IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="0e1ca-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="0e1ca-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="0e1ca-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0e1ca-110">Det andra kommandot tar bort front-IP-konfigurationen som heter FrontEndIP02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0e1ca-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0e1ca-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e1ca-111">PARAMETERS</span></span>

### <span data-ttu-id="0e1ca-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e1ca-112">-ApplicationGateway</span></span>
<span data-ttu-id="0e1ca-113">Anger en Programgateway från vilken en front-IP-konfiguration ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0e1ca-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0e1ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e1ca-114">-DefaultProfile</span></span>
<span data-ttu-id="0e1ca-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e1ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e1ca-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e1ca-116">-Name</span></span>
<span data-ttu-id="0e1ca-117">Anger namnet på en klient konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0e1ca-117">Specifies the name of a front-end IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e1ca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1ca-118">CommonParameters</span></span>
<span data-ttu-id="0e1ca-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e1ca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1ca-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e1ca-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1ca-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e1ca-121">INPUTS</span></span>

### <span data-ttu-id="0e1ca-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e1ca-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e1ca-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e1ca-123">OUTPUTS</span></span>

### <span data-ttu-id="0e1ca-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e1ca-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e1ca-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e1ca-125">NOTES</span></span>

## <span data-ttu-id="0e1ca-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e1ca-126">RELATED LINKS</span></span>

[<span data-ttu-id="0e1ca-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0e1ca-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0e1ca-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0e1ca-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0e1ca-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0e1ca-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0e1ca-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0e1ca-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


