---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 4079d8b6859a2860116520c52928d13c7e3fa29e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758154"
---
# <span data-ttu-id="695f3-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="695f3-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="695f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="695f3-102">SYNOPSIS</span></span>
<span data-ttu-id="695f3-103">Tar bort en HTTP-lyssnare från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="695f3-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="695f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="695f3-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="695f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="695f3-105">DESCRIPTION</span></span>
<span data-ttu-id="695f3-106">Cmdleten **Remove-AzureRmApplicationGatewayHttpListener** tar bort en http-lyssnare från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="695f3-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="695f3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="695f3-107">EXAMPLES</span></span>

### <span data-ttu-id="695f3-108">Exempel 1: ta bort en HTTP-lyssnare för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="695f3-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="695f3-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="695f3-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="695f3-110">Med det andra kommandot tas HTTP-lyssnaren bort med namnet Listener02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="695f3-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="695f3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="695f3-111">PARAMETERS</span></span>

### <span data-ttu-id="695f3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="695f3-112">-ApplicationGateway</span></span>
<span data-ttu-id="695f3-113">Anger den Programgateway från vilken du vill ta bort en HTTP-lyssnare.</span><span class="sxs-lookup"><span data-stu-id="695f3-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="695f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695f3-114">-DefaultProfile</span></span>
<span data-ttu-id="695f3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="695f3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695f3-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="695f3-116">-Name</span></span>
<span data-ttu-id="695f3-117">Anger namnet på den HTTP-lyssnare som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="695f3-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="695f3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695f3-118">CommonParameters</span></span>
<span data-ttu-id="695f3-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="695f3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695f3-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="695f3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695f3-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="695f3-121">INPUTS</span></span>

### <span data-ttu-id="695f3-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="695f3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="695f3-123">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="695f3-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="695f3-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="695f3-124">OUTPUTS</span></span>

### <span data-ttu-id="695f3-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="695f3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="695f3-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="695f3-126">NOTES</span></span>

## <span data-ttu-id="695f3-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="695f3-127">RELATED LINKS</span></span>

[<span data-ttu-id="695f3-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="695f3-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="695f3-129">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="695f3-129">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="695f3-130">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="695f3-130">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="695f3-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="695f3-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


