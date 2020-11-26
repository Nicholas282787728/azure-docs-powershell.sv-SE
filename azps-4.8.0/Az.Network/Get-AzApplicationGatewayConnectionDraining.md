---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b6fe7d8be92e2d82762557a05bf88ef053e0d407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102730"
---
# <span data-ttu-id="b8a88-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8a88-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="b8a88-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8a88-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a88-103">Hämtar anslutningen för ett backend HTTP Settings-objekt.</span><span class="sxs-lookup"><span data-stu-id="b8a88-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="b8a88-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8a88-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8a88-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8a88-105">DESCRIPTION</span></span>
<span data-ttu-id="b8a88-106">Cmdleten **Get-AzApplicationGatewayConnectionDraining** hämtar anslutningen för ett backend http Settings-objekt.</span><span class="sxs-lookup"><span data-stu-id="b8a88-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="b8a88-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8a88-107">EXAMPLES</span></span>

### <span data-ttu-id="b8a88-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b8a88-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="b8a88-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="b8a88-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b8a88-110">Det andra kommandot får de backend-HTTP-inställningarna "Settings01" för $AppGw och lagrar inställningarna i $Settings-variabeln.</span><span class="sxs-lookup"><span data-stu-id="b8a88-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="b8a88-111">Med det senaste kommandot får anslutningen tömning av konfigurationen från backend-HTTP-inställningarna $Settings och lagras i $ConnectionDraining-variabeln.</span><span class="sxs-lookup"><span data-stu-id="b8a88-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="b8a88-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8a88-112">PARAMETERS</span></span>

### <span data-ttu-id="b8a88-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b8a88-113">-BackendHttpSettings</span></span>
<span data-ttu-id="b8a88-114">Server delens http-inställningar</span><span class="sxs-lookup"><span data-stu-id="b8a88-114">The backend http settings</span></span>

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

### <span data-ttu-id="b8a88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a88-115">-DefaultProfile</span></span>
<span data-ttu-id="b8a88-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8a88-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8a88-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a88-117">CommonParameters</span></span>
<span data-ttu-id="b8a88-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8a88-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a88-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8a88-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a88-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8a88-120">INPUTS</span></span>

### <span data-ttu-id="b8a88-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b8a88-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b8a88-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8a88-122">OUTPUTS</span></span>

### <span data-ttu-id="b8a88-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8a88-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="b8a88-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8a88-124">NOTES</span></span>

## <span data-ttu-id="b8a88-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8a88-125">RELATED LINKS</span></span>

[<span data-ttu-id="b8a88-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8a88-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="b8a88-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b8a88-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="b8a88-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8a88-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b8a88-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8a88-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b8a88-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8a88-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)