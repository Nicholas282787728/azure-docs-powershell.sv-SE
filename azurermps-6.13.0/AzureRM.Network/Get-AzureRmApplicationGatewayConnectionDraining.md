---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 147727cffc03de5ba8848705cf79facdbdc43320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576916"
---
# <span data-ttu-id="c56fb-101">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c56fb-101">Get-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="c56fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c56fb-102">SYNOPSIS</span></span>
<span data-ttu-id="c56fb-103">Hämtar anslutningen för ett backend HTTP Settings-objekt.</span><span class="sxs-lookup"><span data-stu-id="c56fb-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c56fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c56fb-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c56fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c56fb-105">DESCRIPTION</span></span>
<span data-ttu-id="c56fb-106">Cmdleten **Get-AzureRmApplicationGatewayConnectionDraining** hämtar anslutningen för ett backend http Settings-objekt.</span><span class="sxs-lookup"><span data-stu-id="c56fb-106">The **Get-AzureRmApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c56fb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c56fb-107">EXAMPLES</span></span>

### <span data-ttu-id="c56fb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c56fb-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="c56fb-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="c56fb-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c56fb-110">Det andra kommandot får de backend-HTTP-inställningarna "Settings01" för $AppGw och lagrar inställningarna i $Settings-variabeln.</span><span class="sxs-lookup"><span data-stu-id="c56fb-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="c56fb-111">Med det senaste kommandot får anslutningen tömning av konfigurationen från backend-HTTP-inställningarna $Settings och lagras i $ConnectionDraining-variabeln.</span><span class="sxs-lookup"><span data-stu-id="c56fb-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="c56fb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c56fb-112">PARAMETERS</span></span>

### <span data-ttu-id="c56fb-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c56fb-113">-BackendHttpSettings</span></span>
<span data-ttu-id="c56fb-114">Server delens http-inställningar</span><span class="sxs-lookup"><span data-stu-id="c56fb-114">The backend http settings</span></span>

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

### <span data-ttu-id="c56fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56fb-115">-DefaultProfile</span></span>
<span data-ttu-id="c56fb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c56fb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c56fb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56fb-117">CommonParameters</span></span>
<span data-ttu-id="c56fb-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c56fb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56fb-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c56fb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56fb-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c56fb-120">INPUTS</span></span>

### <span data-ttu-id="c56fb-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c56fb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>
<span data-ttu-id="c56fb-122">Parametrar: BackendHttpSettings (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c56fb-122">Parameters: BackendHttpSettings (ByValue)</span></span>

## <span data-ttu-id="c56fb-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c56fb-123">OUTPUTS</span></span>

### <span data-ttu-id="c56fb-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c56fb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="c56fb-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c56fb-125">NOTES</span></span>

## <span data-ttu-id="c56fb-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c56fb-126">RELATED LINKS</span></span>

[<span data-ttu-id="c56fb-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c56fb-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="c56fb-128">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c56fb-128">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="c56fb-129">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c56fb-129">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c56fb-130">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c56fb-130">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c56fb-131">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c56fb-131">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)
