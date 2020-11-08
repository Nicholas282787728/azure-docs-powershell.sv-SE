---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 76c017589afd5f8ef0abb6f016dbc80bb5bc30d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089089"
---
# <span data-ttu-id="76873-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="76873-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="76873-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76873-102">SYNOPSIS</span></span>
<span data-ttu-id="76873-103">Ändrar anslutningen tömning av ett objekt för HTTP-inställningsobjektet.</span><span class="sxs-lookup"><span data-stu-id="76873-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="76873-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76873-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76873-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76873-105">DESCRIPTION</span></span>
<span data-ttu-id="76873-106">Cmdleten **set-AzApplicationGatewayWebApplicationFirewallConfiguration** ändrar anslutningen som tömmer konfigurationen för ett objekt med http-inställningar för backend.</span><span class="sxs-lookup"><span data-stu-id="76873-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="76873-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76873-107">EXAMPLES</span></span>

### <span data-ttu-id="76873-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="76873-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="76873-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="76873-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="76873-110">Det andra kommandot får de backend-HTTP-inställningarna "Settings01" för $AppGw och lagrar inställningarna i $Settings-variabeln.</span><span class="sxs-lookup"><span data-stu-id="76873-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="76873-111">Det senaste kommandot ändrar anslutningen tömning av det backend-HTTP-Setting-objekt som är lagrat i $Settings genom att aktivera till false och DrainTimeoutInSec till 3600.</span><span class="sxs-lookup"><span data-stu-id="76873-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="76873-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76873-112">PARAMETERS</span></span>

### <span data-ttu-id="76873-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="76873-113">-BackendHttpSettings</span></span>
<span data-ttu-id="76873-114">Server delens http-inställningar</span><span class="sxs-lookup"><span data-stu-id="76873-114">The backend http settings</span></span>

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

### <span data-ttu-id="76873-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76873-115">-DefaultProfile</span></span>
<span data-ttu-id="76873-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76873-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76873-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="76873-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="76873-118">Antalet sekunder som anslutningen är aktiv.</span><span class="sxs-lookup"><span data-stu-id="76873-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="76873-119">Godkända värden är mellan 1 sekund och 3600 sekunder.</span><span class="sxs-lookup"><span data-stu-id="76873-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="76873-120">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="76873-120">-Enabled</span></span>
<span data-ttu-id="76873-121">Om anslutning är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="76873-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="76873-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76873-122">CommonParameters</span></span>
<span data-ttu-id="76873-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76873-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76873-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76873-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76873-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76873-125">INPUTS</span></span>

### <span data-ttu-id="76873-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="76873-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="76873-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76873-127">OUTPUTS</span></span>

### <span data-ttu-id="76873-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="76873-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="76873-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76873-129">NOTES</span></span>

## <span data-ttu-id="76873-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76873-130">RELATED LINKS</span></span>

[<span data-ttu-id="76873-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76873-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="76873-132">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="76873-132">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="76873-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="76873-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="76873-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="76873-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="76873-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="76873-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)
