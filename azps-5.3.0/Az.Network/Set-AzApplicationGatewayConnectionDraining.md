---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: e2cecb2061b605c5380597c51cb72860596690cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523170"
---
# <span data-ttu-id="49a01-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="49a01-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="49a01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49a01-102">SYNOPSIS</span></span>
<span data-ttu-id="49a01-103">Ändrar anslutningen tömning av ett objekt för HTTP-inställningsobjektet.</span><span class="sxs-lookup"><span data-stu-id="49a01-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="49a01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49a01-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49a01-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49a01-105">DESCRIPTION</span></span>
<span data-ttu-id="49a01-106">Cmdleten **set-AzApplicationGatewayWebApplicationFirewallConfiguration** ändrar anslutningen som tömmer konfigurationen för ett objekt med http-inställningar för backend.</span><span class="sxs-lookup"><span data-stu-id="49a01-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="49a01-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49a01-107">EXAMPLES</span></span>

### <span data-ttu-id="49a01-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="49a01-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="49a01-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="49a01-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="49a01-110">Det andra kommandot får de backend-HTTP-inställningarna "Settings01" för $AppGw och lagrar inställningarna i $Settings-variabeln.</span><span class="sxs-lookup"><span data-stu-id="49a01-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="49a01-111">Det senaste kommandot ändrar anslutningen tömning av det backend-HTTP-Setting-objekt som är lagrat i $Settings genom att aktivera till false och DrainTimeoutInSec till 3600.</span><span class="sxs-lookup"><span data-stu-id="49a01-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="49a01-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49a01-112">PARAMETERS</span></span>

### <span data-ttu-id="49a01-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="49a01-113">-BackendHttpSettings</span></span>
<span data-ttu-id="49a01-114">Server delens http-inställningar</span><span class="sxs-lookup"><span data-stu-id="49a01-114">The backend http settings</span></span>

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

### <span data-ttu-id="49a01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a01-115">-DefaultProfile</span></span>
<span data-ttu-id="49a01-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49a01-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49a01-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="49a01-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="49a01-118">Antalet sekunder som anslutningen är aktiv.</span><span class="sxs-lookup"><span data-stu-id="49a01-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="49a01-119">Godkända värden är mellan 1 sekund och 3600 sekunder.</span><span class="sxs-lookup"><span data-stu-id="49a01-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="49a01-120">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="49a01-120">-Enabled</span></span>
<span data-ttu-id="49a01-121">Om anslutning är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="49a01-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="49a01-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a01-122">CommonParameters</span></span>
<span data-ttu-id="49a01-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49a01-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a01-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a01-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a01-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49a01-125">INPUTS</span></span>

### <span data-ttu-id="49a01-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="49a01-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="49a01-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49a01-127">OUTPUTS</span></span>

### <span data-ttu-id="49a01-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="49a01-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="49a01-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49a01-129">NOTES</span></span>

## <span data-ttu-id="49a01-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49a01-130">RELATED LINKS</span></span>

[<span data-ttu-id="49a01-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49a01-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="49a01-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="49a01-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="49a01-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="49a01-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="49a01-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="49a01-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="49a01-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="49a01-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

