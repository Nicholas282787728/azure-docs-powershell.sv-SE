---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 30f47cf6e345710da0e0d626929f65a33490e246
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091279"
---
# <span data-ttu-id="223d1-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="223d1-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="223d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="223d1-102">SYNOPSIS</span></span>
<span data-ttu-id="223d1-103">Hämtar HTTP-lyssnaren för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="223d1-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="223d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="223d1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="223d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="223d1-105">DESCRIPTION</span></span>
<span data-ttu-id="223d1-106">Cmdleten **Get-AzApplicationGatewayHttpListener** hämtar http-lyssnaren för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="223d1-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="223d1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="223d1-107">EXAMPLES</span></span>

### <span data-ttu-id="223d1-108">Exempel 1: skaffa en viss HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="223d1-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="223d1-109">Det här kommandot får en HTTP-lyssnare som heter Listener01.</span><span class="sxs-lookup"><span data-stu-id="223d1-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="223d1-110">Exempel 2: Hämta en lista med HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="223d1-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="223d1-111">Det här kommandot får en lista med HTTP-lyssnare.</span><span class="sxs-lookup"><span data-stu-id="223d1-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="223d1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="223d1-112">PARAMETERS</span></span>

### <span data-ttu-id="223d1-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="223d1-113">-ApplicationGateway</span></span>
<span data-ttu-id="223d1-114">Anger det Application Gateway-objekt som innehåller HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="223d1-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="223d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="223d1-115">-DefaultProfile</span></span>
<span data-ttu-id="223d1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="223d1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="223d1-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="223d1-117">-Name</span></span>
<span data-ttu-id="223d1-118">Anger namnet på den HTTP-lyssnare som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="223d1-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="223d1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="223d1-119">CommonParameters</span></span>
<span data-ttu-id="223d1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="223d1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="223d1-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="223d1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="223d1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="223d1-122">INPUTS</span></span>

### <span data-ttu-id="223d1-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="223d1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="223d1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="223d1-124">OUTPUTS</span></span>

### <span data-ttu-id="223d1-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="223d1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="223d1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="223d1-126">NOTES</span></span>

## <span data-ttu-id="223d1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="223d1-127">RELATED LINKS</span></span>

[<span data-ttu-id="223d1-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="223d1-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="223d1-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="223d1-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="223d1-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="223d1-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="223d1-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="223d1-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)

