---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ca03b95748203546fb8d9235cb7822a4dde359a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584640"
---
# <span data-ttu-id="f775b-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f775b-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f775b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f775b-102">SYNOPSIS</span></span>
<span data-ttu-id="f775b-103">Skapar en ny anslutning för konfiguration av backend-HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="f775b-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f775b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f775b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f775b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f775b-105">DESCRIPTION</span></span>
<span data-ttu-id="f775b-106">Cmdleten **New-AzureRmApplicationGatewayConnectionDraining** skapar en ny anslutning för konfiguration av backend-http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="f775b-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="f775b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f775b-107">EXAMPLES</span></span>

### <span data-ttu-id="f775b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f775b-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="f775b-109">Kommandot skapar en ny konfiguration för tömning av anslutning med aktiverat värdet true och DrainTimeoutInSec angivet till 42 sekunder och lagrar det i $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="f775b-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="f775b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f775b-110">PARAMETERS</span></span>

### <span data-ttu-id="f775b-111">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="f775b-111">-DrainTimeoutInSec</span></span>
<span data-ttu-id="f775b-112">Antalet sekunder som anslutningen är aktiv.</span><span class="sxs-lookup"><span data-stu-id="f775b-112">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="f775b-113">Godkända värden är mellan 1 sekund och 3600 sekunder.</span><span class="sxs-lookup"><span data-stu-id="f775b-113">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="f775b-114">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="f775b-114">-Enabled</span></span>
<span data-ttu-id="f775b-115">Om anslutning är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="f775b-115">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="f775b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f775b-116">-DefaultProfile</span></span>
<span data-ttu-id="f775b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f775b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f775b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f775b-118">CommonParameters</span></span>
<span data-ttu-id="f775b-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f775b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f775b-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f775b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f775b-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f775b-121">INPUTS</span></span>

### <span data-ttu-id="f775b-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="f775b-122">None</span></span>

## <span data-ttu-id="f775b-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f775b-123">OUTPUTS</span></span>

### <span data-ttu-id="f775b-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f775b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f775b-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f775b-125">NOTES</span></span>

## <span data-ttu-id="f775b-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f775b-126">RELATED LINKS</span></span>

[<span data-ttu-id="f775b-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f775b-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f775b-128">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f775b-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f775b-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f775b-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

