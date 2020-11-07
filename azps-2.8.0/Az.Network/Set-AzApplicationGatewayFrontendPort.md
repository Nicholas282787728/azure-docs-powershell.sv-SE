---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: cdc1535532aad26ad4e3ee67e5fdd822ee3480e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917958"
---
# <span data-ttu-id="4a640-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4a640-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="4a640-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a640-102">SYNOPSIS</span></span>
<span data-ttu-id="4a640-103">Ändrar frontend-port för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4a640-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="4a640-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a640-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a640-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a640-105">DESCRIPTION</span></span>
<span data-ttu-id="4a640-106">Cmdleten **set-AzApplicationGatewayFrontendPort** ändrar en front port för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4a640-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="4a640-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a640-107">EXAMPLES</span></span>

### <span data-ttu-id="4a640-108">Exempel 1: Ange front-end-port för Application Gateway till 80</span><span class="sxs-lookup"><span data-stu-id="4a640-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="4a640-109">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="4a640-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4a640-110">Det andra kommandot ändrar gatewayen i $AppGw så att port 80 används för front porten som heter FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="4a640-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="4a640-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a640-111">PARAMETERS</span></span>

### <span data-ttu-id="4a640-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a640-112">-ApplicationGateway</span></span>
<span data-ttu-id="4a640-113">Anger det Application Gateway-objekt som denna cmdlet associerar fram porten med.</span><span class="sxs-lookup"><span data-stu-id="4a640-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="4a640-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a640-114">-DefaultProfile</span></span>
<span data-ttu-id="4a640-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a640-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a640-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a640-116">-Name</span></span>
<span data-ttu-id="4a640-117">Anger namnet på den frontend-port som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="4a640-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="4a640-118">-Port</span><span class="sxs-lookup"><span data-stu-id="4a640-118">-Port</span></span>
<span data-ttu-id="4a640-119">Anger vilket port nummer som ska användas för front porten.</span><span class="sxs-lookup"><span data-stu-id="4a640-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a640-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a640-120">CommonParameters</span></span>
<span data-ttu-id="4a640-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a640-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a640-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a640-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a640-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a640-123">INPUTS</span></span>

### <span data-ttu-id="4a640-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a640-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a640-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a640-125">OUTPUTS</span></span>

### <span data-ttu-id="4a640-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a640-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a640-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a640-127">NOTES</span></span>

## <span data-ttu-id="4a640-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a640-128">RELATED LINKS</span></span>

[<span data-ttu-id="4a640-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4a640-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4a640-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4a640-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4a640-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4a640-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4a640-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4a640-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
