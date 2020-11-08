---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c1c630c39039d39b1957ccab78bb96d8f085176c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269195"
---
# <span data-ttu-id="a3d76-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a3d76-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="a3d76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3d76-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d76-103">Tar bort en regel för en anslutningsbegäran från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a3d76-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="a3d76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3d76-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3d76-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3d76-105">DESCRIPTION</span></span>
<span data-ttu-id="a3d76-106">Cmdleten **Remove-AzApplicationGatewayRequestRoutingRule** tar bort en regel för anslutningsbegäran från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a3d76-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="a3d76-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3d76-107">EXAMPLES</span></span>

### <span data-ttu-id="a3d76-108">Exempel 1: ta bort en regel för en anslutningsbegäran från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="a3d76-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="a3d76-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="a3d76-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a3d76-110">Det andra kommandot tar bort regeln för anslutningsbegäran med namnet Rule02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a3d76-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a3d76-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3d76-111">PARAMETERS</span></span>

### <span data-ttu-id="a3d76-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3d76-112">-ApplicationGateway</span></span>
<span data-ttu-id="a3d76-113">Anger den Programgateway från vilken en anslutningsbegäran ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a3d76-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="a3d76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d76-114">-DefaultProfile</span></span>
<span data-ttu-id="a3d76-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3d76-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3d76-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3d76-116">-Name</span></span>
<span data-ttu-id="a3d76-117">Anger namnet på regeln för anslutningsbegäran som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a3d76-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="a3d76-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d76-118">CommonParameters</span></span>
<span data-ttu-id="a3d76-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d76-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d76-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3d76-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d76-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3d76-121">INPUTS</span></span>

### <span data-ttu-id="a3d76-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3d76-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3d76-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3d76-123">OUTPUTS</span></span>

### <span data-ttu-id="a3d76-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a3d76-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="a3d76-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3d76-125">NOTES</span></span>

## <span data-ttu-id="a3d76-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3d76-126">RELATED LINKS</span></span>

[<span data-ttu-id="a3d76-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a3d76-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a3d76-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a3d76-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a3d76-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a3d76-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a3d76-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a3d76-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


