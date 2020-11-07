---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 421bc74fb110aa48ff72388462e5496d9ceb1434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576866"
---
# <span data-ttu-id="98157-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="98157-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="98157-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98157-102">SYNOPSIS</span></span>
<span data-ttu-id="98157-103">Ändrar anslutningen tömning av ett objekt för HTTP-inställningsobjektet.</span><span class="sxs-lookup"><span data-stu-id="98157-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98157-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98157-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98157-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98157-105">DESCRIPTION</span></span>
<span data-ttu-id="98157-106">Cmdleten **set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** ändrar anslutningen som tömmer konfigurationen för ett objekt med http-inställningar för backend.</span><span class="sxs-lookup"><span data-stu-id="98157-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="98157-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98157-107">EXAMPLES</span></span>

### <span data-ttu-id="98157-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="98157-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="98157-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="98157-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="98157-110">Det andra kommandot får de backend-HTTP-inställningarna "Settings01" för $AppGw och lagrar inställningarna i $Settings-variabeln.</span><span class="sxs-lookup"><span data-stu-id="98157-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="98157-111">Det senaste kommandot ändrar anslutningen tömning av det backend-HTTP-Setting-objekt som är lagrat i $Settings genom att aktivera till false och DrainTimeoutInSec till 3600.</span><span class="sxs-lookup"><span data-stu-id="98157-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="98157-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98157-112">PARAMETERS</span></span>

### <span data-ttu-id="98157-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="98157-113">-BackendHttpSettings</span></span>
<span data-ttu-id="98157-114">Server delens http-inställningar</span><span class="sxs-lookup"><span data-stu-id="98157-114">The backend http settings</span></span>

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

### <span data-ttu-id="98157-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98157-115">-DefaultProfile</span></span>
<span data-ttu-id="98157-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98157-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98157-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="98157-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="98157-118">Antalet sekunder som anslutningen är aktiv.</span><span class="sxs-lookup"><span data-stu-id="98157-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="98157-119">Godkända värden är mellan 1 sekund och 3600 sekunder.</span><span class="sxs-lookup"><span data-stu-id="98157-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="98157-120">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="98157-120">-Enabled</span></span>
<span data-ttu-id="98157-121">Om anslutning är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="98157-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98157-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98157-122">CommonParameters</span></span>
<span data-ttu-id="98157-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98157-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98157-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98157-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98157-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98157-125">INPUTS</span></span>

### <span data-ttu-id="98157-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="98157-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>
<span data-ttu-id="98157-127">Parametrar: BackendHttpSettings (ByValue)</span><span class="sxs-lookup"><span data-stu-id="98157-127">Parameters: BackendHttpSettings (ByValue)</span></span>

## <span data-ttu-id="98157-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98157-128">OUTPUTS</span></span>

### <span data-ttu-id="98157-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="98157-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="98157-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98157-130">NOTES</span></span>

## <span data-ttu-id="98157-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98157-131">RELATED LINKS</span></span>

[<span data-ttu-id="98157-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98157-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="98157-133">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="98157-133">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="98157-134">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="98157-134">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="98157-135">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="98157-135">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="98157-136">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="98157-136">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)
