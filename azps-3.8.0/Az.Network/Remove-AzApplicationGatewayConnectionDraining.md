---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 342b8e73ff4e3b01cbf51ea567e8eb7490ecd5c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089767"
---
# <span data-ttu-id="9272e-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9272e-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9272e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9272e-102">SYNOPSIS</span></span>
<span data-ttu-id="9272e-103">Tar bort anslutningen tömning av ett objekt för HTTP-inställningar för backend.</span><span class="sxs-lookup"><span data-stu-id="9272e-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9272e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9272e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9272e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9272e-105">DESCRIPTION</span></span>
<span data-ttu-id="9272e-106">Cmdleten **Remove-AzApplicationGatewayConnectionDraining** tar bort anslutningen som tömmer konfigurationen för ett objekt med http-inställningar för backend.</span><span class="sxs-lookup"><span data-stu-id="9272e-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9272e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9272e-107">EXAMPLES</span></span>

### <span data-ttu-id="9272e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9272e-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="9272e-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="9272e-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9272e-110">Det andra kommandot får de backend-HTTP-inställningarna "Settings01" för $AppGw och lagrar inställningarna i $Settings-variabeln.</span><span class="sxs-lookup"><span data-stu-id="9272e-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="9272e-111">Med kommandot senaste tar du bort anslutningen tömning av backend HTTP-inställningar som lagras i $Settings.</span><span class="sxs-lookup"><span data-stu-id="9272e-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="9272e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9272e-112">PARAMETERS</span></span>

### <span data-ttu-id="9272e-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9272e-113">-BackendHttpSettings</span></span>
<span data-ttu-id="9272e-114">Server delens http-inställningar</span><span class="sxs-lookup"><span data-stu-id="9272e-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9272e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9272e-115">-DefaultProfile</span></span>
<span data-ttu-id="9272e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9272e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9272e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9272e-117">CommonParameters</span></span>
<span data-ttu-id="9272e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9272e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9272e-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9272e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9272e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9272e-120">INPUTS</span></span>

### <span data-ttu-id="9272e-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9272e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9272e-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9272e-122">OUTPUTS</span></span>

### <span data-ttu-id="9272e-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9272e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9272e-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9272e-124">NOTES</span></span>

## <span data-ttu-id="9272e-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9272e-125">RELATED LINKS</span></span>

[<span data-ttu-id="9272e-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9272e-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="9272e-127">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9272e-127">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="9272e-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9272e-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9272e-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9272e-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9272e-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9272e-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

