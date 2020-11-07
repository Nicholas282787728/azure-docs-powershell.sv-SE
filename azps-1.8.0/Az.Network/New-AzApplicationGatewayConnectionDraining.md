---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3401010e1b65dbd0ad24f634c32b06449671419f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748153"
---
# <span data-ttu-id="623ef-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="623ef-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="623ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="623ef-102">SYNOPSIS</span></span>
<span data-ttu-id="623ef-103">Skapar en ny anslutning för konfiguration av backend-HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="623ef-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="623ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="623ef-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="623ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="623ef-105">DESCRIPTION</span></span>
<span data-ttu-id="623ef-106">Cmdleten **New-AzApplicationGatewayConnectionDraining** skapar en ny anslutning för konfiguration av backend-http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="623ef-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="623ef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="623ef-107">EXAMPLES</span></span>

### <span data-ttu-id="623ef-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="623ef-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="623ef-109">Kommandot skapar en ny konfiguration för tömning av anslutning med aktiverat värdet true och DrainTimeoutInSec angivet till 42 sekunder och lagrar det i $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="623ef-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="623ef-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="623ef-110">PARAMETERS</span></span>

### <span data-ttu-id="623ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623ef-111">-DefaultProfile</span></span>
<span data-ttu-id="623ef-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="623ef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="623ef-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="623ef-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="623ef-114">Antalet sekunder som anslutningen är aktiv.</span><span class="sxs-lookup"><span data-stu-id="623ef-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="623ef-115">Godkända värden är mellan 1 sekund och 3600 sekunder.</span><span class="sxs-lookup"><span data-stu-id="623ef-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="623ef-116">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="623ef-116">-Enabled</span></span>
<span data-ttu-id="623ef-117">Om anslutning är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="623ef-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="623ef-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623ef-118">CommonParameters</span></span>
<span data-ttu-id="623ef-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623ef-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623ef-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="623ef-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623ef-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="623ef-121">INPUTS</span></span>

### <span data-ttu-id="623ef-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="623ef-122">None</span></span>

## <span data-ttu-id="623ef-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="623ef-123">OUTPUTS</span></span>

### <span data-ttu-id="623ef-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="623ef-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="623ef-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="623ef-125">NOTES</span></span>

## <span data-ttu-id="623ef-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="623ef-126">RELATED LINKS</span></span>

[<span data-ttu-id="623ef-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="623ef-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="623ef-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="623ef-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="623ef-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="623ef-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

