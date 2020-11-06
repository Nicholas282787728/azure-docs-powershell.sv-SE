---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 94cb9e07bc5d4b8d59e543c39ddada5386ebcb27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574797"
---
# <span data-ttu-id="0a723-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0a723-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="0a723-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a723-102">SYNOPSIS</span></span>
<span data-ttu-id="0a723-103">Tar bort en front-IP-konfiguration från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0a723-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a723-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a723-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a723-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a723-105">DESCRIPTION</span></span>
<span data-ttu-id="0a723-106">Cmdleten **Remove-AzureRmApplicationGatewayFrontendIPConfig** tar bort nät ports-IP från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0a723-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="0a723-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a723-107">EXAMPLES</span></span>

### <span data-ttu-id="0a723-108">Exempel 1: ta bort en front-IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="0a723-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="0a723-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="0a723-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0a723-110">Det andra kommandot tar bort front-IP-konfigurationen som heter FrontEndIP02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0a723-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0a723-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a723-111">PARAMETERS</span></span>

### <span data-ttu-id="0a723-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a723-112">-ApplicationGateway</span></span>
<span data-ttu-id="0a723-113">Anger en Programgateway från vilken en front-IP-konfiguration ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0a723-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0a723-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a723-114">-DefaultProfile</span></span>
<span data-ttu-id="0a723-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a723-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a723-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0a723-116">-Name</span></span>
<span data-ttu-id="0a723-117">Anger namnet på en klient konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0a723-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="0a723-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a723-118">CommonParameters</span></span>
<span data-ttu-id="0a723-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a723-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a723-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a723-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a723-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a723-121">INPUTS</span></span>

### <span data-ttu-id="0a723-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a723-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="0a723-123">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0a723-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="0a723-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a723-124">OUTPUTS</span></span>

### <span data-ttu-id="0a723-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a723-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0a723-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a723-126">NOTES</span></span>

## <span data-ttu-id="0a723-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a723-127">RELATED LINKS</span></span>

[<span data-ttu-id="0a723-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0a723-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0a723-129">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0a723-129">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0a723-130">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0a723-130">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0a723-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0a723-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


