---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102723"
---
# <span data-ttu-id="355a6-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="355a6-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="355a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="355a6-102">SYNOPSIS</span></span>
<span data-ttu-id="355a6-103">Hämtar front porten för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="355a6-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="355a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="355a6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="355a6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="355a6-105">DESCRIPTION</span></span>
<span data-ttu-id="355a6-106">Cmdleten **Get-AzApplicationGatewayFrontendPort** får fram front porten för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="355a6-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="355a6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="355a6-107">EXAMPLES</span></span>

### <span data-ttu-id="355a6-108">Exempel 1: skaffa en viss front port</span><span class="sxs-lookup"><span data-stu-id="355a6-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="355a6-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 från resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="355a6-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="355a6-110">Det andra kommandot får fram porten som heter FrontEndPort01 från $AppGw och lagrar den i $FrontEndPort-variabeln.</span><span class="sxs-lookup"><span data-stu-id="355a6-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="355a6-111">Exempel 2: Hämta en lista över front portar</span><span class="sxs-lookup"><span data-stu-id="355a6-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="355a6-112">Det första kommandot får en Programgateway som heter ApplicationGateway01 från resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="355a6-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="355a6-113">Det andra kommandot får en lista över front portarna från $AppGw och lagrar dem i $FrontEndPorts-variabeln.</span><span class="sxs-lookup"><span data-stu-id="355a6-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="355a6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="355a6-114">PARAMETERS</span></span>

### <span data-ttu-id="355a6-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="355a6-115">-ApplicationGateway</span></span>
<span data-ttu-id="355a6-116">Anger den Application Gateway-objekt som innehåller front porten.</span><span class="sxs-lookup"><span data-stu-id="355a6-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="355a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="355a6-117">-DefaultProfile</span></span>
<span data-ttu-id="355a6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="355a6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="355a6-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="355a6-119">-Name</span></span>
<span data-ttu-id="355a6-120">Anger namnet på front porten som ska visas.</span><span class="sxs-lookup"><span data-stu-id="355a6-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="355a6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="355a6-121">CommonParameters</span></span>
<span data-ttu-id="355a6-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="355a6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="355a6-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="355a6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="355a6-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="355a6-124">INPUTS</span></span>

### <span data-ttu-id="355a6-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="355a6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="355a6-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="355a6-126">OUTPUTS</span></span>

### <span data-ttu-id="355a6-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="355a6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="355a6-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="355a6-128">NOTES</span></span>

## <span data-ttu-id="355a6-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="355a6-129">RELATED LINKS</span></span>

[<span data-ttu-id="355a6-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="355a6-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="355a6-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="355a6-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="355a6-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="355a6-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="355a6-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="355a6-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


