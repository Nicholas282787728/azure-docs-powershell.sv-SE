---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: beceb6788fd2d7498fc886cfbc22aec5ad3a9e23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918130"
---
# <span data-ttu-id="0825e-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0825e-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="0825e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0825e-102">SYNOPSIS</span></span>
<span data-ttu-id="0825e-103">Tar bort en HTTP-lyssnare från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0825e-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="0825e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0825e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0825e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0825e-105">DESCRIPTION</span></span>
<span data-ttu-id="0825e-106">Cmdleten **Remove-AzApplicationGatewayHttpListener** tar bort en http-lyssnare från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0825e-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="0825e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0825e-107">EXAMPLES</span></span>

### <span data-ttu-id="0825e-108">Exempel 1: ta bort en HTTP-lyssnare för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="0825e-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="0825e-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="0825e-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0825e-110">Med det andra kommandot tas HTTP-lyssnaren bort med namnet Listener02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0825e-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0825e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0825e-111">PARAMETERS</span></span>

### <span data-ttu-id="0825e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0825e-112">-ApplicationGateway</span></span>
<span data-ttu-id="0825e-113">Anger den Programgateway från vilken du vill ta bort en HTTP-lyssnare.</span><span class="sxs-lookup"><span data-stu-id="0825e-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="0825e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0825e-114">-DefaultProfile</span></span>
<span data-ttu-id="0825e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0825e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0825e-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0825e-116">-Name</span></span>
<span data-ttu-id="0825e-117">Anger namnet på den HTTP-lyssnare som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0825e-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0825e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0825e-118">CommonParameters</span></span>
<span data-ttu-id="0825e-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0825e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0825e-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0825e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0825e-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0825e-121">INPUTS</span></span>

### <span data-ttu-id="0825e-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0825e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0825e-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0825e-123">OUTPUTS</span></span>

### <span data-ttu-id="0825e-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0825e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="0825e-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0825e-125">NOTES</span></span>

## <span data-ttu-id="0825e-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0825e-126">RELATED LINKS</span></span>

[<span data-ttu-id="0825e-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0825e-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="0825e-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0825e-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="0825e-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0825e-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="0825e-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0825e-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


