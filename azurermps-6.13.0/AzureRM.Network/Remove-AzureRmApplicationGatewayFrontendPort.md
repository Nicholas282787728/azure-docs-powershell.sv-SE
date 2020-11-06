---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: de99be99c7b393af6cbbcac8ad9d293c93f4d5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574796"
---
# <span data-ttu-id="28593-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="28593-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="28593-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28593-102">SYNOPSIS</span></span>
<span data-ttu-id="28593-103">Tar bort en front port från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="28593-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28593-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28593-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28593-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28593-105">DESCRIPTION</span></span>
<span data-ttu-id="28593-106">Cmdleten **Remove-AzureRmApplicationGatewayFrontendPort** tar bort en front port från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="28593-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="28593-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28593-107">EXAMPLES</span></span>

### <span data-ttu-id="28593-108">Exempel: ta bort en klient port från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="28593-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="28593-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar gatewayen i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="28593-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="28593-110">Det andra kommandot tar bort porten som heter FrontEndPort02 från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="28593-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="28593-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28593-111">PARAMETERS</span></span>

### <span data-ttu-id="28593-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28593-112">-ApplicationGateway</span></span>
<span data-ttu-id="28593-113">Anger den Programgateway från vilken du vill ta bort en front port.</span><span class="sxs-lookup"><span data-stu-id="28593-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="28593-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28593-114">-DefaultProfile</span></span>
<span data-ttu-id="28593-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28593-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28593-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="28593-116">-Name</span></span>
<span data-ttu-id="28593-117">Anger namnet på klient delen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="28593-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="28593-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28593-118">CommonParameters</span></span>
<span data-ttu-id="28593-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28593-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28593-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28593-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28593-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28593-121">INPUTS</span></span>

### <span data-ttu-id="28593-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28593-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="28593-123">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28593-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="28593-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28593-124">OUTPUTS</span></span>

### <span data-ttu-id="28593-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28593-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="28593-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28593-126">NOTES</span></span>

## <span data-ttu-id="28593-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28593-127">RELATED LINKS</span></span>

[<span data-ttu-id="28593-128">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="28593-128">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="28593-129">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="28593-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="28593-130">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="28593-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="28593-131">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="28593-131">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


