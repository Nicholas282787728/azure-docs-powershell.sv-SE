---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9eaaa8ae6ec4be7a1096bfd9de4a3e20c0cb5ff1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918580"
---
# <span data-ttu-id="a0390-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a0390-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="a0390-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0390-102">SYNOPSIS</span></span>
<span data-ttu-id="a0390-103">Lägger till en frontend-port till en programport.</span><span class="sxs-lookup"><span data-stu-id="a0390-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="a0390-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0390-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0390-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0390-105">DESCRIPTION</span></span>
<span data-ttu-id="a0390-106">Cmdleten **Add-AzApplicationGatewayFrontendPort** lägger till en frontend-port till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a0390-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="a0390-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0390-107">EXAMPLES</span></span>

### <span data-ttu-id="a0390-108">Exempel 1: lägga till en front port i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="a0390-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="a0390-109">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="a0390-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a0390-110">Det andra kommandot lägger till port 80 som front port för programgatewayen som lagras i $AppGw och namnger porten FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="a0390-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="a0390-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0390-111">PARAMETERS</span></span>

### <span data-ttu-id="a0390-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0390-112">-ApplicationGateway</span></span>
<span data-ttu-id="a0390-113">Anger den Programgateway till vilken denna cmdlet lägger till en front port.</span><span class="sxs-lookup"><span data-stu-id="a0390-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="a0390-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0390-114">-DefaultProfile</span></span>
<span data-ttu-id="a0390-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0390-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0390-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0390-116">-Name</span></span>
<span data-ttu-id="a0390-117">Anger namnet på front porten.</span><span class="sxs-lookup"><span data-stu-id="a0390-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="a0390-118">-Port</span><span class="sxs-lookup"><span data-stu-id="a0390-118">-Port</span></span>
<span data-ttu-id="a0390-119">Anger port numret.</span><span class="sxs-lookup"><span data-stu-id="a0390-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="a0390-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0390-120">CommonParameters</span></span>
<span data-ttu-id="a0390-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0390-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0390-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0390-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0390-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0390-123">INPUTS</span></span>

### <span data-ttu-id="a0390-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0390-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0390-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0390-125">OUTPUTS</span></span>

### <span data-ttu-id="a0390-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0390-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0390-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0390-127">NOTES</span></span>

## <span data-ttu-id="a0390-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0390-128">RELATED LINKS</span></span>

[<span data-ttu-id="a0390-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a0390-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a0390-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a0390-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a0390-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a0390-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a0390-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a0390-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


