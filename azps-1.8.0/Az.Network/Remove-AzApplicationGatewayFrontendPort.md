---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: bb37c72368832ee4bbccb6e4c10a227e72ba127f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747943"
---
# <span data-ttu-id="f1dab-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f1dab-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f1dab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1dab-102">SYNOPSIS</span></span>
<span data-ttu-id="f1dab-103">Tar bort en front port från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f1dab-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="f1dab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1dab-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1dab-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1dab-105">DESCRIPTION</span></span>
<span data-ttu-id="f1dab-106">Cmdleten **Remove-AzApplicationGatewayFrontendPort** tar bort en front port från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1dab-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="f1dab-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1dab-107">EXAMPLES</span></span>

### <span data-ttu-id="f1dab-108">Exempel: ta bort en klient port från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="f1dab-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="f1dab-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar gatewayen i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="f1dab-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="f1dab-110">Det andra kommandot tar bort porten som heter FrontEndPort02 från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1dab-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="f1dab-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1dab-111">PARAMETERS</span></span>

### <span data-ttu-id="f1dab-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1dab-112">-ApplicationGateway</span></span>
<span data-ttu-id="f1dab-113">Anger den Programgateway från vilken du vill ta bort en front port.</span><span class="sxs-lookup"><span data-stu-id="f1dab-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="f1dab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1dab-114">-DefaultProfile</span></span>
<span data-ttu-id="f1dab-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f1dab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1dab-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1dab-116">-Name</span></span>
<span data-ttu-id="f1dab-117">Anger namnet på klient delen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f1dab-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="f1dab-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1dab-118">CommonParameters</span></span>
<span data-ttu-id="f1dab-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1dab-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1dab-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1dab-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1dab-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1dab-121">INPUTS</span></span>

### <span data-ttu-id="f1dab-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1dab-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1dab-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1dab-123">OUTPUTS</span></span>

### <span data-ttu-id="f1dab-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1dab-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1dab-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1dab-125">NOTES</span></span>

## <span data-ttu-id="f1dab-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1dab-126">RELATED LINKS</span></span>

[<span data-ttu-id="f1dab-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f1dab-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f1dab-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f1dab-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f1dab-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f1dab-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f1dab-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f1dab-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)

